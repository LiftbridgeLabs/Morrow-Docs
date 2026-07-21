# Getting started with Morrow

Morrow connects to an audiobook server you already operate. It does not host or supply audiobook content.

## Before you begin

You will need:

- An iPhone or iPad running iOS 18 / iPadOS 18 or later
- A working BookOrbit or Audiobookshelf server
- The server address you use from your device
- A valid account for that server (or, for Audiobookshelf, an API key)

## The app at a glance

Morrow has five tabs:

- **Home** — choose which server you're using, see what you're currently listening to, a Continue Playing shelf of that server's in-progress books, and configurable shelves like Recently Added and Discover.
- **Library** — browse the selected server's books, authors, and narrators, with search, sorting, and an A–Z index for jumping around a large library.
- **Playing** — cover art and playback controls for the current book, followed by its full details: synopsis, ratings, chapters, file information, and read/finished status.
- **Collections** — the selected server's series and collections (plus Audiobookshelf playlists or BookOrbit smart scopes, whichever it supports).
- **Settings** — servers, playback cache, iCloud backup, and appearance.

There is no login screen: Morrow connects to your servers in the background and re-authenticates automatically.

## Add a server

1. Open Morrow and go to the **Settings** tab.
2. Choose **Add Server**.
3. Select **BookOrbit** or **Audiobookshelf**.
4. Enter the server address exactly as you use it in a browser.
5. Enter your account credentials (Audiobookshelf also accepts an API key).
6. Save. Select it on the **Home** tab and Morrow connects and loads your books.

You can add more than one server and switch between them from the Home tab. Each server is independent — Morrow doesn't merge or sync anything between them, so switching servers shows that server's own library, listening progress, and status exactly as it is on that server.

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
