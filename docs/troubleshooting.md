# Troubleshooting

## Morrow cannot connect to the server

1. Open the same server address in Safari on the affected device.
2. Confirm the address includes the correct scheme (`https://` or `http://`) and port.
3. Confirm your username and password still work in the server web interface.
4. Temporarily test from the same local network as the server.
5. If you use a reverse proxy, check its logs and authentication rules.

## The library is empty or incomplete

- Confirm the expected audiobook library is visible to the same server account.
- Refresh the library in Morrow.
- Confirm the server has finished scanning or processing the affected books.
- Restart Morrow and try again.

## Playback does not start

- Test a second audiobook to determine whether the problem is file-specific.
- Confirm the same item plays through the server's own web interface.
- Check available device storage and network connectivity.
- Record the exact error message before retrying.

## Progress is not updating

- Confirm the device has a working connection to the server.
- Allow a moment for progress to synchronize after playback stops.
- Avoid signing into the same server account with conflicting playback positions during testing.

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
