### Core Concept
* While hosting your own identity offers a great deal of freedom and customization, Externally-hosted identity is a reality for some SaaS providers. Their customers may simply require them to accept authentication from their identity provider. For other SaaS providers, it may be essential that they support authentication from a variety of well known providers. This could be essential to promoting customer acquisition and reducing the overall friction of the experience. The challenge of this model is that the SaaS provider has no control over the representation of the user within these environments. This means that you’ll need to take other measures to connect user identity with tenant identity and generate the tenant context that your system relies on.

### Key Considerations
* To connecting tenants to user can often be achieved though a federation mechanism that will connect user data with your tenant identity. With Amazon Cognito, for example, you can federate to external identity provider, storing tenant context in Cognito. When the tenant authenticates against the external identity provider, Cognito will stitch its data together with the user identity to get a token that includes tenant context.
* Your ability to support external providers will also be influenced by the authentication specifications that are supported by these external providers. Many comply with OIDC, for example, and may be able to conform to a standard flow. However, their implementation of that specification can vary.
* The degree to which external providers comply with token specifications can vary. The content of ID and Access token, for example, could vary from one implementation to the next. You’ll need to ensure that each provider can comply the needs of your SaaS environment.
* In some instances, you may be required to integrate with a custom identity provider that does not conform to any industry specifications. In these cases, you’ll have to determine how best to abstract away the custom characteristics of these integrations.
* While support externally-hosted identity providers can be essential to your success, you need to strike a balance between embracing one-off solutions and undermining the overall agility of your SaaS offering. If the onboarding of each tenant requires custom code and these integrations add increment overhead, this could end up impacting your ability to achieve the operational efficiency goals that SaaS demands.





