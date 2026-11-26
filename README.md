# E-Commerce Data Management System

A relational database for an online store that records customers, products, orders and browsing behaviour, and uses that behaviour to score product recommendations. Built as a team database-design project (Group 14) in MySQL.

## What it covers

- **Schema design.** Eight related tables: customers, products, categories, brands, orders, interactions, interaction types and recommendations.
- **Recommendations from behaviour.** Each interaction type (for example a view or a purchase) carries a weight. A trigger turns every new interaction into a recommendation score for that customer and product.
- **Order and inventory logic.** Stored procedures place orders and add products. Triggers reduce stock when an order is placed and warn when stock runs low.
- **Business analytics.** SQL queries answer questions such as:
  - Who are the top customers by spending and by activity?
  - Which products sell best, overall and within each category?
  - At what hour are customers most active?
  - Which products are low on stock?
  - Which brands bring in the most revenue?
  - How does revenue split by gender and category?

## Data

Sample data, all fictional:

| Table | Rows |
| --- | --- |
| Customer | 100 |
| Products | 27 |
| Category | 6 |
| Brands | 10 |
| Orders | 100 |
| Interaction | 530 |
| Interaction_Type | 5 |
| Recommendation | 530 |

## Files

| File | Contents |
| --- | --- |
| `*.csv` | Sample data for each table |
| `insert-scripts-all-tables.sql` | `orders` table definition and its sample rows |
| `P1.sql` | Order procedure with the low-stock check |
| `P2.sql` | `orders` table and inserts (phase 2 version) |
| `P3.sql` | Analysis queries (phase 3 version) |
| `Functions.sql`, `Stored procedures.sql`, `Triggers.sql` | Order placement, product management and recommendation logic |
| `SQL Queries_Final.sql`, `Sql Queries.sql` | Analysis queries (final and earlier versions) |
| `Project_Report_Final.pdf` | Full project report |
| `Final_PPT.pptx` | Presentation slides |

## Run it

1. Create a database in MySQL 8: `CREATE DATABASE ecommerce; USE ecommerce;`
2. Import each CSV file as a table with the same name, for example with MySQL Workbench's Table Data Import Wizard. (`insert-scripts-all-tables.sql` can create and fill `orders` instead.)
3. Run `P1.sql`, `Stored procedures.sql` and `Triggers.sql` to add the procedures and triggers. `Functions.sql` documents the design but uses pseudo-code (for example `INPUT()`), so it will not run as is.
4. Run the queries in `SQL Queries_Final.sql`.

## Tools

MySQL, SQL (DDL, DML, functions, stored procedures, triggers), relational modelling.

## License

GPL-3.0. See [LICENSE](LICENSE).
