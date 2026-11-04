<p align="center">
  <img src="smaller.png" width="160" alt="NK Pusher">
</p>

<h1 align="center">NK Pusher</h1>

<p align="center">
  Desktop app for publishing projects to GitHub:<br>
  commit, push and release with a single button.
</p>

<p align="center">
  <a href="README.md">Русский</a> | <b>English</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-1.0.0-ffe600?style=flat-square" alt="version">
  <img src="https://img.shields.io/badge/platform-Windows-ffe600?style=flat-square" alt="platform">
  <img src="https://img.shields.io/badge/electron-33-ffe600?style=flat-square" alt="electron">
  <img src="https://img.shields.io/badge/license-proprietary-ffe600?style=flat-square" alt="license">
</p>

---

## Features

- Commit and push changes to any of your repositories with a single button
- Repository picker with live search across your GitHub projects
- Automatic `git init` for folders that are not a repository yet
- Commit author of your choice: from git config or your GitHub account
- Release creation: version, type (Release / Pre-release / Draft), description
- Attach a `.exe` file to the release right from the app
- Force push with history protection (`--force-with-lease`)
- Detailed log of all git operations right in the window
- Interface in three languages: Russian, English, Ukrainian
- GitHub authorization via Personal Access Token
- Yellow and black theme with a custom frameless window

## Screenshots

<p align="center">
  <img src="screenshots/publish.png" width="700" alt="Publish">
</p>
<p align="center">
  <img src="screenshots/release.png" width="700" alt="Release creation">
</p>
<p align="center">
  <img src="screenshots/settings.png" width="700" alt="Settings">
</p>
<p align="center">
  <img src="screenshots/about.png" width="700" alt="About">
</p>

The interface is fully translated:

<p align="center">
  <img src="screenshots/settings-en.png" width="700" alt="English interface">
</p>

## Quick start

Requirements: Node.js 18+ and Git.

```bash
npm install
npm start
```

## Building the installer

```bash
npm run dist
```

The ready installer will appear in the `dist` folder.

## GitHub setup

A token is required for creating releases:

1. Open [github.com/settings/tokens](https://github.com/settings/tokens)
2. Create a classic token with the `repo` scope (or a fine-grained token with `Contents: Read and write` access)
3. Paste the token in the app: Settings : GitHub auth

## Tech stack

- Electron 33
- Node.js (git child processes, no third-party runtime npm dependencies)
- GitHub REST API (releases, asset uploads, repository list)

## License

Closed source. Copying, distribution and use without the author's written
permission is prohibited. See [LICENSE](LICENSE) for details.
