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
5. Enter your username and password.
6. Save the connection.

Grimmory uses username and password sign-in only. There is no API key or magic link option for this server type. Grimmory servers also have no separate search or pagination endpoint, so Morrow loads the whole audiobook library in one request.

## Problems connecting

See [Troubleshooting](troubleshooting.md). When reporting a problem, include the Morrow version, device operating-system version, server version, and the exact error text. Remove credentials and private tokens first.
