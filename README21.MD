

## What is JWT?
JWT is an acronym for JSON Web Token. JWT is a way for securely transmitting information between parties as a JSON object. This information is verified and trusted because it’s digitally signed. JWT’s can be using a secret (with the HMAC algorithm) or public/private key pair using RSA/ECDSA.

## JWT structure contains three parts:

1. Header: The header consists of two-part one is signing algorithm (HMAC, SHA256, etc.) and the other one is the type of the token which is JWT.

2. Payload : The payload contains the claims. Claims are statements about an entity (typically, the user) and additional data. Again the payload formed JSON is Base64Url encoded to form second part.

3. Signature: For the signature created you need to use encoded header, encoded payload, and secret with the algorithm specified at the header.


## Steps to follow:

1. Create a new project:
Visual Studio -> Create New Project -> Asp.Net Core Web application -> Select Web Api Template -> Create.

2. Install required a package of JWT from NuGet Package:
Right-click on project -> Manage NuGet package -> On browse section search for (Microsoft.AspNetCore.Authentication.JwtBearer) -> install.

3. Update Startup.cs ConfigureService() to register JWT authentication scheme,

services.AddAuthentication(JwtBearerDefaults.AuthenticationScheme)
.AddJwtBearer(options =>
{
options.RequireHttpsMetadata = false;
options.SaveToken = true;
options.TokenValidationParameters = new TokenValidationParameters
{
ValidateIssuer = true,
ValidateAudience = true,
ValidateLifetime = true,
ValidateIssuerSigningKey = true,
ValidIssuer = Configuration[“Jwt:Issuer”],
ValidAudience = Configuration[“Jwt:Audience”],
IssuerSigningKey = new SymmetricSecurityKey(Encoding.UTF8.GetBytes(Configuration[“Jwt:SecretKey”])),
ClockSkew = TimeSpan.Zero
};
});

4.  A further step is to change in the appsettings.json with required details for JWT authentication scheme,

5. The next step is to make an authentication service available to the application to do this we need a call app.UseAuthentication in Configure() method,<br>

public void Configure(IApplicationBuilder app, IWebHostEnvironment env) <br>
{<br>
if (env.IsDevelopment())<br>
{
app.UseDeveloperExceptionPage();<br>
}
app.UseHttpsRedirection();<br>
app.UseRouting();<br>
app.UseAuthentication();<br>
app.UseAuthorization();<br>
app.UseEndpoints(endpoints =><br>
{<br>
endpoints.MapControllers();<br>
});<br>
}<br>

6. Update Startup.cs file ConfigureService() method to add authorization code,<br>

services.AddAuthorization(config =><br>
{<br>
config.AddPolicy(Policies.Admin, Policies.AdminPolicy());<br>
config.AddPolicy(Policies.User, Policies.UserPolicy());<br>
});<br>

7. Generate JSON Web Token

8. Defining the methods according to the role to check authorization

