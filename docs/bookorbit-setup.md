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

## Listening stats (BookOrbit 3.2.0 and newer)

Morrow sends each listening session to BookOrbit when you stop listening, so BookOrbit's statistics, streaks, and each book's Reading Log include what you play in Morrow. Sessions show up with the source **iOS app**.

To add listening from before Morrow 1.10.1, open **Settings**, choose your BookOrbit server, and tap **Send Past Listening to BookOrbit** under **Listening History**:

- It sends the sessions Morrow kept on that device, up to the last 20 per book.
- They are added as time listened, without a position, so no book's status changes.
- Each session is counted once, however often you tap.
- If you also played a book under another account or server on the same device, Morrow holds those sessions back and asks before sending them. Older sessions don't record which account they came from, so sending them counts all of them as this account's listening.

## Problems connecting

See [Troubleshooting](troubleshooting.md). When reporting a problem, include the Morrow version, device operating-system version, BookOrbit version, and the exact error text. Remove credentials and private tokens first.
