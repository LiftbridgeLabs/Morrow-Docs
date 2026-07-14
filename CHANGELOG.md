# Release notes

Morrow is currently in active development and has not yet had a public App Store release.

Public release notes will be recorded here once testing builds and production versions begin shipping.

## Unreleased — current development build

- BookOrbit and Audiobookshelf servers, multiple at once, with automatic re-authentication (Audiobookshelf supports API-key sign-in)
- Library browsing with search, sorting, series, and collections; book details page with synopsis, community ratings, metadata, chapters, and track information
- Listening tab: in-progress books combined across all servers, with swipe-to-remove
- Cross-server listening-position sync for books that exist on more than one server
- Full playback suite: background and lock-screen playback, chapters, playback speed, sleep timer (including end-of-chapter), skip controls
- Offline downloads, plus an automatic playback cache with user-set size limit and cellular protection (nothing downloads over cellular unless enabled)
- iCloud backup of the server list via iCloud Keychain, restorable on other devices
- Ebook-only libraries and entries hidden (audiobook-focused)
- Light/dark appearance with matching app icon
- CarPlay: browse Continue Listening and play from the car; Apple entitlement granted and shipping
- Custom request headers per server, with a one-tap Cloudflare Access preset — for servers behind edge protection
- Password re-authentication prompt when a server rejects saved credentials (dismissable)
- Statistics scoped to the library you're browsing, and listening history now included in the iCloud backup

## Earlier

- Initial public documentation repository created.
- BookOrbit and Audiobookshelf support documented.
- Public bug, feature, and support request forms added.
