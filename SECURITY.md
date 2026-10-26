# Security

## How Music Toolbox protects you

- **Your AI key stays on your Mac.** It's checked with OpenRouter, saved to
  `~/Library/Application Support/Apple Music Toolbox/.env.local` (readable only by your user), never shown again,
  and never included in a build or an update. Builds fail if a key would be packaged.
- **The built-in server only answers the app.** It listens on `127.0.0.1` only, refuses requests addressed to any
  other host name (DNS rebinding) or sent from other websites, and requires a per-launch token that only the app's
  own windows carry.
- **Nothing changes your library without you.** The assistant drafts a plan you approve first; deleting songs from
  your library always asks for confirmation. Removing songs and deleting playlists can be undone.
- **Your library stays local.** The AI model sees song titles, artists and listening stats only while it works on a
  request you made. There's no account, analytics or tracking.

## Supported versions

Security fixes go into the latest release. Test builds (`-test.N`) are for trying things out and don't update
themselves, so move to the latest full release when one is available.

## Reporting a problem

Please **don't** post details of a vulnerability in a public issue. Open an issue in the
[releases repo](https://github.com/kxnerx/apple-music-toolbox-releases/issues) titled **"Security contact request"**
with no details, and we'll get back to you to share them privately.

Never paste your OpenRouter key, Apple credentials or other secrets into an issue. If you did by accident, revoke the
key at [openrouter.ai/settings/keys](https://openrouter.ai/settings/keys) right away.
