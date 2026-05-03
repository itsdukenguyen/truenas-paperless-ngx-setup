# TrueNAS SCALE - Paperless-ngx Setup Guide

![TrueNAS](https://img.shields.io/badge/TrueNAS-SCALE-blue?style=for-the-badge)
![Paperless-ngx](https://img.shields.io/badge/Paperless--ngx-v2.20+-green?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

> Comprehensive, reproducible guide for installing **Paperless-ngx** on **TrueNAS SCALE** — written for my future self.

## Overview
Paperless-ngx is a powerful self-hosted document management system with OCR, tagging, auto-matching, and email ingestion.

## Table of Contents
- [Full Setup Guide](./SETUP-GUIDE.md)
- [Best Practices](./docs/best-practices.md)
- [Troubleshooting](./docs/troubleshooting.md)

## Prerequisites
- TrueNAS SCALE (tested on 24.10+)
- Dedicated storage pool with sufficient space
- Basic knowledge of ZFS datasets and permissions

## Quick Start
1. Create recommended ZFS datasets
2. Install Paperless-ngx via TrueNAS Apps
3. Configure Storage Paths & Document Types
4. Set up Gmail IMAP
5. Start ingesting documents