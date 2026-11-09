# Server compatibility

Morrow works with servers made by other people, and a server update can change what apps are allowed to do. This page lists each server update that changes something in Morrow: what keeps working, what's affected, and which Morrow version adjusts to it.

If something is marked as affected on a server version you're about to install, you can stay on your current version until the Morrow update is out.

## BookOrbit

### BookOrbit 3.7.0

Released November 8, 2026. [BookOrbit's release notes](https://github.com/bookorbit/bookorbit/releases/tag/v3.7.0)

BookOrbit 3.7.0 limits some server features to BookOrbit's own iPhone app. It uses App Attest, an Apple feature that lets a server check a request really comes from a particular app, and BookOrbit accepts that check only from its own app. There's no server setting to allow other apps.

- Listening, progress sync, bookmarks, downloads, your library, search and Continue Listening: work as before.
- Smart scopes, in Collections and in CarPlay: Morrow 1.13.1 for iPhone and iPad loads them on 3.7.0, and a scope with more than 50 books now shows every book. Earlier versions can't load them. The Android fix is on the way.
- BookOrbit's streak in Statistics, the "Streak on this server" and "Longest streak" lines under your server's name: missing on 3.7.0 until Morrow 1.14 for iPhone and iPad and the next Apple TV update. Morrow's own listening stats, counted on your devices, aren't affected.
- Merged books: 3.7.0 can merge duplicate copies of a book into one. Listening on a merged copy keeps working, and its progress saves to the book it was merged into. Morrow doesn't follow a merge everywhere yet: a downloaded copy can show as no longer on your server, and a merged copy drops out of Up Next. A fix is planned.

## Audiobookshelf and Grimmory

Nothing listed yet. Audiobookshelf and Grimmory updates that change something in Morrow will be listed here too.

## Something stopped working after a server update?

Check this page for your server's version first. If it isn't listed, see [Troubleshooting](troubleshooting.md#reporting-a-problem) for how to report it, and include your server type and version.
