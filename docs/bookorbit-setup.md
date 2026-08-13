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
6. Save the connection.

## Problems connecting

See [Troubleshooting](troubleshooting.md). When reporting a problem, include the Morrow version, device operating-system version, BookOrbit version, and the exact error text. Remove credentials and private tokens first.
