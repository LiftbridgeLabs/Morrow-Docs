# Booklore setup

Morrow can connect to a Booklore server using the same address and account you use with the Booklore web interface.

## Connection checklist

- Confirm Booklore opens successfully in Safari on the same device.
- Use the full server address, including `https://` when applicable.
- Confirm your Booklore account can sign in normally.
- If you use a reverse proxy, verify that normal API traffic is allowed and is not limited to a browser-only login page.

## Add Booklore to Morrow

1. Open Morrow and go to the **Settings** tab.
2. Choose **Add Server**.
3. Select **Booklore**.
4. Enter the server address.
5. Enter your Booklore username and password.
6. Save the connection.

Booklore currently supports username and password sign-in only; there is no API key or magic link option for this server type.

## Problems connecting

See [Troubleshooting](troubleshooting.md). When reporting a problem, include the Morrow version, device operating-system version, Booklore version, and the exact error text. Remove credentials and private tokens first.
