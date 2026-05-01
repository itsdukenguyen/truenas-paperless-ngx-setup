# Paperless-ngx on TrueNAS SCALE - Complete Setup Guide

## 1. Create ZFS Datasets (Recommended Structure)

Create a parent dataset and the following child datasets:

- DataPool/apps/paperless-ngx (parent)
- DataPool/apps/paperless-ngx/consume
- DataPool/apps/paperless-ngx/media
- DataPool/apps/paperless-ngx/data
- DataPool/apps/paperless-ngx/postgres-data
- DataPool/apps/paperless-ngx/trash

**Screenshot:**  
![Paperless-ngx Dataset Structure](screenshots/01-paperlessngx-dataset-structure.png)

**Screenshot:**  
![Child Datasets](screenshots/03-paperlessngx-child-datasets.png)

## 2. Install Paperless-ngx App

Go to **Apps** → **Paperless-ngx** → Install.

### Storage Configuration

Configure each storage volume as shown:

- **Data Storage**: /mnt/DataPool/apps/paperless-ngx/data
- **Media Storage**: /mnt/DataPool/apps/paperless-ngx/media
- **Consume Storage**: /mnt/DataPool/apps/paperless-ngx/consume
- **Trash Storage**: /mnt/DataPool/apps/paperless-ngx/trash
- **Postgres Data**: /mnt/DataPool/apps/paperless-ngx/postgres-data

**Screenshots:**

![Data Storage](screenshots/02-paperlessngx-storage-config-01.png)  
![Media Storage](screenshots/02-paperlessngx-storage-config-02.png)  
![Consume Storage](screenshots/02-paperlessngx-storage-config-03.png)  
![Trash Storage](screenshots/02-paperlessngx-storage-config-04.png)  
![Postgres Storage](screenshots/02-paperlessngx-storage-config-05.png)

## 3. Initial Configuration in Paperless-ngx

### Create Storage Paths
Go to **Manage** → **Storage Paths** → Create

**Screenshot:**  
![Storage Paths List](screenshots/04-paperlessngx-storage-path.png)

### Create Document Types
Go to **Manage** → **Document Types** → Create

**Screenshot:**  
![Document Types](screenshots/05-paperlessngx-document-type.png)

### Configure Gmail for Email Ingestion
Go to **Manage** → **Mail** → Add Account

**Screenshot:**  
![Gmail IMAP Setup](screenshots/06-paperlessngx-mail-account.png)

**Settings used:**
- IMAP Server: imap.gmail.com
- IMAP Port: 993
- IMAP Security: SSL

## 4. Dashboard After Setup

**Screenshot:**  
![Paperless-ngx Dashboard](screenshots/07-paperlessngx-dashboard.png)

## 5. First Document Workflow (Tax Returns)

See detailed workflow in the next sections.
