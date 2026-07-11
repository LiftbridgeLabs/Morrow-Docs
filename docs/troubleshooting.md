# Troubleshooting

## Morrow cannot connect to the server

1. Open the same server address in Safari on the affected device.
2. Confirm the address includes the correct scheme (`https://` or `http://`) and port.
3. Confirm your username and password still work in the server web interface.
4. Temporarily test from the same local network as the server.
5. If you use a reverse proxy, check its logs and authentication rules.

## The library is empty or incomplete

- Confirm the expected audiobook library is visible to the same server account.
- Morrow hides ebook-only libraries and ebook-only entries by design — it is an audiobook player. Books with both an ebook and audio files appear normally.
- Confirm the server has finished scanning or processing the affected books.
- Restart Morrow and try again.

## The library takes a long time to load

The first load of a large library streams in from the server. After that, Morrow keeps a local snapshot and the grid appears instantly, refreshing in the background. If a library seems permanently stale, switch servers and back, or restart the app.

## Playback does not start, or starts slowly

- Test a second audiobook to determine whether the problem is file-specific.
- Confirm the same item plays through the server's own web interface.
- Very large single-file audiobooks (one big `.m4b`) take longer to start over the network. Morrow's playback cache removes this after the first listen; downloading the book removes it entirely.
- Check available device storage and network connectivity.

## Playback stops when the app is closed or the screen locks

Morrow plays in the background and on the lock screen. If audio stops when leaving the app, make sure you are on the latest build, then restart the device. Note that swiping the app away in the App Switcher (force quit) stops playback — that is standard iOS behavior for all audio apps.

## A book is missing from the Listening tab

- Books appear after 60 seconds of playback; brief opens are ignored on purpose.
- A book you removed with a left swipe returns once you listen to it again.
- BookOrbit has no complete "audio in progress" listing, so a book started only in the BookOrbit web player may not appear until you have played it in Morrow once.

## Progress is not updating

- Confirm the device has a working connection to the server.
- Allow a moment for progress to synchronize after playback stops.
- Cross-server position sync requires the same book (same edition/length) to exist on both servers.

## Downloads or caching won't start

- By default Morrow never downloads over cellular. Enable **Download over cellular** in Settings, or connect to Wi-Fi.
- The automatic playback cache skips books larger than the cache limit set in Settings.

## Reporting a problem

Use the [bug report form](https://github.com/LiftbridgeLabs/Morrow-Docs/issues/new?template=bug-report.yml) and include:

- Morrow version and build
- Device model
- iOS or iPadOS version
- Server type and version
- Whether the problem occurs locally, remotely, or both
- Exact steps to reproduce it
- Relevant error text

Never include passwords, API keys, access tokens, private server addresses, or unredacted logs containing credentials.
