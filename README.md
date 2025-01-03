# Auth0 Developer Account Setup and API Resource Configuration

This guide provides a step-by-step walkthrough of how I signed up for an Auth0 developer account, created an API resource, set a default audience, and retrieved the Issuer URI for my OAuth server. Each step includes clear explanations and visual references.

## Steps

### 1. Sign Up for an Auth0 Developer Account
I started by visiting Auth0 and signing up for a developer account. After providing the necessary details like my email and password, I was guided to the Auth0 dashboard.

**Image Reference**: 
- A screenshot of the Auth0 signup page or the Auth0 dashboard after signing up.

---

### 2. Create an API Resource
To protect APIs using Auth0 access tokens, I created an API resource:

- In the sidebar, I navigated to **Applications** > **APIs**.
- Then, I clicked on **Create API**.
- I filled in the details:
  - **Name**: (Forge)
  - **Identifier**: (`https://api.forge.com`)
    - The **Identifier** becomes the value of the `audience` claim in access tokens.

Once I clicked **Create**, my new API resource was set up.

**Image Reference**:
- Screenshots showing the **Create API** button and the form for API details.

---

### 3. Set the Default Audience
Setting a default audience ensures that the access tokens issued can work with my API.

- I navigated to **Settings** from the sidebar.
- Scrolled down to the **API Authorization Settings** section, I entered the same API Identifier I used earlier (`https://api.forge.com`) into the **Default Audience** field.
- Finally, I saved my changes.

**Image Reference**:
- Screenshots of the **Settings** page and the **Default Audience** field filled in.

---

### 4. Find the Issuer URI
The **Issuer URI** is crucial for authentication and is derived from the OpenID Configuration URI.

- I navigated to **Applications** in the sidebar and clicked **Applications** again.
- I created a new application, SIFT
- After the application was created, I clicked on the **Settings** tab.
- Scrolled down, I expanded the **Advanced Settings** section and clicked on the **Endpoints** tab.
- From the **Endpoints** tab, I located the **OpenID Configuration URI**. The **Issuer URI** is part of this configuration and serves as the identifier of the authorization server.

**Image Reference**:
- Screenshots of the **Settings** page, **Advanced Settings**, and the **Endpoints** tab showing the **OpenID Configuration URI**.

---

### 5. Summary

At this stage, I had:

1. Signed up for Auth0.
2. Created an API resource to protect with access tokens.
3. Configured the default audience for my API.
4. Retrieved the Issuer URI for further exercises.
