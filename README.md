# Higher Education Enrollment Analysis

## 🎯 Problem
Many higher education institutions are lacking the proper database structure and rely on unstructured and unoptimized queries. This makes it difficult to audit course capacity bottlenecks, monitor student credit progression, and evaluate faculty teaching distribution efficiently[cite: 1, 4].

## 💡 Solution & Technical Architecture
Designed and implemented a relational database schema alongside an analytical query suite built for operational business intelligence. The system transforms raw enrollment logs into actionable administrative metrics using modern, production-grade SQL standards[cite: 1, 4].

* **Database Engine:** PostgreSQL / ANSI SQL Compatible
* **Core Concepts:** DDL Constraints, Composite Primary/Foreign Keys, Performance Indexing, Views, CTEs, Window Functions, Conditional Aggregations[cite: 1, 4]

## 🛠️ Key Analytical Features
* **Window Functions (`DENSE_RANK()`):** Partitioned and ranked student credit loads across the university without collapsing underlying student metadata[cite: 1, 4].
* **Operational Capacity Audit (CTEs + `CASE WHEN`):** Built a multi-stage Common Table Expression calculating real-time section enrollment percentages and classifying sections as *Under Enrolled*, *Near Capacity*, or *At/Over Capacity*[cite: 1, 4].
* **Conditional Demographic Aggregation:** Pivoted faculty age cohorts against salary brackets and teaching loads in a single aggregation pass[cite: 1, 4].
* **Relational Integrity & Refactoring:** Converted implicit joins to explicit `JOIN ... ON` statements and established composite key constraints across course sections.

## 📁 Repository Structure
```text
├── schema.sql         # Database creation, table definitions, and indexes
├── data.sql           # Sample data insertion scripts for testing
├── analytics.sql      # Advanced query suite (CTEs, Window Functions, Aggregations)
└── README.md          # Project documentation
