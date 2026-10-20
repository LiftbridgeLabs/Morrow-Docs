# BookOrbit setup

Morrow can connect to a BookOrbit server using the server address and account credentials you already use.

## Connection checklist

- Confirm BookOrbit opens successfully in Safari on the same device.
- Use the full server address, including `https://` when applicable.
- Confirm the account can sign in through the BookOrbit web interface.
- When using a reverse proxy, verify that it supports normal API traffic and is not limited to a browser-only login page.

## Add BookOrbit to Morrow

1. Open Morrow and go to the **Settings** tab.
2. Choose **Add Server**.
3. Select **BookOrbit**.
4. Enter the server address.
5. Choose how to sign in:
   - **Password**: enter your BookOrbit username and password.
   - **Shared account link**: paste the complete BookOrbit magic link (or just
     its token) when your server provides password-less shared access.
   - **SSO**: sign in with your server's identity provider. See
     [Sign in with SSO](#sign-in-with-sso).
6. Save the connection.

## Sign in with SSO

If your BookOrbit server signs in through an identity provider (OpenID Connect, for example Pocket ID, Authentik, Authelia or Keycloak), Morrow can sign in the same way. Morrow 1.13 and BookOrbit 3.2 or later are required.

Google works for BookOrbit's website, but not for app sign-in. BookOrbit sends every app's sign-in back to the address `bookorbit://oauth2-callback`, and Google only returns to web addresses. This affects all BookOrbit apps, not only Morrow. If a server's only provider is Google, Morrow doesn't offer SSO for it; use a password account or a shared account link instead.

### For the server admin (once)

1. In your sign-in server (for example Pocket ID or Authentik), open the client you use for BookOrbit, or create one, and add `bookorbit://oauth2-callback` to its callback URLs, beside BookOrbit's own web callback (`https://<your server>/oauth2-callback`). In Pocket ID: **OIDC Clients > BookOrbit > Callback URLs**.
2. In BookOrbit, open **Settings > OIDC / SSO** and add the provider with **Add Provider**: its **Issuer URI**, **Client ID** and **Client Secret**. Make sure **Enable provider** is on.
3. Decide how accounts are matched. **Allow local account linking** links a sign-in to an existing BookOrbit account with the same username. **Auto-provision users** creates an account on the first sign-in. With neither, each person links the provider themselves first, in BookOrbit's website under **Settings > Account > Connected Accounts**.

You can keep Google for BookOrbit's website and add a second provider for apps; BookOrbit offers several at once.

### In Morrow

1. Add (or edit) your BookOrbit server and enter its address.
2. Under **Account**, choose **SSO** (or your provider's name, when it is short enough to fit), then **Sign in with** your provider.
3. Sign in on your provider's page. When it closes, the server is saved and connects.

Good to know:

- If your server offers more than one provider, Morrow shows a button for each, and remembers the one you used.
- Your sign-in stays on this device and renews itself. If it ends, Morrow asks you to sign in again with your provider.
- Switching a server you already have from a password to SSO replaces the saved password. To go back, edit the server and enter the password again.
- If the server only allows SSO, the password fields are hidden; a shared account link still works.
- Apple TV and Apple Watch can't sign in to an SSO server yet. Use it on iPhone or iPad.

## Listening stats (BookOrbit 3.2.0 and newer)

Morrow sends each listening session to BookOrbit when you stop listening, so BookOrbit's statistics, streaks, and each book's Reading Log include what you play in Morrow. Sessions show up with the source **iOS app**.

To add listening from before Morrow 1.10.1, open **Settings**, choose your BookOrbit server, and tap **Send Past Listening to BookOrbit** under **Listening History**:

- It sends the sessions Morrow kept on that device, up to the last 20 per book.
- They are added as time listened, without a position, so no book's status changes.
- Each session is counted once, however often you tap.
- If you also played a book under another account or server on the same device, Morrow holds those sessions back and asks before sending them. Older sessions don't record which account they came from, so sending them counts all of them as this account's listening.

## Problems connecting

See [Troubleshooting](troubleshooting.md). When reporting a problem, include the Morrow version, device operating-system version, BookOrbit version, and the exact error text. Remove credentials and private tokens first.
