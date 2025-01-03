# Auth0 Developer Account Setup and API Resource Configuration

This guide provides a step-by-step walkthrough of how I signed up for an Auth0 developer account, created an API resource, set a default audience, and retrieved the Issuer URI for my OAuth server. Each step includes clear explanations and visual references.

## Steps

### 1. Sign Up for an Auth0 Developer Account

I started by visiting Auth0 and signing up for a developer account. After providing the necessary details like my email and password, I was guided to the Auth0 dashboard.

**Image Reference**:
![Screenshot 2025-01-02 094629](https://github.com/user-attachments/assets/90113364-3169-43bb-8b13-a117f9b3a4bf)


### 2. Create an API Resource

To protect APIs using Auth0 access tokens, I created an API resource:

- In the sidebar, I navigated to **Applications** > **APIs**.
- Then, I clicked on **Create API**.
- I filled in the details:
  - **Name**: (Forge)
  - **Identifier**: (https://api.forge.com)
    - The **Identifier** becomes the value of the `audience` claim in access tokens.

Once I clicked **Create**, my new API resource was set up.

**Image Reference**:
![Screenshot 2025-01-02 102451](https://github.com/user-attachments/assets/874877ba-c65b-4e17-9109-2108514cfaec)
![Screenshot 2025-01-02 102553](https://github.com/user-attachments/assets/bc30b3fa-9fdc-46cb-9e37-05fbdbc00536)



### 3. Set the Default Audience

Setting a default audience ensures that the access tokens issued can work with my API.

- I navigated to **Settings** from the sidebar.
- Scrolling down to the **API Authorization Settings** section, I entered the same API Identifier I used earlier (`https://api.forge.com`) into the **Default Audience** field. 
- Finally, I saved my changes.

**Image Reference**:
- ![Screenshot 2025-01-02 103116](https://github.com/user-attachments/assets/6cc2e4cb-86d9-4143-8323-4202171e1014)


### 4. Find the Issuer URI

The **Issuer URI** is crucial for authentication and is derived from the OpenID Configuration URI.

- I navigated to **Applications** in the sidebar and clicked **Applications** again.
- I created a new application, **SIFT**.
- After the application was created, I clicked on the **Settings** tab.
- Scrolled down, I expanded the **Advanced Settings** section and clicked on the **Endpoints** tab.
- From the **Endpoints** tab, I located the **OpenID Configuration URI**. The **Issuer URI** is part of this configuration and serves as the identifier of the authorization server.
- I located the **OpenID Configuration URI**. Copied the URL and visited the url on a new tab this revealed The **Issuer URI** 

**Image Reference**:
![Screenshot 2025-01-02 103820](https://github.com/user-attachments/assets/32d6281a-5014-4c5a-bed2-aee363bc1f91)
![Screenshot 2025-01-02 104129](https://github.com/user-attachments/assets/a62b05b7-b51d-4345-8e9f-8461e673ab45)
![Screenshot 2025-01-02 104306](https://github.com/user-attachments/assets/26753a45-9e77-4a22-a2eb-8ace1769e818)
![Screenshot 2025-01-02 104532](https://github.com/user-attachments/assets/738bdc4c-fc38-4c02-bf3b-4fa7e0e57537)


### 5. Summary

At this stage, I had:

1. Signed up for Auth0.
2. Created an API resource to protect with access tokens.
3. Configured the default audience for my API.
4. Retrieved the Issuer URI.
