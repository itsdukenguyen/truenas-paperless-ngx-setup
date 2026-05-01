# Paperless-ngx on TrueNAS SCALE - Complete Setup Guide

## 1. Prepare ZFS Datasets

Recommended structure:
- 	ank/paperless
- 	ank/paperless/consume
- 	ank/paperless/media

## 2. Install Paperless-ngx App

- Go to **Apps** → Search **Paperless-ngx**
- Map storage:
  - Consumption directory → /mnt/tank/paperless/consume
  - Media directory → /mnt/tank/paperless/media

## 3. Initial Configuration

- Create **Storage Path**: Tax Documents
- Create **Document Type**: Tax Return
- Set up **Correspondent**: IRS
- Configure **Gmail IMAP** for email ingestion

## 4. Document Workflow (Tax Returns)

- Recommended title format: 2010_Tax_Return
- Use consistent tags: Tax Return, 2010, etc.

*(I will expand this section fully once you confirm)*
