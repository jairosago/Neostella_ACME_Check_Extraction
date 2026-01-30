# Neostella ACME Check Extraction

## Overview
This project is a UiPath automation developed as part of a technical assessment.  
It processes Work Items from the ACME Test System by filtering items with Type **WI2** and Status **Open**, extracting check information from PDF documents, and generating a consolidated Excel report.

## Process Description
The automation performs the following steps:
- Logs into the ACME Test System
- Navigates to the Work Items section
- Filters Work Items with Type **WI2** and Status **Open**
- Downloads the associated check request PDFs
- Extracts key check data (Client Name, Client ID, Check Number, Check Date, Check Amount)
- Stores the extracted data in a DataTable
- Generates an Excel report at the end of the process
- Updates each Work Item status to **Completed**

## Project Structure
- **Framework/**: UiPath REFramework components
- **Processes/**: Business process workflows (Login, Get Work Items, Process Work Item, Update Work Item)
- **Utils/**: Reusable utility workflows (PDF and Regex extraction)
- **Data/**: Configuration and supporting data files

## Configuration
- ACME credentials are managed via `Config.xlsx` using SecureString values.
- The project uses UiPath REFramework without Orchestrator queues, allowing local execution.

## Prerequisites
- UiPath Studio installed
- Valid ACME Test System credentials
- Internet access

## Notes
- Sample PDFs and output files are not included in the repository for security and best practices reasons.
