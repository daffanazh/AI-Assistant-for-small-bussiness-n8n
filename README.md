# AI-Powered Transaction & Receipt Management Bot

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e8281bf4-b586-484d-978c-dd11cbd5db4c" />

## Executive Summary
This project demonstrates a highly advanced, multimodal Telegram bot built with **n8n**. Designed for automated transaction logging and expense tracking, the system intelligently parses user inputs—processing both text commands and AI-driven image analysis for physical receipts. It functions as a complete micro-application, featuring live database management, on-demand Excel report generation, and built-in interactive menus.

## Business Value
* **Multimodal Data Entry:** Users can log transactions by typing text or simply snapping a photo of a physical receipt, drastically reducing manual administrative work.
* **Automated AI Vision:** Leverages AI image analysis to extract structured financial data from raw photos and maps them directly into database columns.
* **On-Demand Excel Reporting:** Dynamically fetches database records, converts the JSON payload into a downloadable `.xlsx` file, and delivers it directly to the user's chat.
* **Self-Contained Ecosystem:** Features a custom JavaScript routing engine that handles invalid inputs, displays module guides, and safely executes database resets.

## System Architecture & Dynamic Routing
The workflow is orchestrated by a central JavaScript parser that acts as the "brain" of the bot, directing traffic to specialized execution branches:

1. **Master Trigger & Logic Engine:** Intercepts Telegram payloads and runs custom JavaScript to define command rules and validation logic.
2. **Central Router (`Switch`):** Evaluates the parsed rules and routes the data to one of the following execution paths:
   * **Path A: Text Transactions & Document Generation:** Appends text inputs to Google Sheets. When a summary is requested, it retrieves the dataset, converts it into a binary Excel file, and sends the document to the user.
   * **Path B: Visual AI Processing:** Downloads image attachments, processes the receipt via an AI Image Analyzer, formats the extracted data using JavaScript, and logs it into the database.
   * **Path C: Utility & Maintenance:** Handles operational commands by sending interactive menus, usage guides, and executing database purges (`Clear sheet`) with success confirmations.

## Tech Stack
* **Workflow Automation:** n8n (Advanced Routing & Binary Data Handling)
* **AI Engine:** AI Vision / Image Analysis
* **Database Operations:** Google Sheets API (CRUD operations)
* **Data Transformation:** Custom JavaScript & JSON-to-XLSX Conversion
* **User Interface:** Telegram Bot API

---
*Built to streamline financial tracking and data extraction. Open for freelance opportunities and custom workflow architecture.*
