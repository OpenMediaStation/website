---
title: Setting Up Authentik
weight: 3
draft: false
description: A tutorial on how to use the Authentik identity provider with OpenMediaStation.
---

You can use any identity provider that supports OAuth with your OpenMediaStation (OMS) instance. This guide focuses on the Authentik identity provider, but the same settings can be applied to other providers.

## Creating an Application

To connect Authentik to OMS, we first need to create a public application in Authentik and save the `ClientId` and `ConfigurationURL` for later use in OMS.

To create an application, navigate to the **Applications** tab in the admin interface, as shown in the image below.

![Screenshot of the application menu in Authentik](applications_authentik.png)

In this menu, click the `Create with wizard` button.

![Screenshot of the application configuration menu in Authentik.](application_configuration_authentik.png)

Enter an application name and slug (used in the URL). These values can be set freely.

After clicking **Next**, you will be prompted to choose a provider type. Select `OAuth2/OpenID Provider`.

![Screenshot of the provider configuration screen in Authentik.](provider_configuration_authentik.png)

In the next menu, configure the OAuth2 provider settings. You can choose any name. For `Authorization flow`, select `default-provider-authorization-explicit-consent` and for `ClientType`, choose `Public`.

![Screenshot of the top of the OAuth2 provider configuration in Authentik.](provider_authentik_top.png)

The `Client ID` displayed now should be saved for later use in the OpenMediaStation configuration, as described in [Getting Started](../getting-started/).

![Screenshot of the redirect URIs dialog in Authentik.](redirect_uris.png)

Now, enter two redirect URIs:
- **Mobile apps:** `my.test.app:/oauth2redirect`
- **Desktop:** `http://localhost:8000/redirect.html`

Please enter both URIs, even if you do not plan to use a specific platform.

![Screenshot of the advanced flow settings and advanced protocol settings in Authentik.](advanced_oauth_authentik.png)

Next, set the `Authentication flow` to `default-authentication-flow` and adjust the `Access Token validity` to `hours=5`. *(This setting is required due to a bug in a library we use. It may be reduced in a future release or if you are using a third-party frontend application.)*

![Screenshot of the process of selecting scopes in Authentik.](scopes_authentik.png)

When selecting scopes, be sure to include the `offline_access` scope. After that, click **Next** to complete the application setup.

Finally, copy the `OpenID Configuration URL` of your newly created provider and proceed with the OMS installation.

> If you have not yet set up a device code flow, continue with the next section.

## Ensuring the Device Code Flow Exists

A `Device code flow` must be selected in `System/Brands/{YourBrand}/Default flows`. A default option should be available for selection.

![Screenshot of updating the Device Code Flow in Authentik.](update_brand_authentik.png)

