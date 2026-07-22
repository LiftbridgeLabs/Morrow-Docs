# Frequently asked questions

## Is Morrow an audiobook server?

No. Morrow is a player that connects to a BookOrbit or Audiobookshelf server you already operate.

## Does Morrow include audiobooks?

No. Morrow does not provide, sell, or host audiobook content.

## Is Morrow open source?

No. Morrow is a commercial, closed-source application. This repository contains public documentation and issue tracking only.

## Which devices are supported?

iPhone and iPad running iOS 18 / iPadOS 18 or later.

## Can I connect more than one server?

Yes. Servers are added on the Settings tab and selected on the Home tab. Each server is completely independent — Morrow doesn't merge, combine, or sync anything between them, even if the same audiobook exists on more than one. Switching servers shows that server's own library, progress, and status exactly as it is there.

## Does Morrow work offline?

Two ways:

- **Downloads** — the download button on a book's details page (or the Playing tab) stores the whole book on the device until you remove it.
- **Playback cache** — while a book streams, Morrow can automatically save it on the device so future starts and seeks are instant. The cache has a size limit you choose, removes the least-recently-played books first, and is fully visible in Settings.

By default nothing downloads over cellular; there is an explicit switch in Settings if you want to allow it.

## Where did my ebooks go?

Morrow is an audiobook player, so ebook-only libraries and ebook-only entries are hidden. Books that have both an ebook and audio files appear normally.

## How does Home's Continue Playing decide what's "in progress"?

A book appears after 60 seconds of playback. Briefly opening a book doesn't shelve it — and doesn't create a progress record on your server. Remove a book from the list with the context menu; it returns if you listen to it again. Continue Playing shows only the currently selected server's in-progress books — Morrow doesn't combine servers together.

## What does "Back up servers to iCloud" do?

It stores your server list (including passwords) in your iCloud Keychain — the same protected storage Apple uses for your saved passwords. You won't see a file in iCloud Drive. Another device signed into the same Apple Account can restore the whole setup from Settings, and the backup survives deleting the app.

## Does Morrow support CarPlay?

Yes. Plug in (or connect wirelessly) and Morrow appears with tabs for Home (your Continue Listening and Up Next queue, plus cover art for whatever shelves you've set up on your phone's Home tab), Collections, a full A-Z Library browse, Offline downloads, and Now Playing — with chapter, speed, and skip controls built in. If you connect more than one server, switch between them right from Home.

## My server sits behind Cloudflare (or another proxy that requires a header)

Open the server in **Settings**, scroll to **Advanced**, and add the headers your proxy expects. There is a one-tap **Cloudflare Access** preset that fills in `CF-Access-Client-Id` and `CF-Access-Client-Secret` for you — paste in the values from your Cloudflare service token. Header values are stored in the iOS Keychain, and Morrow sends them on everything it asks of your server, including audio streaming and downloads.

## Can I use Morrow outside my home network?

Yes, provided your BookOrbit or Audiobookshelf server is safely reachable from your device. HTTPS through a properly configured reverse proxy is recommended.

## Where do I report a bug?

Use the [bug report form](https://github.com/LiftbridgeLabs/Morrow-Docs/issues/new?template=bug-report.yml).

## Where do I request a feature?

Use the [feature request form](https://github.com/LiftbridgeLabs/Morrow-Docs/issues/new?template=feature-request.yml).
