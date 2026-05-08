---
layout: ../../layouts/GuideLayout.astro
title: WebDAV backup
description: How Aethelgard's encrypted off-site backup works, why it uses an open protocol instead of Google Drive, and how to set it up against your own infrastructure.
slug: webdav-backup
---

Your financial vault is the most sensitive file on your machine. Lose the device or have it fail, and without a backup you lose the ledger. Aethelgard's answer is WebDAV: an open standard for off-site backup, with end-to-end encryption applied locally before anything leaves your device.

The result is the resilience of cloud storage with the privacy of a local-first vault. The provider hosting your backups cannot read them.

## Why WebDAV, not Google Drive or Dropbox

WebDAV is a long-standing, open file-management protocol. We chose it deliberately:

- **No vendor lock-in.** Any WebDAV-compatible host works — Nextcloud, ownCloud, Fastmail, ProtonDrive, Synology, a self-hosted box. If you outgrow one provider, you move the files.
- **No proprietary client.** Aethelgard talks to the server directly. There is no third-party app sitting between your data and your storage.
- **Privacy-first by default.** WebDAV is the protocol; the encryption is ours. The server holds an encrypted blob it cannot decrypt.

## How the encryption works

A WebDAV backup never leaves your device unencrypted.

1. **Client-side AES-256-GCM.** Aethelgard encrypts the backup archive on your machine before transmission, using AES-256 in Galois/Counter Mode for both confidentiality and integrity.
2. **Argon2id key derivation.** The encryption key is derived from a backup password you set, run through Argon2id — the password-hashing standard designed to resist GPU-accelerated brute force.
3. **Zero-knowledge at the server.** The WebDAV host stores ciphertext only. A breach of the host does not expose your ledger.

The trade-off is non-negotiable: lose the backup password and there is no recovery path. Aethelgard cannot recover what it never saw.

## Setting it up

You will need three things from your WebDAV provider: the server URL, a username, and an app-specific password. (Most providers — Nextcloud, Fastmail, ProtonDrive — issue app-specific passwords from a security settings page so the credential can be revoked without changing your account password.)

1. Open the **Vault Settings** panel and switch to the Cloud Sync section.
2. Enter the WebDAV URL, username, and app-specific password.
3. Set the backup password — the one used to encrypt the archive. Store it somewhere durable and offline.
4. Test the connection before relying on it. A successful test confirms the credentials work and the server accepts the archive format.
5. Run a manual encrypted backup to verify end-to-end. The archive will appear on the WebDAV server as a single encrypted file.

## Restoring

In a recovery scenario — new machine, lost device, corrupted vault — the process is straightforward:

1. Install Aethelgard on the new device.
2. Choose **Restore from backup** on the launch screen.
3. Provide the WebDAV credentials to access the remote server.
4. Pick the archive to restore.
5. Enter the backup password to decrypt and mount the vault locally.

The restored vault behaves identically to the original, including the SHA-256 hash chain that Aethelgard builds across every transaction. If the chain ever fails to verify on restore, that is the integrity check working — it means the archive was tampered with in transit or storage, and the right action is to use a different backup.

## Practical advice

- **Run a backup before any consequential change.** Before opening a new tax year, before bulk-importing a custodian export, before applying an Aethelgard upgrade. The cost is a minute; the value if something goes wrong is the entire ledger.
- **Test the restore at least once.** A backup nobody has restored from is not a backup; it is a hope. Restore to a spare machine or a clean profile and verify the books open.
- **Keep the backup password and the vault PIN in different places.** They protect different things; storing them together collapses two separate defences into one.
