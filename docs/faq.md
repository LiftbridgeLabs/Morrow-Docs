# Frequently asked questions

## Is Morrow an audiobook server?

No. Morrow is a player that connects to a BookOrbit or Audiobookshelf server you already operate.

## Does Morrow include audiobooks?

No. Morrow does not provide, sell, or host audiobook content.

## Is Morrow open source?

No. Morrow is a commercial, closed-source application. This repository contains public documentation and issue tracking only.

## Which devices are supported?

Morrow is being developed for iPhone and iPad. Exact operating-system requirements will be published before release.

## Can I connect more than one server?

Yes. Servers are managed on the Settings tab, and the Library tab switches between them. When the same audiobook exists on more than one server, Morrow keeps its listening position in sync across them (this can be turned off in Settings).

## Does Morrow work offline?

Two ways:

- **Downloads** — the download button on a book's details page (or the Playing tab) stores the whole book on the device until you remove it.
- **Playback cache** — while a book streams, Morrow can automatically save it on the device so future starts and seeks are instant. The cache has a size limit you choose, removes the least-recently-played books first, and is fully visible in Settings.

By default nothing downloads over cellular; there is an explicit switch in Settings if you want to allow it.

## Where did my ebooks go?

Morrow is an audiobook player, so ebook-only libraries and ebook-only entries are hidden. Books that have both an ebook and audio files appear normally.

## How does the Listening tab decide what's "in progress"?

A book appears after about a minute of real listening. Briefly opening a book doesn't shelve it — and doesn't create a progress record on your server. Swipe a book left to remove it from the list; it returns if you listen to it again.

## What does "Back up servers to iCloud" do?

It stores your server list (including passwords) in your iCloud Keychain — the same protected storage Apple uses for your saved passwords. You won't see a file in iCloud Drive. Another device signed into the same Apple Account can restore the whole setup from Settings, and the backup survives deleting the app.

## Does Morrow support CarPlay?

CarPlay support is built and planned for release; it is awaiting Apple's CarPlay entitlement approval.

## Can I use Morrow outside my home network?

Yes, provided your BookOrbit or Audiobookshelf server is safely reachable from your device. HTTPS through a properly configured reverse proxy is recommended.

## Where do I report a bug?

Use the [bug report form](https://github.com/LiftbridgeLabs/Morrow-Docs/issues/new?template=bug-report.yml).

## Where do I request a feature?

Use the [feature request form](https://github.com/LiftbridgeLabs/Morrow-Docs/issues/new?template=feature-request.yml).
