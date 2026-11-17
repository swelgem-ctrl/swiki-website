# Swiki
## Your ideas, connected. Your knowledge, at home.

Review draft — unpublished — 17 November 2026

Swiki is a portable Windows application for organizing notes and building a personal wiki. Capture ideas, organize notebooks, connect topics and paragraphs, and trace knowledge back to its sources. Choose a complete Arabic or English interface.

## A workspace that fits how you work

- Nested notebooks and folders, multiple tabs, and independent editor windows.
- Rich text, tasks, tags, attachments, and templates.
- Search as you type, favourites, pinned notes, quick capture, and clipboard capture.
- Topic pages, aliases, contextual backlinks, and relationship maps.
- Links to individual paragraphs and live views of linked paragraphs.
- Paragraph citations with sources, quotations, and page numbers; text PDF search and optional local OCR, whose accuracy depends on the document and configuration.
- Optional types and properties, dynamic views, and periodic reviews.
- Customizable application and editor toolbars, with editable keyboard shortcuts.

## Local data, optional cloud backup

Swiki stores your notebook locally. Core note-taking features work without a cloud account. Settings are stored in settings.ini within the application folder. Locally saved Google credentials and the cached recovery key can be tied to your Windows account; moving installations may require fresh authorization and the original recovery key.

Optional Google Drive backup encrypts the notebook package before upload and displays the last confirmed upload after checking the remote copy. Restore previous versions using your recovery key. Automatic backup runs while Swiki is running, including in the system tray if the application has not fully exited. It does not guarantee immediate upload of every edit or backup while the application is closed.

Backup provides snapshots for recovery. Notebook synchronization is a separate workflow with change previews and conflict handling. Enabling Drive backup does not automatically enable live synchronization between devices.

## Protection with clear boundaries

Protected notes can be locked or hidden using a master password, privacy profile, or independent password. Protected note content uses AES-256-GCM encryption. The local database is not fully encrypted: titles, tags, and some metadata may remain readable. Externally linked files do not automatically receive a note's protection.

Your cloud backup recovery key is separate from note passwords. Keep it outside your computer; losing it may prevent decryption of your backups. See the [Privacy Policy](PRIVACY-en.md).

## Status and contact

Current release: Swiki 4.7.0 Beta, for limited evaluation. This draft does not announce public downloads or final distribution licensing.

Developer: Dr. Ahmed Swelam  
Support and privacy: Swelgem@gmail.com

[العربية](HOME-ar.md) · [Privacy Policy](PRIVACY-en.md)

Pre-publication editorial note: Swiki-branded Google authorization is being prepared and has not been integrated. Do not display Google approval claims or promise access to old backups through the new identity until tested. Local Markdown review links must be replaced with website URLs before publication.
