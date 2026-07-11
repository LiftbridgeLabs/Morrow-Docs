# Getting started with Morrow

Morrow connects to an audiobook server you already operate. It does not host or supply audiobook content.

## Before you begin

You will need:

- An iPhone or iPad running a supported iOS or iPadOS version
- A working BookOrbit or Audiobookshelf server
- The server address you use from your device
- A valid account for that server (or, for Audiobookshelf, an API key)

## The app at a glance

Morrow has four tabs:

- **Library** — browse the active server's books, series, and collections, with search and sorting. Tapping a book opens its details page (synopsis, ratings, chapters, and file information) with a Play button.
- **Listening** — every audiobook you have in progress, combined across all of your configured servers.
- **Playing** — cover art and playback controls for the current book. On launch, Morrow loads your most recent book here, paused at the synced position.
- **Settings** — servers, playback cache, iCloud backup, and appearance.

There is no login screen: Morrow connects to your servers in the background and re-authenticates automatically.

## Add a server

1. Open Morrow and go to the **Settings** tab.
2. Choose **Add Server**.
3. Select **BookOrbit** or **Audiobookshelf**.
4. Enter the server address exactly as you use it in a browser.
5. Enter your account credentials (Audiobookshelf also accepts an API key).
6. Save. The Library tab connects and loads your books.

You can add more than one server and switch between them from the Library tab. Listening progress for the same book is kept in sync across servers automatically.

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
- [Frequently asked questions](faq.md)
- [Troubleshooting](troubleshooting.md)
