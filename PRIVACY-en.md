# Swiki Privacy Policy

Review draft only — unpublished and not yet effective.  
Draft prepared: 17 November 2026. Effective date: to be set when the published version is approved.

## 1. Who is responsible for Swiki?

Swiki is a Windows application developed by Dr. Ahmed Swelam. Privacy questions and requests: Swelgem@gmail.com. This draft describes desktop version 4.7 and identifies checks required before adopting Swiki-branded Google authorization.

## 2. Data on your computer

Swiki stores the notes, notebooks, tasks, tags, links, properties, and attachments you manage, together with settings, revision history, and local backups you create. The database and attachments are stored in application folders; settings are stored in settings.ini. Depending on your use, these may include file paths, modification times, and information about your work.

The developer does not receive your notebook merely because you run Swiki. Sharing through export, synchronization, email, or other services depends on the feature you use and the destination you choose.

## 3. Google Drive connection and permissions

Connecting Google Drive is optional and uses Google's authorization page in your browser. Swiki does not ask you to enter your Google password inside the application. Google issues access and refresh tokens that enable authorized access until they expire or you revoke them.

The existing 4.7 connection uses drive.file, which is also configured for the new Swiki project. This allows creation and management of files created by the app or made available to it by you, rather than general access to every Drive file. Backup uses this permission to create, read, download, and verify backups, manage staging files, and clean up older versions after your review and confirmation.

Swiki runs rclone locally as a transport helper connecting to Google services. The current release uses rclone's authorization identity; preparing Swiki's identity does not automatically change an existing connection. Reauthorization and access to earlier backups must be tested before migration is approved. Backup does not require Gmail or contacts permissions.

## 4. What is uploaded, and why?

When you choose cloud backup, Swiki prepares an archive containing the notebook database, settings, and attachments included in the backup package, then encrypts it on your computer before uploading it to Google Drive for recovery. Do not assume externally linked files outside the attachment folder are included; check them during restore testing.

The storage provider can still see transport metadata such as backup filenames, sizes, and timestamps, which may reveal when a backup was created. Content encryption does not hide every item of metadata or connection information. Google processes service requests under its policies, including network information needed to provide the service. Backup confirmation can involve downloading the copy more than once to compare hashes.

## 5. Encryption and its limits

Cloud backups use AES-256-GCM encryption with your recovery key. Locally saved Google credentials and the cached recovery key are protected using Windows DPAPI for the current user. Moving to another account or computer may require fresh authorization and your original recovery key.

Note protection is separate from cloud backup encryption. Protected note content and additional notes are encrypted; the local database is not fully encrypted, and titles, tags, and some metadata may remain readable. External attachments are not automatically encrypted; use the encrypted-attachment feature where needed.

Backup creation and restoration can temporarily place unencrypted files in a workspace restricted to your Windows account. Decrypted content also exists in memory during use. Swiki cleans operation files and handles interrupted-operation leftovers at startup, but deletion is not secure erasure or protection against device administrators, malware, or file-recovery tools.

The developer has no service to recover a lost encryption key. You are responsible for keeping an external copy of your recovery key. Passwords copied from credential cards remain in the Windows clipboard until replaced or cleared, and can be affected by Windows clipboard history and synchronization settings.

## 6. Retention, retry, and deletion

Local notebook data remains until you manage or delete it. Moving an item to Swiki's recycle bin is not permanent deletion; copies may remain in revision history, backups, and exports.

If upload fails, encrypted backup files remain in a local retry queue. Retrying may transfer the entire file again. Confirmed copies remain on Drive until you delete them or use reviewed version cleanup. Swiki does not promise automatic deletion of every copy; other installations or exports may have copies, and Drive trash behavior also applies.

You can disable automatic backup in Swiki and revoke access through your Google Account connections at https://myaccount.google.com/connections . Revocation does not delete existing local or Drive backups. Delete those separately if desired and review Google's trash settings. Restoring protected content may require both the backup recovery key and original note passwords.

## 7. Logs, connections, and sharing

Swiki locally records backup stages, times, outcomes, operation identifiers, queue counts, and error categories. The cloud operations log rotates and is designed to exclude authorization tokens, passwords, and note text. Other diagnostic logs may include technical information or paths; review files before sharing them with support.

Checking for or downloading updates contacts the configured update address. Opening links and using optional transfer or synchronization features sends requests to the selected destinations. Local storage does not mean that these requested features make no network connections.

Drive uploads go from your device to Google, without a developer-operated storage relay in the current implementation. If you email support, the developer receives your message and any files you attach. Do not send passwords, recovery keys, or account tokens. Google, email providers, and any future website host process service data under their respective policies.

## 8. Use of Google data

Google data available to Swiki is used to provide user-selected backup, restoration, and backup-management functions. Proposed commitment for approval before publication: Swiki's use and transfer of information received from Google APIs will adhere to the Google API Services User Data Policy, including Limited Use requirements. Such data will not be sold, used for targeted advertising or training general-purpose AI models, or shared for purposes unrelated to the disclosed features.

This proposed commitment requires owner approval and implementation checks before publication. It does not represent approval or certification by Google. No AI feature is enabled within the scope described here.

## 9. Website, changes, and contact

A Swiki website host has not yet been selected, so this draft does not assume a particular website cookie or analytics policy. Actual hosting logs, analytics, and cookie disclosures must be added before publication.

The published policy will be updated when behavior changes. New uses of Google data will be disclosed, with consent requested where required before data is used differently. Saving this draft does not make it effective. Contact: Swelgem@gmail.com.

[Application page](HOME-en.md) · [العربية](PRIVACY-ar.md)
