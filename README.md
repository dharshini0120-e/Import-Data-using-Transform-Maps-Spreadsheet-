# Import Data using Transform Maps (Spreadsheet)

## Project Overview
This project demonstrates importing structured employee data from an external spreadsheet into the ServiceNow platform using **Import Sets** and **Transform Maps**. The workflow automates data migration, prevents duplicate records using **Coalesce**, and provides visual insights via custom **Reports and Dashboards**.

---

## Technical Specifications

### Target Table Configuration
* **Table Label:** `Employee Test`
* **Table Name:** `u_employee_test`
* **Fields Created:**
  * `Employee ID` (String)
  * `Employee Name` (String)
  * `Email` (String)
  * `Department` (String)
  * `Location` (String)

---

## Project Execution Steps

### Phase 1: Data Preparation & Import Set Table
1. Created a sample spreadsheet containing employee details (`Employee ID`, `Name`, `Email ID`, `Department`, `Location`).
2. Loaded data into ServiceNow via **System Import Sets -> Load Data**.
3. Created an Import Set Table labeled **`Employee Import`** (`u_employee_import`).

### Phase 2: Transform Map Configuration
1. Created a Transform Map named **`Sample Spreadsheet Import`**.
   * **Source Table:** `u_employee_import`
   * **Target Table:** `u_employee_test`
2. Configured field mapping using **Auto Map Matching Fields** and verified mapping accuracy via **Mapping Assist**.
3. Executed the transformation to insert records into the target table.

### Phase 3: Preventing Duplicates (Coalesce Setting)
1. Enabled **Coalesce = True** on the **`Employee ID`** field within the Transform Map.
2. Verified that re-importing updated data updates existing records rather than creating redundant duplicates.

### Phase 4: Reports & Dashboards Creation
Created three custom reports on the `u_employee_test` table:
1. **Employees by Department:** Pie Chart grouped by `Department`.
2. **Employees by Location:** Bar Chart grouped by `Location`.
3. **Employee List Report:** Detailed List view of all records.

Consolidated all three reports into a centralized dashboard named **`Employee Analytics Dashboard`**.

---

## Submission Resources
* **Demo Video Link:** [Click Here to Watch Demo Video](PASTE_YOUR_GOOGLE_DRIVE_VIDEO_LINK_HERE)

---

## Deliverables
* Sample Excel Data Sheet (`sample_data.csv`)
* Transform Map Script Setup (`transform_script_notes.txt`)
* Executive Analytics Dashboard
*
