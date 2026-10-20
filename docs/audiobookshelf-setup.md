# Audiobookshelf setup

Morrow can connect to an Audiobookshelf server using the same address and account you use with the Audiobookshelf web interface.

## Connection checklist

- Confirm Audiobookshelf opens successfully in Safari on the same device.
- Use the full server address, including `https://` when applicable.
- Confirm your Audiobookshelf account can sign in normally.
- If you use a reverse proxy, verify that normal API traffic is allowed.

## Add Audiobookshelf to Morrow

1. Open Morrow and go to the **Settings** tab.
2. Choose **Add Server**.
3. Select **Audiobookshelf**.
4. Enter the server address.
5. Choose how to sign in:
   - **Password**: your Audiobookshelf username and password.
   - **API Key**: generate one in the Audiobookshelf web UI under **Settings → API Keys**. API keys keep working when the account password changes, which makes them the more durable choice.
   - **SSO**: when your server signs in through an identity provider. See below.
6. Save the connection.

## Sign in with SSO

If your Audiobookshelf server uses OpenID Connect sign-in (for example Pocket ID, Authentik, Authelia, Keycloak or Google), Morrow can sign in the same way. Morrow 1.13 or later and Audiobookshelf 2.26.0 or later are required.

### For the server admin (once)

1. In Audiobookshelf, open **Settings > Authentication > OpenID Connect Authentication**.
2. Under **Allowed Mobile Redirect URIs**, add `morrow://oauth`. Keep the existing entries.
3. At your provider, on Audiobookshelf's client, the callback URLs must be the two Audiobookshelf lists under "Authorize these URLs in your OAuth provider". With the default **Subfolder for Redirect URLs** (`/audiobookshelf`) they are:
   - `https://your-server/audiobookshelf/auth/openid/callback`
   - `https://your-server/audiobookshelf/auth/openid/mobile-redirect`
4. After saving, restart Audiobookshelf. Its settings page notes that OpenID changes need a restart.

Switching an existing account to a different provider: Audiobookshelf keeps each account linked to the provider it first signed in with, and refuses the new one with "Unauthorized". In **Settings > Users**, edit the user and choose **Unlink OpenID**, then sign in with the new provider.

### In Morrow

1. Add (or edit) your Audiobookshelf server and enter its address.
2. Under **Account**, choose **SSO**. The button uses your server's own text, for example **Login with Pocket ID**.
3. Sign in on your provider's page. When it closes, the server is saved and connects.

Good to know:

- Your sign-in stays on this device and renews itself. If it ends, Morrow asks you to sign in again with your provider.
- Removing the server from Morrow signs out only this device.
- Apple TV and Apple Watch can't sign in to an SSO server yet. Use it on iPhone or iPad.
- If `morrow://oauth` is missing from the allowed list, Morrow says so and names the setting.

## Problems connecting

See [Troubleshooting](troubleshooting.md). When reporting a problem, include the Morrow version, device operating-system version, Audiobookshelf version, and the exact error text. Remove credentials and private tokens first.
