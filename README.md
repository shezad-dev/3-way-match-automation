# 3-Way Match Automation System

**Version:** 1.0  
**Status:** Production Ready  
**Platform:** Python 3, Google Sheets, Gmail SMTP

---

## Overview

Automated reconciliation engine for Purchase Orders, Goods Receipt Notes, and Supplier Invoices. Identifies quantity discrepancies, price variances, and missing documentation. Delivers exception reports via email.

---

## Business Value

- Eliminates manual reconciliation effort
- Reduces payment delays caused by mismatches
- Prevents overpayments and duplicate payments
- Provides audit trail with timestamps
- Enables daily automated reconciliation

---

## System Workflow

1. Extract data from Google Sheets (PO, DeliveryNote, Invoice)
2. Perform 3-way matching logic
3. Flag exceptions (quantity/price/missing documents)
4. Generate email report with all mismatches
5. Save results locally for audit purposes
6. Execute on scheduled intervals

---

## Technical Specifications

| Component | Details |
|-----------|---------|
| Language | Python 3 |
| Data Source | Google Sheets (CSV export) |
| Email Service | Gmail SMTP |
| Runtime | Pydroid 3 (Android) / Any Python 3 environment |
| Storage | Local file system (.txt) |

---

## Configuration

### Sheet Structure (Required Tabs)
- `PO` – Purchase Orders
- `DeliveryNote` – Goods Receipt Notes  
- `Invoice` – Supplier Invoices

### Credentials Setup (config.py)
```python
GMAIL_USER = "sender@domain.com"
GMAIL_PASSWORD = "app_password_16char"
ALERT_EMAIL = "recipient@domain.com"
