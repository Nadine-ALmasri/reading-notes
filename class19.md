 # Claims-Based Authorization in ASP.NET Core

## Claims and Identity:

Claims are name-value pairs representing characteristics of a subject (user).
Claims are issued by a trusted party and indicate information about the subject, not their permissions.
Example: A driver's license claim with "DateOfBirth: 8th June 1970" issued by a driving license authority.
Authorization Process:

Claims-based authorization checks the value of a claim to determine access to resources.
Access decisions are based on evaluating claims and trusting their issuers.
## Adding Claims Checks:

Claims checks are declarative and applied to Razor Pages, controllers, or their actions.
Claims requirements are policy-based and specified using the RequireClaim method.
Policies express required claims for access.
## Building and Registering Policies:

Policies are registered in the Authorization service configuration.
Example: Registering an "EmployeeOnly" policy requiring the "EmployeeNumber" claim.
## Applying Policies with [Authorize] Attribute:

- The [Authorize] attribute applies policies to actions or controllers.
Restricts access based on fulfilling specified policies.
Applying Policies to Razor Pages:

- The [Authorize] attribute can be applied to Razor Pages.
Policies are applied to the entire page, not individual handler methods.
Allowing Anonymous Access:

- Use the [AllowAnonymous] attribute to allow access to specific actions within a protected controller.
Useful when needing both protected and public actions in a controller.
Specifying Allowed Claim Values:

## Policies can specify allowed claim values.
Example: A "Founders" policy allows access only to employees with specific employee numbers.
## Using RequireAssertion for Custom Checks:

Use RequireAssertion when claim values require transformation or complex checks.
Example: Custom logic to check claims beyond simple comparisons.
Multiple Policy Evaluation:

When multiple policies are applied, all must be satisfied for access.
Example: An action requires both "EmployeeOnly" and "HumanResources" policies.
## Custom Policy Handlers for Complex Checks:

For advanced scenarios, custom policy handlers are used.
Example: Calculating age from birthdate and requiring a minimum age.
## Authentication vs Authorization:
1. differnt between them :
- Authentication: Determining the identity of a user.
- Authorization: Deciding what actions a user is allowed to perform.
2. Authentication in ASP.NET Core:

ASP.NET Core maintains the concept of identity properties.
In ASP.NET Core, User property on HttpContext is of type ClaimsPrincipal.
3. Claims-Based Authentication:

Claims are statements about an identity, consisting of a name and a value.
Claims describe properties of the identity (e.g., DateOfBirth, FirstName, IsVIP).
Claims are different from permissions; they represent "who" an identity is, not "what" it can do.
4. Claims and Identities:

An identity in ASP.NET Core is represented by a ClaimsIdentity.
A ClaimsIdentity contains properties like AuthenticationType, IsAuthenticated, and Claims.
Claims holds a collection of claims associated with the identity.
5. AuthenticationType and IsAuthenticated:

AuthenticationType: Method used for user authentication (e.g., Cookies, Bearer, Google).
IsAuthenticated: Indicates if an identity is authenticated.
Unauthenticated users may have identities with claims, useful for scenarios like guest users.
6. Multiple Identities:

A ClaimsPrincipal is the main class representing a user.
ClaimsPrincipal contains multiple ClaimsIdentity instances.
Different identities can represent different forms of identity, each with its own set of claims.
7. Example Scenarios:

Example of using multiple identities at an airport to demonstrate the concept.
Different forms of identity (passport, boarding pass) for different security checks.
Claims are inherited by the ClaimsPrincipal from its Identities.
8. Role-Based Authorization:

ASP.NET Core supports role-based authorization using claims.
IsInRole method is used to check if a user belongs to a specific role.
Claims can be used to represent roles as well.
9. Creating a New Principal:

Building a ClaimsPrincipal involves creating a list of claims.
Claims represent different aspects of the identity.
Claims are used to construct a ClaimsIdentity.
The identity is used to create a new ClaimsPrincipal.
The user is signed in using the SignInAsync method.

## JWT (JSON Web Token) Recap:

1. JWT Overview:

JSON Web Token (JWT) is used for transferring claims between two parties securely.
Claims are encoded as a JSON object, and JWTs can be digitally signed using JSON Web Signature (JWS) or encrypted using JSON Web Encryption (JWE).
2. Purpose of JWT:

JWTs are used as access tokens for authentication.
JWTs encode information in JSON format and can be used to represent various claims or attributes of an identity.
3. JWT Components:

A JWT consists of three main parts: Header, Payload, and Signature.
4. Header:

Contains metadata about the JWT such as the signing algorithm used (alg) and the token type (typ).
Encoded as a base64 URL string.
5. Payload:

Contains the claims (custom data) and sometimes standard claims.
Standard claims include "exp" (expiry), "iat" (issued at), "iss" (issuer), "sub" (subject), "aud" (audience), and more.
Encoded as a base64 URL string.
6. Signature:

Created by encrypting the base64 URL encoded Header and Payload with a secret key.
Provides integrity and authenticity, allowing recipients to verify the sender and content.
Ensures the token hasn't been tampered with.

 [Home](./README.md) 