# Paperless-ngx on TrueNAS SCALE - Complete Setup Guide

## 1. Create ZFS Datasets

**Recommended Structure** (under your main pool, e.g. `DataPool`):

- `DataPool/apps/paperless-ngx` ← Parent
- `DataPool/apps/paperless-ngx/consume`
- `DataPool/apps/paperless-ngx/media`
- `DataPool/apps/paperless-ngx/data`
- `DataPool/apps/paperless-ngx/postgres-data`
- `DataPool/apps/paperless-ngx/trash`

**Screenshots:**
- ![Dataset Structure](screenshots/01-paperlessngx-dataset-structure.png)
- ![Child Datasets](screenshots/03-paperlessngx-child-datasets.png)

**Tip**: Create datasets with `compression=lz4` and enable snapshots.

## 2. Install Paperless-ngx App

1. Go to **Apps** → Available Applications → Search **Paperless-ngx**
2. Click **Install**

### Storage Configuration (Critical)

Map each volume exactly as shown:

- **Data Storage** → `/mnt/DataPool/apps/paperless-ngx/data`
- **Media Storage** → `/mnt/DataPool/apps/paperless-ngx/media`
- **Consume Storage** → `/mnt/DataPool/apps/paperless-ngx/consume`
- **Trash Storage** → `/mnt/DataPool/apps/paperless-ngx/trash`
- **Postgres Data** → `/mnt/DataPool/apps/paperless-ngx/postgres-data`

**Screenshots:**
- [Data Storage](screenshots/02-paperlessngx-storage-config-01.png)
- [Media Storage](screenshots/02-paperlessngx-storage-config-02.png)
- [Consume Storage](screenshots/02-paperlessngx-storage-config-03.png)
- [Trash Storage](screenshots/02-paperlessngx-storage-config-04.png)
- [Postgres Storage](screenshots/02-paperlessngx-storage-config-05.png)

## 3. Post-Install Configuration

### Storage Paths
**Manage → Storage Paths → Create**

Example: Name = `Tax Documents`

**Screenshot:** ![Storage Paths](screenshots/04-paperlessngx-storage-path.png)

### Document Types
**Manage → Document Types → Create**

Example: Name = `Tax Return`

**Screenshot:** ![Document Types](screenshots/05-paperlessngx-document-type.png)

### Gmail Integration
**Manage → Mail → Add Account**

- Name: `Gmail`
- Username: `your.email@gmail.com`
- IMAP Server: `imap.gmail.com`
- Port: `993`
- Security: `SSL`
- Use **App Password**

**Screenshot:** ![Gmail Setup](screenshots/06-paperlessngx-mail-account.png)

## 4. Final Dashboard
![Dashboard](screenshots/07-paperlessngx-dashboard.png)

## 5. Tax Return Workflow (2010–Present)

See [Best Practices](./docs/best-practices.md) for detailed naming and organization strategy.