# Getting started with Morrow

Morrow connects to an audiobook server you already operate. It does not host or supply audiobook content.

## Before you begin

You will need:

- An iPhone or iPad running a supported iOS or iPadOS version
- A working BookOrbit or Audiobookshelf server
- The server address you use from your device
- A valid account for that server

## Add a library

1. Open Morrow.
2. Choose **Add Server**.
3. Select **BookOrbit** or **Audiobookshelf**.
4. Enter the server address exactly as you use it in a browser.
5. Enter your account credentials.
6. Save the connection and allow Morrow to load your library.

## Server addresses

Use the complete address, including `https://` when your server uses HTTPS. A reverse-proxy address is usually preferable for access outside your home network.

Examples:

```text
https://books.example.com
http://192.168.1.20:13378
```

Do not post private server addresses, access tokens, passwords, or screenshots containing credentials in public GitHub issues.

## Next steps

- [BookOrbit setup](bookorbit-setup.md)
- [Audiobookshelf setup](audiobookshelf-setup.md)
- [Troubleshooting](troubleshooting.md)
