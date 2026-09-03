# Privacy

Morrow connects your device directly to audiobook servers that you choose and operate. This page describes exactly what the app stores and where, based on the current implementation. It will be finalized as the formal App Store privacy policy before public release.

## The short version

Morrow has no accounts, analytics, ads, tracking, crash-reporting SDKs, or advertising SDKs. Liftbridge Labs never receives your data. Network traffic is between your device and the servers you configure; Apple users can optionally enable an iCloud Keychain backup.

## Server credentials

- On Apple devices, server passwords, proxy-header values, and Audiobookshelf API keys are stored in the iOS Keychain.
- On Android, secrets are encrypted using a key held by Android Keystore; non-secret server settings are stored in app-private DataStore storage.
- Credentials leave the device only to authenticate with the server you configured them for (for example, a sign-in request to your own BookOrbit server). They are never sent anywhere else.

## iCloud backup (optional, Apple only)

- "Back up servers to iCloud" in Settings is **off by default**.
- When enabled, it stores your server list (server name, address, username, sign-in type, and the password or API key) as a synchronized item in your **iCloud Keychain**, which Apple end-to-end encrypts. No file appears in iCloud Drive, and Liftbridge Labs cannot read it.
- The backup persists if you delete the app (so a reinstall can restore your setup). Turning the toggle off deletes the backup from iCloud for all devices.
- Separately, the Apple app syncs a short list of recently played book identifiers (IDs and timestamps only, no titles or audio) and listening history through iCloud Keychain so those records can follow your Apple devices. Android secure backup is currently disabled.

## Sync between your Apple devices (optional)

The same "Sync Servers and Up Next" setting that controls the iCloud backup above also keeps a small amount of state in step between your Apple devices, including Apple TV. iCloud Keychain alone cannot do this, because Apple TV has no access to it. This covers Apple devices only; Android keeps the equivalent records on the device.

- This uses your **private iCloud database (CloudKit)**, in your own iCloud account. Liftbridge Labs has no access to it and receives nothing.
- Everything Morrow stores there is written to **end-to-end encrypted fields**, so only your own devices can read it. That includes your server passwords and API keys, your server addresses and usernames, and every list described below. Apple stores it but cannot read it.
- What is kept there: your server list (as described above), your Up Next list, which books you have swiped off Continue Listening, your short recently played list, your per-book playback speed, your Home shelf arrangement, and your per-book listening history. Book identifiers, titles, authors, and timestamps only. No audio, no account credentials beyond the server sign-in details already covered above.
- Devices check for changes while the app is open, and when it is opened or closed. Nothing is checked while the app is in the background, including during background audio playback.
- Turning the setting off deletes these records from iCloud.

## Listening data

- Playback progress is stored **on your own servers**, using each server's normal progress features, the same records their web players use.
- Morrow also keeps device-local position records so a server-side re-import does not lose your place. Android additionally checkpoints the exact current position about every five seconds for process-death recovery.
- Recently played identifiers and per-book listening-session history are kept on the device. Apple can sync those records as described above; Android keeps them device-local.

## On-device data

- Cover images and library listings are cached on-device so the app opens fast.
- Downloaded books are stored on-device until you remove them.
- The automatic playback cache stores streamed books on-device up to the size limit you set, and is excluded from device backups. You can inspect and clear it in Settings at any time.
- Deleting the Android app removes its local data and Android Keystore secrets. On Apple devices, local files are removed while Keychain items follow Apple's standard behavior; the optional iCloud backup remains until you disable it.

## Diagnostics and third parties

- Morrow contains **no** analytics, crash-reporting, or advertising SDKs, and no third-party service receives app data.
- Apple or Google may collect standard operating-system/store diagnostics according to your device and account settings. Those platform-controlled data flows are not sent to Liftbridge Labs by Morrow.

## Data retention and deletion

- Liftbridge Labs retains nothing, because it receives nothing.
- Your servers retain the listening progress you send them, under your control.
- On-device data is removed by deleting the app, subject to Apple's standard Keychain retention behavior; the optional iCloud backup is removed by turning the backup toggle off.

## Contact

For privacy questions, email **liftbridgelabs@gmail.com** or open a support issue (never include passwords, tokens, or private URLs in a public issue).
