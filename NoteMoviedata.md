# Movies Data Cleaning Project

## Author
**Mazedul Dipu** – *Data Enthusiast*

## Project Overview
This project focuses on cleaning a raw movie dataset (`movies_db_uncleaned`) to prepare it for analysis. 
The goal is to ensure consistency, accuracy, and completeness across columns such as **studio**, 
**movie_id_title**,
 and financial data using Excel functions and operations.

## Dataset Description
- **Source File:** `movies_db_uncleaned`
- **Main Sheets:**
  - **Movies** – Contains movie details such as studio, movie ID & title.
  - **Financials** – Contains financial information such as budget, currency, unit, and revenue.

## Cleaning Steps Performed

### 1. Handling Missing Values in `studio` Column
- Selected the entire `studio` column using **Ctrl + Shift + ↓**.
- Used **Ctrl + F → Replace** to replace blank cells with **"Not Available"**.

### 2. Removing Extra Spaces (TRIM Function)
- Applied `TRIM` function in a new column to remove leading/trailing spaces.
- Copied the cleaned values and pasted them back into the original `studio` column using
 **Paste Special (Values Only)**.

### 3. Removing Duplicate Movie Entries
- Selected the `movie_id_title` column.
- Used **Data → Remove Duplicates** to eliminate duplicate records.
- Optionally highlighted duplicates for review.

### 4. Splitting `movie_id_title` into Two Columns
- Used **Text to Columns** to separate **Movie ID** and **Movie Title**.
- Created two blank columns first to avoid overwriting existing columns (e.g., industry, release year).

### 5. Merging Financial Data Using VLOOKUP
- Added a new column in the **Movies** sheet to bring financial data.
- Used `VLOOKUP` to pull **Budget**, **Currency**, **Unit**, and **Revenue** from the **Financials** sheet.

#### Example Formula Used:
```excel
=VLOOKUP([@[movie_id]], Financials, 2, FALSE)
Key Excel Functions Used
Purpose	Function/Feature
Replace blanks	Ctrl + F → Replace
Trim spaces	TRIM()
Remove duplicates	Data → Remove Duplicates
Text separation	Text to Columns
Lookup values	VLOOKUP()

Final Outcome
The cleaned dataset is now:

Free of blanks and unnecessary spaces.

Structured with separate Movie ID and Title columns.

Enriched with financial data using VLOOKUP.