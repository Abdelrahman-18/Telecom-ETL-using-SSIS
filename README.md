📡 Telecom ETL SSIS Project

An ETL pipeline built with SQL Server Integration Services (SSIS) for a telecom company.
It extracts CSV files generated every 5 minutes, transforms them using business rules, and loads clean records into SQL Server while redirecting invalid rows to error tables for review.

🚀 Key Features

File Handling – Loops through CSV files from source folders, moves processed files.

Data Transformation – Validates columns (IMSI, IMEI, CELL, LAC, EVENT_TS) with derived columns, lookups, and conditional splits.

Database Loading – Inserts valid rows into [dbo].[telecom_transaction], rejects invalid ones into [dbo].[error_transaction] and logs sources in [dbo].[error_source_output].

🧰 Tech Stack

SSIS (Foreach Loop, Data Flow Task, File System Task, OLE DB Destination)

SQL Server 2019+ (Database: SSIS_Telecom_DB)

Visual Studio (SSDT) for package development

📁 Structure
Telecom_ETL_SSIS_Project/
│── Packages/       # SSIS .dtsx packages
│── SQL_Scripts/    # Database scripts
│── Config/         # Connection settings
└── README.md

