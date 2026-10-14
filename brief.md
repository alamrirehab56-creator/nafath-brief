Version: NAFATH-V1
Track:  Software 

## Overview
A national single sign-on system needs different IT fields to work together to provide secure and easy access to digital services. Software engineering is responsible for developing the system and making sure users can log in safely. Artificial intelligence can help identify unusual login attempts and detect possible threats. Mobile development focuses on protecting user information and controlling app permissions on smartphones. Networking helps keep communication between users and the system secure. Cybersecurity protects accounts from hackers and unauthorized access by using strong authentication methods. Data management ensures that users’ personal information is stored and handled safely according to data protection laws. The Software track focuses on securely validating OpenID Connect ID tokens across multiple services.
## Software
OAuth 2.0 and OpenID Connect serve distinct functions. OAuth 2.0 is a framework for authorizaion enabling applications to obtain access to secured resources for a user with their consent. OpenID Connect enhances OAuth 2.0 withan identity layer and enables user login through identity verification. An ID token is utilized to convey details regardingthe authentication event. Thus, OAuth 2.0 enables delegated resource access, whereas OpenID Connect facilitates user authentication.

Resource: OpenID Connect Core 1.0 — Section 1, Introduction — https://openid.net/specs/openid-connect-core-1_0.html


## AI
AI can help the national login service detect suspicious login attempts by looking at user activity. However, it may sometimes flag a normal login by mistake or miss a real threat. Before using the model, the authority should check its accuracy, reliability, fairness, security, and privacy risks. The NIST AI Risk Management Framework explains how these risks can be identified, measured, and managed. The model should also be tested and monitored after launch.

Resource: NIST AI Risk Management Framework (AI RMF 1.0) — https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf


## Mobile
Mobile apps may need access to features like the camera, location, or contacts. On supported Android versions, users must approve certain sensitive permissions when the app needs them. The app should explain why it needs permission and only ask for access when necessary. If a user refuses, the app should handle this properly. This helps protect personal information and gives users more control over what the login app can access on their phones.

Resource: Android Developers — Request app permissions — https://developer.android.com/training/permissions/requesting


## Networking
DNS over HTTPS (DoH) sends DNS requests through an encrypted HTTPS connection. It helps protect users by making DNS traffic harder for others on the network to read or change. It also helps prevent some attacks that redirect users to fake servers. However, DoH does not hide all online activity or protect every part of the connection. The service still needs other security measures, such as HTTPS, to protect users.

Resource: RFC 8484 - DNS Queries over HTTPS (DoH) - https://www.rfc-editor.org/rfc/rfc8484

## Cybersecurity
Phishing-resistant authentication helps stop attackers from stealing login details through fake websites. Passkeys and FIDO2 security keys can provide phishing-resistant authentication because they are linked to the legitimate website. However, passwords and manually entered one-time codes, including SMS codes, are not considered phishing-resistant. Using phishing-resistant methods can make account login safer and reduce the risk of attackers pretending to be trusted services.

Resource: NIST SP 800-63B-4 - Authentication and Authenticator Management - https://pages.nist.gov/800-63-4/sp800-63b.html


## Data
Under Oman’s Personal Data Protection Law, the authority must handle citizens’ personal data transparently and lawfully. It generally needs explicit consent before processing personal data, although the law lists exceptions. The authority should protect stored data, limit access, and respect people’s rights to request corrections, copies, or deletion where applicable. It must also follow the law’s requirements for handling personal data breaches and other data protection responsibilities.

Resource: Royal Decree 6/2022 - Personal Data Protection Law (Consolidated) - https://decree.om/2022/l20220006/


## Misconception in My Track
A common misconception is that OAuth 2.0 is a login protocol that confirms a user’s identity. In fact, OAuth 2.0 is mainly designed for authorization, allowing applications to access protected resources with permission. OpenID Connect adds an identity layer to OAuth 2.0 and supports user authentication. For example, an application can use an ID token to receive information about the authentication event. Therefore, developers should use OpenID Connect when they need a standard way to verify a user’s identity. This difference is explained in the “Introduction” (Section 1) of the OpenID Connect Core 1.0 specification.

## Open Question
How should a software developer validate OpenID Connect ID tokens to ensure they are genuine and have not expired before allowing users to access government services?
