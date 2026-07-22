# Release notes

Morrow is currently in active development and has not yet had a public App Store release.

Public release notes will be recorded here once testing builds and production versions begin shipping.

## Unreleased — current development build

- BookOrbit and Audiobookshelf servers, multiple at once, with automatic re-authentication (Audiobookshelf supports API-key sign-in)
- Library browsing with search, sorting, series, and collections; book details page with synopsis, community ratings, metadata, chapters, track information, and your current listening position
- Home tab: your in-progress books on the currently selected server, with swipe-to-remove, plus a manual "Up Next" queue you can add books to and reorder — finishing a book automatically starts the next one queued
- Read/finished status shown and editable per book, matching what each server actually supports — all 8 of BookOrbit's statuses (Unread, Want to Read, Reading, On Hold, Re-reading, Read, Skimmed, Abandoned), or Audiobookshelf's 3 (Not Started, In Progress, Finished)
- Your place is kept even when a book is re-imported on the server (for example, when automation upgrades it to a better-quality file): Morrow recognizes the same book and carries your position forward, asking first if it isn't certain
- Full playback suite: background and lock-screen playback, chapters, playback speed, sleep timer (including end-of-chapter), skip controls
- Offline downloads that keep going in the background (and, for single-file books, even if you fully quit the app) — cancel one in progress with a swipe — plus an automatic playback cache with user-set size limit and cellular protection (nothing downloads over cellular unless enabled)
- iCloud backup of the server list via iCloud Keychain, restorable on other devices
- Ebook-only libraries and entries hidden (audiobook-focused)
- Light/dark appearance with matching app icon
- CarPlay: Home (with cover-art shelves matching whatever you've configured on your phone's Home tab), Collections, a full A-Z Library browse, Offline, and Now Playing with chapter/speed/skip controls — switch servers from the car if you connect more than one
- Custom request headers per server, with a one-tap Cloudflare Access preset — for servers behind edge protection
- Password re-authentication prompt when a server rejects saved credentials (dismissable)
- Statistics describe your listening across your devices (combined through your iCloud backup), with each server's own numbers shown separately
- Listening history is included in the iCloud backup, so it survives a reinstall or a new device

## Earlier

- Initial public documentation repository created.
- BookOrbit and Audiobookshelf support documented.
- Public bug, feature, and support request forms added.
