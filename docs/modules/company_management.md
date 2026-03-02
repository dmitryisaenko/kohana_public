# Company Management Module

> Multi-tenant company management with employee onboarding, role-based access control, and subscription handling.

## Overview

The Company Management module is the backbone of Kohana's multi-tenant architecture. It handles the entire company lifecycle - from creation through a guided wizard, to employee onboarding, role & permission management, and subscription billing. Every entity in Kohana is scoped to a company, ensuring complete data isolation between tenants.

---

## Features

### Company Creation Wizard

A 4-step guided process:

1. **Basic Info** - Company name, country selection
2. **Detailed Info** - Logo, contact details, financial information, social links
3. **Team Invitations** - Invite employees by email with role pre-assignment
4. **Plan Selection** - Subscription plan, billing period, promo codes

Default roles and country-specific settings are automatically configured on creation.

### Employee Management

- **Email invitations** with 7-day token expiry and role pre-assignment
- **Role assignment** - assign or change roles at any time
- **Individual permissions** - grant or revoke specific permissions per employee
- **Removal workflow** - employee requests to leave, owner approves or rejects
- **Force removal** - owner can immediately remove an employee

### Role-Based Access Control

Custom RBAC with granular permission control:

- **Permission hierarchy** - super admin > company owner > individual grants > role permissions > revocations
- **Role types** - global (system), template (clonable), custom (created by owner)
- **Wildcard matching** - e.g. `orders.*` grants all order-related permissions
- **Module-grouped permissions** - organized by business module for easy management
- **Company-scoped** - roles in one company don't affect another

### Company Settings

- Company name and branding (logo upload)
- Contact details and financial information
- Module-specific configuration (e.g. allowed countries for Contragents)
- Company deletion with password confirmation

### Subscription & Billing

- Trial period with configurable duration
- Plan selection with country-based pricing
- Promo code support and free month offers
- Payment tracking and status management
- Access blocking for expired subscriptions
