# 🗓️ Day 1: Database Setup & Schema Design

## 🎯 Problem Statement
Before Synexus can onboard a single member or host a technical event, we need a secure environment to store our data. Today, we initialize our database and create our very first tables using Data Definition Language (DDL). We must carefully choose our data types to ensure we aren't wasting memory, while strictly ensuring our records have unique identifiers.

## 🛠️ Tech Stack & Focus Areas
* **Tool:** MySQL Workbench
* **Core Concepts:** `CREATE DATABASE`, `CREATE TABLE`, Data Types (`INT`, `VARCHAR`, `TIMESTAMP`, `BOOLEAN`), `PRIMARY KEY`.
* **Goal:** Create the `synexus_db` database and establish the core `members` and `events` tables.

## 📝 Task Requirements

**Step 1: The Database**
Write a query to create a new database named `synexus_db`. 
*Hint: Use `IF NOT EXISTS` to prevent errors if you run the script twice.* 
Make sure to tell MySQL to `USE` this database for the remaining queries.

**Step 2: The Members Table**
Create a `members` table with the following columns:
* `member_id`: An integer that auto-increments and serves as the Primary Key.
* `first_name`: A variable character string (max 50).
* `last_name`: A variable character string (max 50).
* `email`: A variable character string (max 100) that MUST be unique.
* `designation`: A variable character string (max 50) (e.g., 'Core Member', 'Chief Strategic Officer').
* `joined_at`: A timestamp that defaults to the current time.

**Step 3: The Events Table**
Create an `events` table to log community workshops and hackathons:
* `event_id`: An integer that auto-increments and serves as the Primary Key.
* `event_name`: A variable character string (max 150) that cannot be null.
* `event_date`: A standard `DATE` format.
* `location`: A variable character string (max 100).
* `is_active`: A boolean (or tinyint) that defaults to true (1).

## ⚠️ Common Pitfalls & Expected Bugs
* **Forgetting `USE database_name;`:** If you create the database but forget to select it, MySQL Workbench won't know where to put your tables and will throw a "No database selected" error.
* **String Lengths:** Always limit your `VARCHAR` lengths. Giving a first name `VARCHAR(255)` wastes memory. Be precise with your architecture.

## 🧠 Outcomes & Learnings
* Understood how to map real-world entities (community members, tech events) into strict digital schemas.
* Mastered the creation of Primary Keys to ensure absolute data integrity.

---

## 📱 LinkedIn Post Template

**Share your progress!** Copy this template, attach a screenshot of your successful MySQL Workbench execution, and post it to LinkedIn. 

> **Day 1/21 of the SQL Database Challenge! 🚀**
>
> Today, I kicked off my journey into raw data architecture with @Synexus. For the next 21 days, I am building the backend data infrastructure for the Synexus Core Operations platform—an application designed to manage technical communities, projects, and event telemetry.
>
> Instead of relying on frameworks to do the heavy lifting, I am writing pure SQL. Today’s focus was Data Definition Language (DDL). I successfully initialized the database and architected the schemas for the `members` and `events` tables, focusing strictly on optimal data types and Primary Key integrity.
> 
> Standard, not a trend. The logic, not a language. Let's build! 
> 
> 🔗 Source Code: [Link to your GitHub Repo]
> 
> #21DaysSQL #Synexus #DatabaseDesign #MySQL #DataEngineering #SQL #BuildInPublic