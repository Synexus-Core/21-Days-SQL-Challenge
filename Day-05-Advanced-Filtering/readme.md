# 🗓️ Day 5: Advanced Filtering (LIKE, IN, BETWEEN)

## 🎯 Problem Statement
As data scales, your search requirements become more complex. You won't always know the exact name or date you are looking for. You might need to find members based on a pattern (like a specific email domain), or check if an event falls within a specific quarter of the year. Today, we replace long, messy `OR` chains with highly efficient, advanced filtering operators.

## 🛠️ Tech Stack & Focus Areas
* **Tool:** MySQL Workbench
* **Core Concepts:** * `LIKE`: Pattern matching using wildcards (`%` and `_`).
  * `IN`: Checking if a value matches any item in a specific list.
  * `BETWEEN`: Filtering within a specific numerical or date range.
* **Goal:** Write clean, optimized queries to find specific subsets of the Synexus community data.

## 📝 Task Requirements

**Step 1: Setup**
As always, begin with `USE synexus_db;`. 

**Step 2: Pattern Matching (`LIKE`)**
Write a query to find all members whose `first_name` starts with the letter 'A'. 
* *Beginner Tip: The `%` symbol is a wildcard that means "zero or more of any character". So, `'A%'` means "Starts with A, and can have anything after it."*

**Step 3: Checking Lists (`IN`)**
Imagine the Core Committee wants a list of all leadership roles. Instead of writing `designation = 'Founder' OR designation = 'Chief Strategic Officer' OR designation = 'Chief Planning Officer'`, use the `IN` operator!
Write a query to find all members whose designation is in a list of at least three specific roles.

**Step 4: Filtering Ranges (`BETWEEN`)**
Write a query to find all community events that are scheduled to happen between two specific dates (e.g., September 1st, 2026 and December 31st, 2026).
* *Beginner Tip: `BETWEEN` includes the start and end values (it is inclusive).*

## ⚠️ Common Pitfalls & Expected Bugs
* **Case Sensitivity with `LIKE`:** In standard MySQL configurations, `LIKE` is not case-sensitive. `'A%'` and `'a%'` will return the same results. 
* **The `BETWEEN` Date Trap:** When using `BETWEEN` with standard dates (e.g., `'2026-10-31'`), it assumes the time is exactly midnight (`00:00:00`) on that day. If an event has a specific timestamp later in that day, it might get excluded! Stick to standard `DATE` columns for this exercise.
* **Overusing Wildcards:** Writing `LIKE '%A%'` (finding 'A' anywhere in the string) forces the database to scan every single letter of every single row. It is very slow on massive databases!

## 🧠 Outcomes & Learnings
* Replaced messy logical chains (`OR`) with clean, readable operators (`IN`).
* Mastered wildcard string searching to find partial data matches.
* Easily isolated date ranges using the `BETWEEN` operator.

---

## 📱 LinkedIn Post Template

**Share your progress!** > **Day 5/21 of the SQL Database Challenge! 🚀**
>
> Writing endless `OR` statements is inefficient. Today with @Synexus, I upgraded my querying logic using advanced SQL filters: `LIKE`, `IN`, and `BETWEEN`.
>
> I successfully extracted members based on text patterns using wildcard operators (`%`), filtered leadership roles using standard list matching, and isolated Q4 community events using date ranges. 
>
> Learning to ask the database the *right* questions, in the cleanest possible way, is the true mark of a Data Engineer.
> 
> 🔗 Source Code: [Link to your GitHub Repo]
> 
> #21DaysSQL #Synexus #DatabaseDesign #MySQL #DataEngineering #SQL #BuildInPublic