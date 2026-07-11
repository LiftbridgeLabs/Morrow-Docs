# Privacy

Morrow connects your device directly to audiobook servers that you choose and operate. This page describes exactly what the app stores and where, based on the current implementation. It will be finalized as the formal App Store privacy policy before public release.

## The short version

Morrow has no accounts, no analytics, no ads, no tracking, and no third-party SDKs. Liftbridge Labs never receives your data. The only network traffic the app produces is between your device, your own servers, and — if you enable backup — Apple's iCloud Keychain.

## Server credentials

- Server passwords and Audiobookshelf API keys are stored in the iOS Keychain on your device — the same protected storage the system uses for saved passwords.
- Credentials leave the device only to authenticate with the server you configured them for (for example, a sign-in request to your own BookOrbit server). They are never sent anywhere else.

## iCloud backup (optional)

- "Back up servers to iCloud" in Settings is **off by default**.
- When enabled, it stores your server list — server name, address, username, sign-in type, and the password or API key — as a synchronized item in your **iCloud Keychain**, which Apple end-to-end encrypts. No file appears in iCloud Drive, and Liftbridge Labs cannot read it.
- The backup persists if you delete the app (so a reinstall can restore your setup). Turning the toggle off deletes the backup from iCloud for all devices.
- Separately, Morrow syncs a short list of recently played book identifiers (IDs and timestamps only — no titles or audio) through iCloud Keychain so your in-progress shelf matches across your devices.

## Listening data

- Playback positions and progress are stored **on your own servers**, using each server's normal progress features — the same records their web players use.
- Recently played book identifiers are kept on the device (and synced as described above).

## On-device data

- Cover images and library listings are cached on-device so the app opens fast.
- Downloaded books are stored on-device until you remove them.
- The automatic playback cache stores streamed books on-device up to the size limit you set, and is excluded from device backups. You can inspect and clear it in Settings at any time.
- Deleting the app removes all of this local data. Keychain items follow Apple's standard behavior, and the optional iCloud backup remains until you disable it.

## Diagnostics and third parties

- Morrow contains **no** analytics, crash-reporting, or advertising SDKs, and no third-party code that communicates over the network. It is built entirely on Apple's frameworks.
- Apple may collect standard operating-system diagnostics (such as crash logs) according to the privacy settings on your device and your agreement with Apple; that data flow is controlled by iOS, not by Morrow.

## Data retention and deletion

- Liftbridge Labs retains nothing, because it receives nothing.
- Your servers retain the listening progress you send them, under your control.
- On-device data is removed by deleting the app; the iCloud backup is removed by turning the backup toggle off.

## Contact

For privacy questions, email **liftbridgelabs@gmail.com** or open a support issue (never include passwords, tokens, or private URLs in a public issue).
