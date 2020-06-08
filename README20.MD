# Read20 

- ASP.NET Core Identity is a membership system that adds login functionality to ASP.NET Core apps. Users can create an account with the login information stored in Identity or they can use an external login provider. Supported external login providers include Facebook, Google, Microsoft Account, and Twitter.

- Create a Web app with authentication
Create an ASP.NET Core Web Application project with Individual User Accounts.

* Select File > New > Project.
* Select ASP.NET Core Web Application. Name the project WebApp1 to have the same namespace as the project download. Click OK.
* Select an ASP.NET Core Web Application, then select Change Authentication.
* Select Individual User Accounts and click OK.

- The generated project provides ASP.NET Core Identity as a Razor Class Library. The Identity Razor Class Library exposes endpoints with the Identity area. For example:

* /Identity/Account/Login
* /Identity/Account/Logout
* /Identity/Account/Manage