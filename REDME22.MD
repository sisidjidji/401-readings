
## Policies 


- Underneath the covers, role-based authorization and claims-based authorization use a requirement, a requirement handler, and a pre-configured policy. These building blocks support the expression of authorization evaluations in code. The result is a richer, reusable, testable authorization structure.

- Examples of scenarios where a custom IAuthorizationPolicyProvider may be useful include:

1. Using an external service to provide policy evaluation.
2. Using a large range of policies (for different room numbers or ages, for example), so it doesn't make sense to add each individual authorization policy with an AuthorizationOptions.AddPolicy call.
3. Creating policies at runtime based on information in an external data source (like a database) or determining authorization requirements dynamically through another mechanism.


- The IAuthorizationPolicyProvider interface contains three APIs:

1. GetPolicyAsync returns an authorization policy for a given name.
2. GetDefaultPolicyAsync returns the default authorization policy (the policy used for [Authorize] attributes without a policy specified)
3. GetFallbackPolicyAsync returns the fallback authorization policy (the policy used by the Authorization Middleware when no policy is specified).

- When using custom IAuthorizationPolicyProvider implementations, keep in mind that ASP.NET Core only uses one instance of IAuthorizationPolicyProvider. If a custom provider isn't able to provide authorization policies for all policy names that will be used, it should defer to a backup provider.

For example, consider an application that needs both custom age policies and more traditional role-based policy retrieval. Such an app could use a custom authorization policy provider that:

Attempts to parse policy names.
Calls into a different policy provider (like DefaultAuthorizationPolicyProvider) if the policy name doesn't contain an age.