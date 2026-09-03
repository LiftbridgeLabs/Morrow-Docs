# Release notes

Morrow is currently in active development and has not yet had a public App Store release.

Public release notes will be recorded here once testing builds and production versions begin shipping.

## Unreleased: current development build

- BookOrbit and Audiobookshelf servers, multiple at once, with automatic re-authentication (Audiobookshelf supports API-key sign-in; BookOrbit supports magic-link sign-in for password-less "Shared account" servers). On iPhone and iPad, Booklore is also supported as a server type (username and password sign-in)
- Library browsing with search, sorting, series, and collections; book details page with synopsis, community ratings, metadata, chapters, track information, and your current listening position
- Home tab: your in-progress books on the currently selected server, with swipe-to-remove, plus a manual "Up Next" queue you can add books to and reorder. Finishing a book automatically starts the next one queued; Morrow Unlock adds an optional setting to automatically keep the next queued book downloaded before you get to it
- A Home Screen widget shows the book you're currently listening to (cover, title, author, and progress) and taps straight into Now Playing on Apple and Android
- Read/finished status shown and editable per book, matching what each server actually supports: all 8 of BookOrbit's statuses (Unread, Want to Read, Reading, On Hold, Re-reading, Read, Skimmed, Abandoned), or Audiobookshelf's 3 (Not Started, In Progress, Finished). Each status has its own color, shown right in the picker
- Your place is kept even when a book is re-imported on the server (for example, when automation upgrades it to a better-quality file): Morrow recognizes the same book and carries your position forward, asking first if it isn't certain
- Full playback suite: background and lock-screen playback, chapters, continuously adjustable playback speed from 0.50x to 2.50x in 0.05x steps, sleep timer (including end-of-chapter), and skip controls you can set to whatever amount you prefer. Playback speed has a default plus per-book overrides, and the scrubber can switch between the whole book and the current chapter when chapter metadata is available. The on-screen scrubber spans the whole book by default, with an option to show time remaining and/or your progress as a percentage
- Offline downloads that keep going in the background (on Apple, a single-file download can even survive app termination), cancel one in progress with a swipe, plus an automatic playback cache with user-set size limit and cellular protection (nothing downloads over cellular unless enabled). A book that finishes downloading while already playing switches to its local copy, so it keeps playing in airplane mode. Progress made while listening offline is queued and pushed to your server the instant you're back online, so switching devices afterward picks up from where you actually left off
- iCloud backup of the server list via iCloud Keychain, restorable on other devices
- Sync between your Apple devices, including Apple TV: your Up Next list, the books you have swiped off Continue Listening, your recently played list, per-book playback speed, Home shelf arrangement, and listening history all follow you, so a change made on one device shows up on the others while they are open. Uses your own private iCloud database, everything end-to-end encrypted so only your devices can read it, and is covered by the same "Sync Servers and Up Next" setting as the server backup. Your place in a book is separate: that lives on your own server, so it reaches Android and your server's web player too
- Your place in a book is restored instantly from the device instead of waiting on a server request, so a downloaded book opens straight to where you were even on a bad connection. Positions that go missing on one device now repair themselves from the other rather than staying lost
- Continue Listening, Up Next, and playback speed keep up while an app sits open, instead of only refreshing when you reopen it
- Removing a book from Continue Listening now clears that record once you listen to the book again, rather than leaving it stored indefinitely
- CarPlay shows one set of skip buttons instead of two, and they follow the skip amounts you chose rather than a fixed 15 and 30 seconds
- CarPlay no longer briefly shows another server's books when you start the car
- The Chapter and Book scrubber toggle keeps working on books loaded over a weak connection
- Ebook-only libraries and entries hidden (audiobook-focused)
- Light/dark appearance with matching app icon
- CarPlay: Home (with cover-art shelves matching whatever you've configured on your phone's Home tab), Collections, a full A-Z Library browse, Offline, and Now Playing with chapter/speed/skip controls. Switch servers from the car if you connect more than one
- Custom request headers per server, with a one-tap Cloudflare Access preset, for servers behind edge protection
- Password re-authentication prompt when a server rejects saved credentials (dismissable)
- Statistics describe your listening across your Apple devices (combined through your iCloud backup), with each server's own numbers shown separately
- Per-book listening-session history records when each session began, its start and end positions, and how long you actually listened. On Apple devices, listening history is included in the iCloud backup so it survives a reinstall or a new device
- Android keeps a crash-safe listening-position checkpoint on the device every five seconds and reconciles it with the server when reopening a book, preventing a force close or battery optimization from resetting your place
- Genre Spotlight can be limited to a custom allow-list of eligible genres, while retaining an All Genres default
- Android orders progress saves so a delayed older request cannot overwrite a newer listening position, and caches each server's library list for faster Android Auto startup on weak connections
- When a server does not provide chapters, Morrow can recover common chapter marks embedded in M4B/M4A audio files
- Six accent themes (Bronze, Ink, Forest, Plum, Rust, and Slate) provide coordinated light and dark appearances; all are available during beta testing
- Android clearly distinguishes automatic playback caching from Keep Offline downloads and can promote the same transfer without downloading the book twice
- Android uses consistent cover sizing across Home, Library, and Collections, with a larger phone grid and an alphabet index that no longer obscures the last book
- Playing presents Chapters, Tracks, and History directly beneath the current book details; genres now appear before the synopsis, and an extra empty band above the bottom tabs has been removed
- Android's light and dark launcher icons now preserve the complete M and its surrounding border instead of appearing zoomed or clipped by adaptive launcher masks
- Switching from one book directly to another no longer risks saving the wrong position if playback is interrupted mid-switch, protecting real listening progress
- Continue Listening keeps showing your in-progress books through a spotty connection instead of going blank on a failed refresh, on both the phone and CarPlay
- Chapter numbers on the lock screen and in CarPlay now stay in sync the instant you jump to a new chapter, including when that chapter is in a different audio file
- Removing a book from Continue Listening on one Apple device now carries over to your other Apple devices instead of staying local to the one you removed it on
- Android now supports removing books from Continue Listening too; Audiobookshelf stores the choice on the server so it is shared with Apple and the Audiobookshelf web app, while BookOrbit keeps it on the Android device because that server has no matching field
- Android protects listening progress throughout a book switch and will not fall back to an old local position when a live server progress request merely failed
- Android Home, Library, and Android Auto retain their last confirmed content through temporary refresh failures, and changing the active server immediately refreshes the connected Android Auto browse tree
- Android's Recent Series and Newest Authors shelves now use full-library date-added history instead of echoing Recently Added; Library also adds Date Added ordering, reversible sort direction, downloaded-only filtering, and provider-native read-status filters
- Android records persistent playback-load and download-failure diagnostics so a device-only failure can be investigated after the fact

## Earlier

- Initial public documentation repository created.
- BookOrbit and Audiobookshelf support documented.
- Public bug, feature, and support request forms added.
