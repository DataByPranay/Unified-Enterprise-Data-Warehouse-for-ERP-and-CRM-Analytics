## Naming Conventions

This project follows consistent naming standards across all data warehouse layers.

### General Rules

* Use **snake_case** (lowercase, underscores)
* Use **English** only
* Avoid **SQL reserved words**

---

### Table Naming

**Bronze & Silver**

* Format: `<source>_<entity>`
* Names must match source system tables (no renaming)
* Example: `crm_customer_info`

**Gold**

* Format: `<category>_<entity>`
* Use business-friendly names
* Examples:

  * `dim_customers`
  * `fact_sales`

**Category Prefixes**

* `dim_` → Dimension tables
* `fact_` → Fact tables
* `report_` → Reporting tables

---

### Column Naming

**Surrogate Keys**

* Format: `<entity>_key`
* Example: `customer_key`

**Technical Columns**

* Prefix: `dwh_`
* Example: `dwh_load_date`

---

### Stored Procedures

* Format: `load_<layer>`
* Examples:

  * `load_bronze`
  * `load_silver`


