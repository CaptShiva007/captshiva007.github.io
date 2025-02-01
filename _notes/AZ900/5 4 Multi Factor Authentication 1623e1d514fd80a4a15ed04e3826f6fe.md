# 5.4 Multi Factor Authentication

Having just one key is never enough, sometimes we need different authentication mechanisms to ensure security. 

> It’s not about something you know, like password. But something you have or something you are, or in 3FA both.
> 

Azure incorporates MFA as a key component for Azure Entra ID, for sign in and transactions.

### Benefits

- Increased security, prevents the risk of unauthorized access because even if one set of credentials are compromised, unauthorized users still need to bypass additional security features.
- Flexibility, users can choose from a variety of authentication methods like OTP, biometrics, etc.
- Compliance, MFA helps organizations meet various compliance standards.

### Common Methods

- Phone calls
- Text Messages
- Mobile app notifications
- Biometrics
- Authenticator apps

### Use Cases

- Securing cloud access
- Remote work security

> MFA is best with the help of conditional access policies
>