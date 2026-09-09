# Frequently asked questions

## Is Morrow an audiobook server?

No. Morrow is a player that connects to a BookOrbit, Audiobookshelf, or Grimmory server you already operate.

## Does Morrow include audiobooks?

No. Morrow does not provide, sell, or host audiobook content.

## Is Morrow open source?

No. Morrow is a commercial, closed-source application. This repository contains public documentation and issue tracking only.

## Which devices are supported?

iPhone and iPad running iOS 18 / iPadOS 18 or later, and Android devices running Android 8.0 or later.

## Can I connect more than one server?

The free version connects to one server. Morrow Unlock removes that limit, so you can add several and switch between them from the Home tab.

However many you connect, each server is completely independent. Morrow doesn't merge, combine, or sync anything between them, even if the same audiobook exists on more than one. Switching servers shows that server's own library, progress, and status exactly as it is there.

## What is free, and what does Morrow Unlock add?

The free version is a complete player: playback with chapters, adjustable speed, and a sleep timer; CarPlay or Android Auto, the Home Screen widget, and lock-screen controls; the Up Next queue with auto-advance; one connected server; and up to three downloaded books.

Morrow Unlock is a one-time purchase (with an Individual and a Family option) that adds unlimited downloads, automatically keeping the next queued book downloaded, the accent color themes, and unlimited connected servers with switching between them. There is also an optional tip jar. Nothing is a subscription.

## Does Morrow work offline?

Two ways:

- **Downloads**: the download button on a book's details page (or the Playing tab) stores the whole book on the device until you remove it.
- **Playback cache**: while a book streams, Morrow can automatically save it on the device so future starts and seeks are instant. The cache has a size limit you choose, removes the least-recently-played books first, and is fully visible in Settings.

Once a full-book download is complete, that book plays without a server connection, including in airplane mode. If it finishes downloading while you are already listening, Morrow switches the loaded player to the local copy.

By default nothing downloads over cellular; there is an explicit switch in Settings if you want to allow it.

## Can I see where I started listening?

Yes. Open the Playing screen and choose **History** to see each session's start time, starting and ending book positions, chapter, and actual listening duration. This is useful for finding your place after falling asleep.

On Android, the current listening position is also checkpointed locally every five seconds. If Android force closes Morrow or ends its process for battery optimization, reopening the book restores the newer of the device checkpoint and the position saved on your server.

## Where did my ebooks go?

Morrow is an audiobook player, so ebook-only libraries and ebook-only entries are hidden. Books that have both an ebook and audio files appear normally.

## Does Morrow handle very large libraries?

Yes. Libraries of about 8,000 audiobooks or fewer are loaded once and browsed entirely on the device. Search, sorting, and the A–Z index all work instantly, exactly as they always have.

Above roughly 8,000 books, Morrow switches to loading your library from the server as you go: the Library tab loads more as you scroll instead of all at once, search runs on the server instead of scanning a full local copy, and the A–Z scrubber is hidden (jumping to a letter isn't meaningful over a partial list). Everything you can do stays the same. Only how the data arrives changes, so a library this size doesn't freeze the app or come up blank.

## How does Home's Continue Listening decide what's "in progress"?

A book appears after 60 seconds of playback. Briefly opening a book doesn't shelve it, and doesn't create a progress record on your server. Remove a book from the list with the context menu; it returns if you listen to it again. Continue Listening shows only the currently selected server's in-progress books. Morrow doesn't combine servers together.

On Audiobookshelf, removing a book from Continue Listening is saved to your server, so it stays removed everywhere you sign in, including Audiobookshelf's own web player. On BookOrbit, which has no equivalent server-side option, the removal syncs between your own Apple devices but won't reach an Android device or BookOrbit's own web interface.

## What does "Back up servers to iCloud" do?

This Apple-only option stores your server list (including passwords) in your iCloud Keychain, the same protected storage Apple uses for your saved passwords. You won't see a file in iCloud Drive. Another device signed into the same Apple Account can restore the whole setup from Settings, and the backup survives deleting the app. Android secure backup is not currently enabled.

## What syncs between my devices?

Two different things sync, by two different routes, and it's worth knowing which is which.

**Your place in a book syncs everywhere.** Playback progress is stored on your own server, so an iPhone, iPad, Apple TV, Android device, and your server's own web player all see the same position. Stop on one, pick up on another.

**Everything else syncs within one platform, not between platforms.** Your Up Next queue, the books you swipe off Continue Listening, your recently played list, per-book playback speed, Home shelf arrangement, and listening history sync between your iPhone, iPad, and Apple TV through your private iCloud database. Android keeps its own copies on the device.

So if you use an iPhone and an Android device, you'll keep your place in a book across both, but each will have its own separate Up Next list. Your servers don't offer a queue Morrow could store there instead, so these lists live with the platform rather than with the library.

The Apple-side sync is controlled by the "Sync Servers and Up Next" setting and is off until you turn it on. Everything it stores is end-to-end encrypted, readable only by your own devices.

## Does Morrow support CarPlay or Android Auto?

Yes. CarPlay provides Home, Collections, a full A-Z Library browse, Offline downloads, server switching, and native Now Playing controls. Android Auto/AAOS provides the equivalent Home, Collections, Library, Offline, Up Next, server-switching, and host-owned Now Playing experience.

## Does Morrow have a Home Screen widget?

Yes, on both Apple and Android. Add it like any other widget (long-press the Home Screen, tap **+**, search "Morrow"). The Now Playing widget shows the book you're currently listening to (cover, title, author, and progress), has working play/pause and skip buttons, and taps through to Now Playing in the app.

On Apple it comes in small, medium, and large sizes; the larger sizes also let you jump straight back into a recent book. Apple additionally has a monthly listening-stats widget and a Control Center / Action Button control that resumes your last book.

## Can I choose a different playback speed for each book?

Yes. The Settings playback speed is the default for new books. Changing speed
from the Playing screen saves an override for that book, and marking the book
finished clears its override. When chapter metadata is available, the Playing
scrubber can also switch between the whole-book timeline and the current
chapter.

## Can I limit Genre Spotlight?

Yes. In Settings → Home Shelves → Genre Spotlight Genres, leave **All Genres**
enabled or choose a custom allow-list. Only genres with at least four books
are eligible for that shelf.

## My server sits behind Cloudflare (or another proxy that requires a header)

Open the server in **Settings**, scroll to **Advanced**, and add the headers your proxy expects. There is a one-tap **Cloudflare Access** preset that fills in `CF-Access-Client-Id` and `CF-Access-Client-Secret` for you. Paste in the values from your Cloudflare service token. Header values are stored in protected platform storage (the iOS Keychain or Android Keystore-backed encrypted storage), and Morrow sends them on everything it asks of your server, including audio streaming and downloads.

## Can I use Morrow outside my home network?

Yes, provided your server is safely reachable from your device. HTTPS through a properly configured reverse proxy is recommended.

## Where do I report a bug?

Use the [bug report form](https://github.com/LiftbridgeLabs/Morrow-Docs/issues/new?template=bug-report.yml).

## Where do I request a feature?

Use the [feature request form](https://github.com/LiftbridgeLabs/Morrow-Docs/issues/new?template=feature-request.yml).
