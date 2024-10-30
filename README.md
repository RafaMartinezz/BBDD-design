# Database Design and Normalization Practice Project

This project focuses on practicing **database design, modeling, and normalization** techniques. It includes conceptual, logical, and relational model design activities for three different case studies, covering entities, relationships, and normalization steps up to Boyce-Codd Normal Form (BCNF). This project is ideal for developing foundational skills in database theory and practical SQL design.

## Table of Contents

- [Project Overview](#project-overview)
- [Learning Goals](#learning-goals)
- [Project Structure](#project-structure)
- [Case Studies](#case-studies)
- [Normalization Process](#normalization-process)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

This educational project comprises three separate database design scenarios, each requiring a different relational database model. Each case study is divided into:
- **Conceptual Design**: Identifying and defining key entities and relationships.
- **Logical Design**: Structuring tables, keys, and constraints in a relational model.
- **Normalization**: Ensuring that each model achieves Boyce-Codd Normal Form (BCNF).

> **Note**: This project is intended for training purposes only and does not represent a production database model.

## Learning Goals

This project is designed to help learners practice the following:

1. Identifying and defining entities, relationships, and attributes in a database.
2. Applying normalization processes (1NF, 2NF, 3NF, BCNF) to ensure data integrity and efficiency.
3. Constructing Entity-Relationship Diagrams (ERDs) and defining relationships between entities.
4. Creating structured relational database models with primary keys, foreign keys, and constraints.

## Project Structure

The project includes the following case studies:

1. **Banking System**: Includes tables for banks, branches, employees, and security personnel with many-to-many relationships and association tables for contracts.
2. **Youth Protection System**: Manages information on minors, families, housing, legal cases, and judicial entities.
3. **Project Management System**: Covers clients, projects, project phases, and employees, with additional client entity considerations.

Each case study includes details on:
- **Entities**: Key data entities required to meet the project requirements.
- **Relationships**: Connections between entities and any derived associative entities (e.g., for many-to-many relationships).
- **Logical Tables**: Relational tables and attributes needed to model the database.
- **Normalization**: Steps taken to achieve BCNF, ensuring each model follows database best practices.

## Case Studies

### 1. Banking System

- **Entities**: BANK, BRANCH, SECURITY GUARD, ROBBER, GANG, JUDGE.
- **Derived Tables**: Additional tables are created to handle many-to-many relationships, such as `CONTRACTS_TO_SECURITY_GUARDS` (for branch-to-security guard relationships) and `BRANCH_ROBBER`.
- **Normalization**: Attributes are atomic and all tables satisfy BCNF requirements.

### 2. Youth Protection System

- **Entities**: MINOR, FAMILY, HOUSING, POPULATION, PROVINCE, CASE FILE, CRIME, COURT, LAWYER.
- **Derived Tables**: The many-to-many relationship between minors and families is represented by the `ASSIGNMENTS` table, while crimes and courts are connected through the `TRIALS` table.
- **Normalization**: The model achieves BCNF with all attributes depending functionally on primary keys.

### 3. Project Management System

- **Entities**: PROJECT, CLIENT, PHASES, EMPLOYEE.
- **Additional Considerations**: Added client details for completeness; debated relationship structure for project hiring details, but assigned start and end dates directly to the project entity.
- **Normalization**: Ensures BCNF compliance by verifying atomic attributes, primary key dependencies, and eliminating transitive dependencies.

## Normalization Process

Each case study includes a **step-by-step normalization process** up to Boyce-Codd Normal Form:

1. **1NF**: Ensures all attributes are atomic (indivisible values).
2. **2NF**: Removes partial dependencies for tables with composite keys.
3. **3NF**: Eliminates transitive dependencies, ensuring each attribute depends solely on the primary key.
4. **BCNF**: Confirms that every non-key attribute is a candidate key, achieving the highest level of normalization.

Este `README.md` está listo para ser copiado y pegado como un solo bloque.
