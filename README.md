# Awesome-Flexible-Billing-Data-Custom-Fields

# Top Flexible Billing Data & Custom Fields Ecosystem

**Curated List of SaaS Platforms & Open-Source GitHub Projects**  
*Focused on Extensible Billing Schemas, Custom Metadata & Self-Hosted Field Engines*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Flexible Billing Data & Custom Fields**. These tools help organizations extend billing and subscription data models with business-specific attributes—covering everything from custom field configuration APIs in commercial billing platforms to open-source billing engines that let you attach arbitrary metadata to any object, and no-code database platforms that serve as flexible billing data layers.

**Examples** include Chargebee Custom Fields, Stripe Metadata, Salesforce Custom Fields, HubSpot Custom Properties, Kill Bill, Flexprice, and Baserow (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted billing with extensible data models, open-source no-code databases, and community-driven field engines—ideal for organizations seeking data sovereignty and avoiding per-custom-field or per-object SaaS upcharges. The open-source landscape is genuinely functional: **Kill Bill** allows tags and custom fields on any object (accounts, invoices, payments) in its open-source edition [citation:16], **Flexprice** supports per-customer plan overrides and flexible pricing models without schema migrations [citation:27], and **Baserow** provides a self-hosted Airtable-like layer with unlimited rows for modeling billing data [citation:2].

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[Chargebee Custom Fields](https://www.chargebee.com/)** | **Configuration API for defining custom fields across 16 entity types** (customer, subscription, plan, addon, invoice, credit_note, item_family, quote, and more). Fields support datatypes including string, long, double, timestamp, email, url, and date; edit UI types include text, textarea, dropdown, radio buttons, checkbox, file, and password. Custom field configs are retrievable via REST API with `entity_type` and `api_name` parameters [citation:19][citation:23]. | Included with Chargebee subscription (verify plan availability) | No standalone free tier for custom fields; bundled with eligible plans |
| **[Stripe Metadata](https://stripe.com/)** | **Key-value pairs attachable to any Stripe object** (customers, subscriptions, invoices, charges, checkout sessions). Useful for storing structured additional information—external IDs, internal codes, or business-specific attributes. Individual keys can be unset by posting an empty value [citation:17][citation:21]. **Trade-off**: metadata is flat string-to-string; no typed fields or validation at the API layer. | Included with Stripe (no extra charge for metadata) | **Free**: metadata on all objects in test mode; production charges apply to transactions |
| **[Salesforce Custom Fields](https://www.salesforce.com/)** | Enterprise CRM with custom fields on standard and custom objects. Supports relationships, validation rules, and page layouts. **Platform Starter: $25/user/month** (10 custom objects); **Platform Plus: $100/user/month** (110 custom objects). | Starter: **$25/user/month**; Plus: **$100/user/month** | No free tier for platform access; free Developer Edition org available |
| **[HubSpot Custom Properties](https://www.hubspot.com/)** | CRM custom properties on contacts, companies, deals, and tickets. Supports multiple field types including text, number, date, dropdown, and calculation properties. | Quote-only (tiered by contacts/features) | **Free CRM**: limited custom properties; paid tiers for more |
| **[Zendesk Custom Fields](https://www.zendesk.com/)** | Ticket and user custom fields with dropdowns, text, numeric, and date types. Used to capture business-specific ticket attributes for routing and reporting. | Included with Zendesk plans | **Free trial** available; no permanent free tier |
| **[Zoho CRM Custom Fields](https://www.zoho.com/crm/)** | Custom fields across CRM modules with various datatypes and validation. | Standard: **$14/user/month** (annual) | **Free edition**: 3 users, limited fields |
| **[ServiceNow Dictionary](https://www.servicenow.com/)** | System dictionary for extending tables with custom fields. Enterprise-grade with audit trails and role-based access. | Quote-only (enterprise contract) | No free tier; demo via sales |
| **[Quickbase Fields](https://www.quickbase.com/)** | Custom fields on Quickbase apps with types including user, file attachment, URL, and formula fields. | Free: **$0** (3 users, 100 credits); Paid: from **$99/month** | **Free**: 1 app, 3 users, 100 credits |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Kill Bill](https://github.com/killbill/killbill)** | [![Stars](https://img.shields.io/github/stars/killbill/killbill?style=social&color=white)](https://github.com/killbill/killbill/stargazers) | **The most mature open-source billing platform with native custom fields and tags on any object.** **Apache-2.0**, open-source edition free forever. **Attach tags and key-value custom fields to accounts, invoices, payments, and other objects**—tag a customer as VIP, flag an account for review, or store business-specific data without schema changes [citation:16]. **Full billing cycle**: catalog, subscriptions, usage billing, invoicing, payments, retries, dunning, tax plugins, and multi-tenancy. **Audit logs** record every change with who/what/when. **Trade-off**: XML catalog configuration and JVM stack; Aviate enterprise adds catalog editor, metering, and wallet features [citation:16]. **Best for B2B SaaS and marketplaces** needing a proven open-source billing engine with extensible data. |
| **[Flexprice](https://github.com/flexprice/flexprice)** | [![Stars](https://img.shields.io/github/stars/flexprice/flexprice?style=social&color=white)](https://github.com/flexprice/flexprice/stargazers) | **Open-source usage-based and hybrid billing with flexible per-customer data.** **Open-source and self-hostable**—no black-box dependency or surprise fees. **Pricing plans can be overridden per customer** and versioned over time without schema updates or migration scripts [citation:27]. **Usage metering** handles millions of events; **credit grants** (prepaid/promotional) with automatic top-ups. **Feature entitlements and limits** per plan or per customer. **Composable**: augments existing payment providers (Stripe, Chargebee) rather than replacing them [citation:27]. **Best for AI and usage-based products** needing flexible billing data models without vendor lock-in. |
| **[Baserow](https://github.com/baserow/baserow)** | [![Stars](https://img.shields.io/github/stars/baserow/baserow?style=social&color=white)](https://github.com/baserow/baserow/stargazers) | **The closest self-hosted Airtable replacement for modeling billing data with custom fields.** **MIT licensed**, self-hosted version runs with **unlimited rows, storage, and databases** [citation:2]. **Multiple field types, custom views, filters, real-time collaboration**, REST API, webhooks, and plugin architecture with custom field types . **Trade-off**: not a billing engine—you model billing data as tables and use the API for integration. Some views (Kanban, calendar) may sit behind paid Premium license even when self-hosted [citation:2]. **Best for teams wanting a flexible, self-hosted data layer** to store and manage billing custom fields before or alongside a billing engine. |
| **[NocoDB](https://github.com/nocodb/nocodb)** | [![Stars](https://img.shields.io/github/stars/nocodb/nocodb?style=social&color=white)](https://github.com/nocodb/nocodb/stargazers) | **Turn any SQL database into a smart spreadsheet—ideal for existing billing schemas.** **MIT license** (Sustainable Use License since v0.301.0—verify commercial use terms) [citation:11]. **Respects existing Postgres/MySQL schemas**—no migration needed. **Virtual Columns** (Lookup, Rollup, Formula) exist only in the NocoDB layer without polluting raw SQL [citation:8]. **Auto-generated REST and GraphQL APIs** with Swagger docs. **Trade-off**: interface layer, not a billing engine; no native automation (webhooks/triggers are limited) [citation:7]. **Best for teams with existing billing databases** wanting a no-code UI for custom field management. |
| **[Grist](https://github.com/gristlabs/grist-core)** | [![Stars](https://img.shields.io/github/stars/gristlabs/grist-core?style=social&color=white)](https://github.com/gristlabs/grist-core/stargazers) | **Spreadsheet-database hybrid with Python formulas and granular access rules.** **Apache-2.0**. **Individuals and organizations under $1M total annual income can request a free activation key** for the hosted version [citation:2]. **Python formulas** replace proprietary spreadsheet languages—real code in cells. **Access rules go down to row, column, and table level**—ideal for mixed-trust billing data where contractors see some fields but not others [citation:2]. **Trade-off**: Python knowledge is a wall for non-technical users; no front-end app builder; automations gated to Business plan [citation:2]. **Best for analytical billing data** needing row-level permissions and code-driven calculations. |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Teable](https://github.com/teableio/teable)** | [![Stars](https://img.shields.io/github/stars/teableio/teable?style=social&color=white)](https://github.com/teableio/teable/stargazers) | **Postgres-native Airtable alternative with real-time collaboration and SQL editor.** **MIT license**. **Built directly on Postgres** for performance with large datasets; **built-in SQL editor** for when the spreadsheet metaphor runs out [citation:2]. **AI fields native**. **Trade-off**: **charges per seat on cloud and self-hosted licenses**—the one thing NocoDB and Baserow fix outright; community has pushed for instance-based pricing without success [citation:2]. **Best for performance-critical billing data** where Postgres-native scale matters more than zero per-seat cost. |
| **[ERPNext](https://github.com/frappe/erpnext)** | [![Stars](https://img.shields.io/github/stars/frappe/erpnext?style=social&color=white)](https://github.com/frappe/erpnext/stargazers) | **Full open-source ERP with built-in custom field support.** **GPL-3.0**, 100% open-source with no feature gates. **Add custom fields in forms without code**; customize behavior with auto-fetch values, role-based hiding, and custom print formats [citation:22]. **Complete accounting**: chart of accounts, journal entries, invoicing, bank reconciliation, multi-currency. **Best for organizations wanting billing custom fields within a complete ERP** rather than a standalone billing engine. |

**Frameworks for building custom systems**: Choose **Kill Bill** for a proven billing engine with native custom fields on every object [citation:16], **Flexprice** for flexible per-customer billing data in usage-based models [citation:27], or **Baserow**/**NocoDB** as a self-hosted data layer for modeling billing custom fields without a full billing engine [citation:2][citation:8].

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Flexible billing data and custom fields often contain business-specific identifiers and financial metadata; enforce access controls and audit logging, especially when custom fields store PII or sensitive commercial terms.
- **Custom field implementations have different storage and query trade-offs.** **JSONB columns** are often preferred over EAV models for custom fields in billing systems—a Salesforce system design reference explicitly chose JSONB with metadata-as-API-contract over EAV because **EAV requires a self-join per field, making three-field reports slow** [citation:10][citation:14]. **Commercial platforms vary**: Chargebee exposes custom field configuration via API with typed fields and edit UI options [citation:19], Stripe metadata is flat key-value strings without validation [citation:17], and Salesforce/HubSpot/Zendesk offer typed custom properties within their respective ecosystems. **Open-source options differ**: Kill Bill's custom fields are native to the billing engine [citation:16], while Baserow/NocoDB are data layers that require integration with a separate billing system [citation:2][citation:8]. **Validate whether you need custom fields *inside* a billing engine (Kill Bill, Flexprice) or a flexible data layer *alongside* one (Baserow, NocoDB)** before committing.

---

**Made for billing engineers, finance operations teams, and developers building extensible billing data models.**  
Let's make flexible billing data and custom fields more open, structured, and cost-predictable.
