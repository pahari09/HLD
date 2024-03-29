We dive into three parts of security

1> Verification
 
 Types of Verification:
   *Captcha:
     Definition: 
	  Captcha verification (or Completely Automated Public Turing Test to tell Computers and Humans Apart) is a common web technique used to help ensure that your respondents are real humans and not a program written to spam your survey. In a captcha verification, the respondent is presented with a picture (or “challenge”) of words or characters, and the respondent must correctly type out those characters in order to proceed.
	  Captcha is a third-party service provided by Google. No respondent information is sent to Google as part of this service. Visit Google’s reCAPTCHA page to learn more. It’s also important to note that not all languages are supported by this feature, and that supported languages are owned and decided upon by Google. See Google’s documentation for more details.
	 
Video: https://www.youtube.com/watch?v=5ge3vM4JjLg&ab_channel=TechnicalSagar
   
   *SSL/TLS(Secure Socket Layer/Transport Layer security)
    SSL: 
	Concepts: https://www.cloudflare.com/en-gb/learning/ssl/what-is-ssl/
	 * In order to provide a high degree of privacy, SSL encrypts data that is transmitted across the web. This means that anyone who tries to intercept this data will only see a garbled mix of characters that is nearly impossible to decrypt.
     * SSL initiates an authentication process called a handshake between two communicating devices to ensure that both devices are really who they claim to be.
     * SSL also digitally signs data in order to provide data integrity, verifying that the data is not tampered with before reaching its intended recipient.
	 
TLS:
	  Concepts: https://www.cloudflare.com/en-gb/learning/ssl/transport-layer-security-tls/
	  
Transport Layer Security, or TLS, is a widely adopted security protocol designed to facilitate privacy and data security for communications over the Internet. A primary use case of TLS is encrypting the communication between web applications and servers, such as web browsers loading a website. TLS can also be used to encrypt other communications such as email, messaging, and voice over IP (VoIP).
   
     
   

2> Authentication
Definition: In simple terms, authentication is the process of verifying who a user is, while authorization is the process of verifying what they have access to.

Comparing these processes to a real-world example, when you go through security in an airport, you show your ID to authenticate your identity. Then, when you arrive at the gate, you present your boarding pass to the flight attendant, so they can authorize you to board your flight and allow access to the plane.

Types:
   =>Single Sign On
    Concept: Single Sign-On (SSO) is an authentication method that lets users access multiple applications and services using a single set of login credentials. SSO can help businesses improve user satisfaction and productivity, strengthen access security, and reduce IT operations expense and complexity.
	//Link: https://www.cyberark.com/what-is/sso/#:~:text=Single%20Sign%2DOn%20(SSO)%20is%20an%20authentication%20method%20that,IT%20operations%20expense%20and%20complexity.
     Two protocol: 
	   *SAML-based SSO 
		 Concept: Security Assertion Markup Language, or SAML, is a standardized way to tell external applications and services that a user is who they say they are. SAML makes single sign-on (SSO) technology possible by providing a way to authenticate a user once and then communicate that authentication to multiple applications. The most current version of SAML is SAML 2.0. 
		 //Link: https://www.cloudflare.com/en-gb/learning/access-management/what-is-saml/
		 //Video: https://www.youtube.com/watch?v=O1cRJWYF-g4&ab_channel=ByteByteGo
		 
*OpenID: .OpenID is an open specification for authentication and single sign-on (SSO). It was created in 2005 
	            to allow websites and authentication services to exchange security information in a standardized way.
	            .OpenID Connect (OIDC) is a protocol built on top of the OAuth 2.0 framework. It allows individuals to use SSO to access relying on party sites using OpenID Providers (OPs). OPs can be email providers or social networks.

=>User Tokens:
      Token-based authentication is a protocol which allows users to verify their identity, and in return receive a unique access token. During the life of the token, users then access the website or app that the token has been issued for, rather than having to re-enter credentials each time they go back to the same webpage, app, or any resource protected with that same token.
	  
Link: https://www.geeksforgeeks.org/how-does-the-token-based-authentication-work/

=>OAuth Authorization abused for authentication!)
     . It stands for open Authorization
	 .OAuth, or Open Authorization, is a standard for access delegation. It allows users to grant applications or   websites access to their information on other sites without giving them their passwords.
	 .OAuth is an open-standard authorization framework that enables third-party applications to gain limited access to user’s data.
	 eg  For example, you can tell Facebook that it’s OK for ESPN.com to access your profile or post updates to your timeline without having to give ESPN your Facebook password
	 .A  classic example of valet parking is often retold to understand this concept. In this case, the car owner has access to both the car and the valet. To have his car parked for him, the car owner gives the valet key to the attendant. The valet key starts the car and opens the driver’s side door but prevents the valet from accessing valuables in the trunk or glove box.
	 //Concepts Link:
       Video: https://www.youtube.com/watch?v=O8sgkKRIZyo&ab_channel=BittenTech
	   Page: https://www.geeksforgeeks.org/workflow-of-oauth-2-0/
	         https://www.csoonline.com/article/562635/what-is-oauth-how-the-open-authorization-framework-works.html
   
   =>Oauth 2.0
     *OAuth 2.0, or "Open Authorization", is a standard that allows a website or application to access resources on behalf of a user. It's the industry standard for online authorization.
	 *OAuth 2.0 allows users to share specific data with an application while keeping their usernames, passwords, and other information private. For example, an application can use OAuth 2.0 to obtain permission from users to store files in their Google Drives.
	 //Concepts: https://www.digitalocean.com/community/tutorials/an-introduction-to-oauth-2
       Video: https://www.youtube.com/watch?v=65-6asTjuB8&t=356s&ab_channel=GauravSen
	   
3>Authorization
Defination: In simple terms, authentication is the process of verifying who a user is, while authorization is the process of verifying what they have access to.

Comparing these processes to a real-world example, when you go through security in an airport, you show your ID to authenticate your identity. Then, when you arrive at the gate, you present your boarding pass to the flight attendant, so they can authorize you to board your flight and allow access to the plane.

Authentication vs. Authorization
 Concepts: 
 https://www.youtube.com/watch?v=B76BhEq1FN8&t=5s&ab_channel=EngineeringDigest
 https://auth0.com/docs/get-started/identity-fundamentals/authentication-and-authorization

Types:
   Access Control Lists:
    .An access control list includes a set of rules used to assign permissions or grant different levels of access to files and business-critical information.
	.Organizations can use access control lists (ACL) to secure data. One of the major reasons to use access control lists is to restrict unauthorized users from accessing business-sensitive information. It can also be used to control network traffic by limiting the number of users accessing files, systems, and information. This increases network performance and helps protect business information.
	.Advantages of using an ACL:
      -Help enhance network performance by limiting network traffic
      -Provide security by defining permission and access rights
      -Offer granular control over the traffic flow entering the network
	  
Concepts:https://www.solarwinds.com/resources/it-glossary/access-control-list-acl
Video:https://www.youtube.com/watch?v=ffB9i05VxVo&ab_channel=SheshChauhanITTrainer

   Rule Engines:
     .A rules engine is a software that uses a set of rules to determine if a user or resource has permission to perform an action. Rules engines are useful for handling complex authorization requirements.
	 .Rules engines are often implemented as if statements. For example, a basic rule might be "If A, then B, else if X, then do Y". 
     .Rules engines can handle multiple objects and rules efficiently. They are especially useful when there are many possible outcomes based on different conditions and criteria.
	 Concepts: https://medium.com/@er.rameshkatiyar/what-is-rule-engine-86ea759ad97d
