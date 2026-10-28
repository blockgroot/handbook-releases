# Handbook Self-Hosted

Handbook answers your team's questions from your company's own tools: Slack, Google Drive, Notion, Linear and GitHub. This page is where you download Handbook to run on your own server.

## What you need

- A Linux server with Docker and Docker Compose 2.20 or later (about 2 CPUs, 4 GB of memory, 20 GB of disk to start).
- A domain for Handbook (for example `handbook.yourcompany.com`) pointing at the server, with ports 80 and 443 open.
- A Claude API key, a Jina API key, and an SMTP server for sign-in emails.
- **The registry username and token we sent you with your license.** They let your server download Handbook.

## Install

Find the latest version under [Releases](https://github.com/blockgroot/handbook-releases/releases), then on your server (for version 1.0.0):

```sh
curl -LO https://github.com/blockgroot/handbook-releases/releases/download/v1.0.0/handbook-selfhost-1.0.0.zip
unzip handbook-selfhost-1.0.0.zip
cd handbook
./install.sh
```

The installer asks a few questions, sets everything up, starts Handbook and creates your company with you as its admin. Then open `https://<your domain>` and sign in.

## Then

The package's `docs/` folder has the full guides:

| Guide | For |
| --- | --- |
| `INSTALL.md` | Installing, everyday commands, troubleshooting |
| `CHECKLIST.md` | Everything to do after installing: connecting tools, checking answers, inviting your colleagues |
| `CONNECTORS.md` | Creating the Slack, GitHub, Google, Notion and Linear apps Handbook connects through |
| `BACKUP.md` | Backups and restoring |
| `UPGRADE.md` | Moving to a new version |

## New versions

Each version is listed under [Releases](https://github.com/blockgroot/handbook-releases/releases) with its notes. Your Handbook also tells its admins when a new version is out, in **Admin › Updates**, where they can update with one click.

`releases.json` in this repository is the list Handbook reads to know about new versions. It is a plain file; nothing about your company is sent to us when Handbook reads it.
