📡 Telecom ETL SSIS Project

An ETL pipeline built with SQL Server Integration Services (SSIS) for a telecom company.
It extracts CSV files generated every 5 minutes, transforms them using business rules, and loads clean records into SQL Server while redirecting invalid rows to error tables for review.

🚀 Key Features

The telecom system generates a CSV file every 5 minutes with customer transaction data.
The SSIS package automates the following steps:

1. File Iteration – Scans source folders using a Foreach Loop Container.

2 .Extraction – Reads CSV data through Flat File Sources.

3. Transformation – Applies rules with Derived Columns, Lookups, and Conditional Splits.

4. Loading – Inserts valid data into the main transaction table.

5 .Error Handling – Redirects invalid rows to error tables with file-level tracking.


🧰 Tools Used

SSIS (Foreach Loop, Data Flow Task, File System Task, OLE DB Destination)

SQL Server 2019+ (Database: SSIS_Telecom_DB)

Visual Studio (SSDT) for package development


🗃️ Database & Tables

Target database: SSIS_Telecom_DB

[dbo].[telecom_transaction] → Valid, clean records ✅

[dbo].[error_transaction] → Invalid rows ❌

[dbo].[error_source_output] → Logs source file names & rejected rows 📄

[dbo].[dim_imsi_reference] → Lookup table for IMSI validation 🔍


📁 Structure

Telecom_ETL_SSIS_Project/
│── Packages/       # SSIS .dtsx packages
│── SQL_Scripts/    # Database scripts
│── Config/         # Connection settings
└── README.md


