# 💼 Venture Investment Database Analysis (SQL)

This project focuses on analyzing a relational database containing information about venture capital funds, startup companies, employees, educational backgrounds, and investment activities. The project is completed using only SQL without any Jupyter Notebook.

> 📌 **Note**: The dataset is not included in this repository due to storage and licensing constraints.
---

## 🧠 Project Objective

To explore and analyze the structure and content of a startup investment database derived from the [Kaggle Startup Investments dataset](https://www.kaggle.com/datasets), and answer business-relevant questions using SQL queries.

The main goals include:
- Understanding how startups and venture capital funds are connected through funding rounds.
- Analyzing acquisition trends, investment behavior, and educational backgrounds of startup employees.
- Extracting insights into successful funding patterns and the life cycle of startups.

---

## 🗃️ Database Schema

The database contains the following tables:

| Table | Description |
|-------|-------------|
| **company** | Details of startup companies: name, category, founding date, status, funding history, etc. |
| **fund** | Information about venture funds: name, country, investments made, and milestones. |
| **people** | Employee data including names, affiliated companies, and user profiles. |
| **education** | Educational background of employees (degree, institution, graduation date). |
| **acquisition** | Acquisition records: buyer company, acquired company, payment terms, and price. |
| **funding_round** | Investment round data: company, date, round type (e.g., series A, angel), amount raised. |
| **investment** | Relationships between funds and startups in investment rounds. |
| **education** | Academic credentials linked to startup employees. |

*Refer to the ER diagram for a visual overview of table relationships.*

![ER Diagram](./9d23a440-e2d3-458b-b293-6f62e809d4cc.png)

---

## 🧩 Key Questions Explored

- Which countries have the most active startup ecosystems?
- What are the most common funding round types and their average raised amounts?
- Which funds have made the most investments?
- What are the top categories for successful acquisitions?
- What academic backgrounds are common among startup employees?
- How many companies were acquired vs. went public (IPO)?

---

## 📂 Files

- `queries.sql` — A set of SQL scripts that include all analysis and queries performed.
- `README.md` — This file with project overview and documentation.
- `ER_diagram.png` — ER diagram for the database.

---

## 🧪 Technologies Used

- PostgreSQL (compatible dialect)
- SQL (joins, subqueries, aggregations, filtering, sorting)
- DB visualization tools (e.g., DBeaver, DataGrip, pgAdmin)

---

## 📌 Notes

- The data is synthetic and anonymized; it is used for educational purposes only.
- All analysis was conducted without using Python or notebooks — this project is purely SQL-based.
- The dataset is not included in this repository due to storage and licensing constraints.

---

