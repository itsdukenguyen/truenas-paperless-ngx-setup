# Best Practices for Paperless-ngx on TrueNAS

## Naming Conventions
- **Tax Returns**: YYYY_Tax_Return (e.g. 2010_Tax_Return)
- Use consistent titles before uploading

## Organization Strategy
- **Storage Paths**: One per major category (Tax Documents, Medical, etc.)
- **Document Types**: Create specific types (Tax Return, Invoice, Receipt, etc.)
- **Tags**: Use year + category (e.g. 2023, Tax Return, Filed)
- **Correspondents**: IRS, Bank Name, Insurance, Doctor, etc.

## Performance & Maintenance
- Use dedicated ZFS datasets with regular snapshots
- Regularly run the **Sanity Checker** in Paperless-ngx
- Export backups using document_exporter
- Keep Paperless-ngx and TrueNAS updated
- Monitor File Tasks for any failed consumptions

## Workflow Tips
- Rename files before dropping them into the consume folder
- Let the auto-matching / machine learning improve over time
- Enable barcode separation for batch scanning
- Use NFS share for the consume directory (more reliable than SMB)
- Consider enabling 2FA on your Paperless-ngx user account
