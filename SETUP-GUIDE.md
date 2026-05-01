# TrueNAS Scale - Paperless-ngx Detailed Setup Guide

This guide covers my full installation and configuration of **Paperless-ngx** on TrueNAS Scale.

## 1. ZFS Dataset Structure

Created a parent dataset `DataPool/apps/paperless-ngx` with the following child datasets:

- `consume`
- `data`
- `media`
- `postgres-data`
- `trash`

**Screenshots:**
- [Dataset Details](./datasets/01-paperlessngx-dataset-structure.png)
- [Child Datasets](./datasets/03-paperlessngx-child-datasets.png)

## 2. Storage Configuration during App Installation

All volumes were configured as **Host Path** (not ixVolume):

**Screenshots:**
- [Data Storage](./storage-config/data-storage.png)
- [Media Storage](./storage-config/media-storage.png)
- [Consume Storage](./storage-config/consume-storage.png)
- [Trash Storage](./storage-config/trash-storage.png)
- [Postgres Data Storage](./storage-config/postgres-data-storage.png)

**Important:** Do **not** enable ACL unless you have permission problems.

## 3. Configuration Inside Paperless-ngx Web UI

### Storage Paths
**Screenshot:** [Storage Paths List](./paperless-ui/04-storage-paths-list.png)

### Document Types
**Screenshot:** [Document Types List](./paperless-ui/05-document-types-list.png)

I created "Tax Return" among many others.

### Gmail Mail Account
**Screenshot:** [Gmail Configuration](./paperless-ui/06-mail-account.png)

**Settings:**
- Name: `Gmail`
- Username: `duke.h.nguyen@gmail.com`
- IMAP Server: `imap.gmail.com`
- IMAP Port: `993`
- IMAP Security: `SSL`
- Password: **Gmail App Password** (recommended)

### Dashboard Overview
**Screenshot:** [Dashboard](./paperless-ui/07-dashboard.png)

## 4. Tax Returns Workflow

- File naming: `Tax_Return_2010.pdf`, `Tax_Return_2011.pdf`, ...
- Document Type: `Tax Return`
- Correspondent: `IRS`
- Tags: `Tax Return`, year tags, etc.

Drop files into the **Consume** folder for automatic processing.

## 5. Lessons Learned

- Separate child datasets give better control for snapshots and backups.
- Use **Host Path** for all storage.
- Gmail needs an App Password.
- Start with one category (like Tax Returns) before scaling up.

Last updated: April 2026
