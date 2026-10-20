# Grimmory setup

Morrow can connect to a Grimmory server using the same address and account you use with the Grimmory web interface. A compatible legacy Booklore server also works: select the **Grimmory** type for it.

## Connection checklist

- Confirm the server opens successfully in Safari on the same device.
- Use the full server address, including `https://` when applicable.
- Confirm your account can sign in normally.
- If you use a reverse proxy, verify that normal API traffic is allowed and is not limited to a browser-only login page.

## Add Grimmory to Morrow

1. Open Morrow and go to the **Settings** tab.
2. Choose **Add Server**.
3. Select **Grimmory**.
4. Enter the server address.
5. Sign in with your username and password, or with your server's single sign-on (see below).
6. Save the connection.

Grimmory has no API key or magic link option. Grimmory servers also have no separate search or pagination endpoint, so Morrow loads the whole audiobook library list in one request.

## Sign in with SSO

If your Grimmory server signs in through an identity provider (OpenID Connect, for example Pocket ID, Authentik, Authelia or Keycloak), Morrow can sign in the same way. Morrow 1.13 or later is required.

**Google sign-in can't be used.** Grimmory's app sign-in needs a provider that accepts an app address, and Google doesn't. Morrow says so on the server form. Use a Grimmory password account instead.

### For the server admin (once)

1. In Grimmory, open **Settings > OIDC** and set up your provider. Leave **Client Secret** empty for a public client.
2. Under **Allowed Mobile Redirect URIs**, add `morrow://oauth`. Keep the existing entries.
3. At your provider, on Grimmory's client, add `morrow://oauth` as a callback URL, beside Grimmory's own web callback. In Pocket ID: **OIDC Clients > Grimmory > Callback URLs**. Grimmory's client should be **Public** with **PKCE** on.

Grimmory matches a sign-in to an existing account by the claim set in **Username Claim**. If accounts were created with a password, turn on **Link Existing Local Accounts** until each person has signed in once with SSO.

### In Morrow

1. Add (or edit) your Grimmory server and enter its address.
2. Under **Account**, choose your provider (for example **Pocket ID**), then **Sign in with Pocket ID**.
3. Sign in on your provider's page. When it closes, the server is saved and connects.

Good to know:

- Your sign-in stays on this device and renews itself. If it ends, Morrow asks you to sign in again with your provider.
- If the server only allows SSO, the password fields are hidden. Admins can still use **Use a password (admins only)**.
- Removing the server from Morrow signs out only this device.
- Apple TV and Apple Watch can't sign in to an SSO server yet. Use it on iPhone or iPad.
- If something isn't set up, Morrow names the setting to change: for example, when `morrow://oauth` is missing from Grimmory's allowed list.

## Problems connecting

See [Troubleshooting](troubleshooting.md). When reporting a problem, include the Morrow version, device operating-system version, server version, and the exact error text. Remove credentials and private tokens first.
