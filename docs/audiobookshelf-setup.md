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
   - **Password** — your Audiobookshelf username and password.
   - **API Key** — generate one in the Audiobookshelf web UI under **Settings → API Keys**. API keys keep working when the account password changes, which makes them the more durable choice.
6. Save the connection.

## Problems connecting

See [Troubleshooting](troubleshooting.md). When reporting a problem, include the Morrow version, iOS or iPadOS version, Audiobookshelf version, and the exact error text. Remove credentials and private tokens first.
