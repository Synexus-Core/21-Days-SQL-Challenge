# 🗓️ Day 3: Modifying & Removing Data (Update & Delete)

## 🎯 Problem Statement
In the real world, data changes constantly. A Synexus community member might get promoted to a leadership role, or a scheduled event might get cancelled due to weather. We cannot simply add new records every time something changes; we must modify the existing ones. Today, we learn the final pieces of basic CRUD: `UPDATE` and `DELETE`.

## 🛠️ Tech Stack & Focus Areas
* **Tool:** MySQL Workbench
* **Core Concepts:** `UPDATE`, `SET`, `DELETE FROM`, and the critical `WHERE` clause.
* **Goal:** Safely change a member's designation and remove a cancelled event from the database.

## 📝 Task Requirements

**Step 1: Setup & Mock Data**
Start with `USE synexus_db;`. To practice safely, write an `INSERT` statement to add a "Test Member" and a "Test Event" so we have data we don't mind changing or deleting.

**Step 2: The `UPDATE` Statement**
Write an `UPDATE` query to change the designation of your test member. 
* *Beginner Tip: You must tell SQL exactly WHICH row to update using the `WHERE` clause (e.g., `WHERE first_name = 'Test'`).*

**Step 3: The `DELETE` Statement**
Write a `DELETE FROM` query to permanently remove the test event you created from the `events` table. 
* *Beginner Tip: Just like `UPDATE`, you MUST use `WHERE` to target the specific event.*

**Step 4: Verify Your Changes**
Write `SELECT *` queries for both tables to confirm that the member was updated and the event was successfully deleted.

## ⚠️ Common Pitfalls & Expected Bugs
* **THE FORGOTTEN WHERE CLAUSE (DANGER):** If you type `UPDATE members SET designation = 'Lead';` without a `WHERE` clause, SQL will update **EVERY SINGLE MEMBER** in your table to 'Lead'. If you type `DELETE FROM events;`, it will wipe the entire table. **Always use `WHERE`.**
* **Safe Update Mode Error:** MySQL Workbench has a built-in safety net called "Safe Updates" (Error Code: 1175). It prevents you from updating or deleting rows unless you use the Primary Key (like `member_id`) in your `WHERE` clause. If you hit this error, the reference solution shows how to temporarily disable it, or you can find the specific `member_id` and use that!

## 🧠 Outcomes & Learnings
* Mastered the complete CRUD lifecycle (Create, Read, Update, Delete).
* Understood the critical importance of the `WHERE` clause for targeting specific data.
* Learned how to navigate database safety features.

---

## 📱 LinkedIn Post Template

**Share your progress!** 

> **Day 3/21 of the SQL Database Challenge! 🚀**
>
> Today, I completed the foundational CRUD lifecycle by mastering `UPDATE` and `DELETE` operations! 
>
> Modifying and removing data is powerful, but dangerous. The biggest lesson today was the critical importance of the `WHERE` clause. Forgetting it means accidentally wiping or overwriting your entire database! I successfully updated member roles and removed cancelled events from the Synexus database safely.
>
> The core foundation is set. Tomorrow, we start filtering and sorting our data!
> 
> 🔗 Source Code: [Link to your GitHub Repo]
> 
> #21DaysSQL #Synexus #DatabaseDesign #MySQL #DataEngineering #SQL #BuildInPublic