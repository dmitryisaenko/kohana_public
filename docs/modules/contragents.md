# Contragents Module

> Customer and supplier management with multi-step wizard, country-specific configurations, and delivery address tracking.

## Overview

The Contragents module provides comprehensive CRM functionality for managing customers and suppliers. It features a guided creation wizard, flexible contact hierarchies, country-specific legal and banking fields, delivery address management across multiple carriers, and powerful filtering.

---

## Features

### Multi-Step Wizard

A 3-step process for creating and editing contragents:

1. **Basic Info** — Name, type (customer/supplier), entity type (company/individual), country, legal info, banking details, primary contact
2. **Employee Contacts** — Contact persons with phones, emails, social networks, messengers
3. **Delivery Settings** — Delivery addresses across multiple carrier services

Each step is independently editable after creation.

### Country-Specific Configuration

Form fields and validation rules adapt based on the selected country:

| Country | Tax ID | Delivery Services |
|---------|--------|-------------------|
| Ukraine | EDRPOU / RNOKPP | Nova Poshta, Meest, Ukrposhta, Justin |
| USA | EIN | USPS, UPS, FedEx, Amazon Logistics |
| Poland | — | Poczta Polska, InPost, DPD |
| Germany | — | Deutsche Post, DHL, Hermes |

Legal info, banking, and addresses are stored flexibly — adding a new country doesn't require database changes.

### Contact Management

- **Primary contact** — main point of contact
- **Employee contacts** — additional contact persons
- **Multi-channel** — phones, emails, social networks, messengers per contact
- **Messenger linking** — phone numbers can have associated Telegram, Viber, WhatsApp accounts

### Delivery Addresses

Universal delivery types across all carriers:

- **Pickup Point** — carrier warehouse / collection point
- **Parcel Locker** — automated lockers
- **Courier** — door-to-door delivery
- **Post Office** — traditional postal service

### Financial Tracking

- Per-contragent discount percentage and credit limit
- Balance automatically updated from orders
- Payment terms: prepayment, partial, net-21/30/60, cash on delivery
- Currency auto-determined from company country

### Advanced Filtering & Search

- Full-text search across names (multi-word, case-insensitive)
- Filter by type, country, region, city, category, source
- Balance and discount range filters
- Color-coded tag system (7 preset colors)
- Date range filters, alphabetical navigation
- Soft-deleted records management
- Sortable columns

### Permissions

Granular access control:

- Separate permissions for customers and suppliers lists
- Create, view, update, delete, restore permissions
- Financial data visibility control
- Company-scoped — owners always have full access
