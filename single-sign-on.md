## Single Sign-On (SSO) in Microsoft Entra ID

---

**What is Single Sign-On (SSO)?**

- Single sign-on (SSO) is an authentication method that allows users to access multiple independent software systems with a single set of credentials.
- With SSO, users sign in once and gain access to all assigned applications without needing to authenticate again for each one.
- SSO improves user experience and security by reducing password fatigue and centralizing authentication[4].

---

**SSO Options in Microsoft Entra ID**

Microsoft Entra ID supports several SSO methods, depending on the application and its authentication capabilities:

| SSO Method              | Description                                                                                   | Protocols Supported          |
|-------------------------|----------------------------------------------------------------------------------------------|------------------------------|
| Federated SSO           | Uses federation protocols to authenticate users via Entra ID.                                 | SAML 2.0, OpenID Connect, WS-Federation |
| Password-based SSO      | Entra ID stores and replays credentials for apps that don't support federation.               | Native app login forms       |
| Linked SSO              | Publishes links to applications for easy access during migrations.                           | N/A                          |
| Disabled SSO            | No SSO; users must authenticate separately in each app.                                      | N/A                          |

- **Federated SSO** is the most secure and feature-rich, enabling seamless authentication using modern protocols.

---

**Planning and Prerequisites for SSO Deployment**

Before deploying SSO, consider:

- Application compatibility with SSO protocols (SAML, OpenID Connect, etc.).
- Required user roles in Entra ID: Cloud Application Administrator, Application Administrator, or Service Principal Owner.
- User and group assignments for application access.
- Testing in a controlled environment before production rollout.

---

**Typical Steps to Configure SSO in Microsoft Entra ID**

1. **Register the Application**
   - Add the application from the Entra ID gallery or register a custom (non-gallery) app.
   - Assign users or groups who need access.

2. **Configure SSO Method**
   - Navigate to **Identity > Applications > Enterprise applications > [Your App] > Single sign-on** in the Entra admin center.
   - Choose the SSO method (commonly SAML for third-party SaaS apps).

3. **Set Up SAML/Protocol Settings**
   - Enter required values such as Entity ID, Reply URL (ACS URL), and Sign-on URL as provided by the service provider.
   - Configure attribute mappings (e.g., user.email, user.givenname) as required by the application
4. **Download and Share Metadata**
   - Download the SAML metadata or certificate from Entra ID and upload it to the service provider.

5. **Test and Assign Users**
   - Test SSO with a pilot user to ensure successful authentication.
   - Assign the application to additional users or groups as needed.

---

**Key Concepts and Best Practices**

- **Just-in-Time (JIT) Provisioning:** Some applications support automatic account creation upon first SSO login.
- **Role-Based Access Control (RBAC):** Use Entra ID groups and roles to manage who can access which applications.
- **Security:** Always use federated SSO where possible; avoid password-based SSO for sensitive applications.
- **Centralized Management:** Entra ID allows you to manage all user access and credentials in one place, simplifying administration.

---

**Summary Table: SSO Setup Workflow**


| Step                         | Action                                                                                      |
|------------------------------|---------------------------------------------------------------------------------------------|
| Register Application         | Add from gallery or create custom app in Entra ID                                           |
| Assign Users/Groups          | Grant access to the appropriate users or groups                                             |
| Configure SSO Protocol       | Choose and configure SAML/OpenID Connect/other protocol settings                            |
| Attribute Mapping            | Map user attributes as required by the service provider                                     |
| Metadata Exchange            | Share SAML metadata/certificates between Entra ID and the application                       |
| Test & Rollout               | Test with pilot users, then assign to production users                                      |

---

