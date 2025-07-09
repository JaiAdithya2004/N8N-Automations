# N8N-Automations


***Gmail Automation***

![Screenshot 2025-06-30 213005](https://github.com/user-attachments/assets/c1c83030-2ae6-4013-9304-c3a7db835b12)

Workflow:

Trigger
→ Manually execute the workflow using the "Execute Workflow" node in n8n.

Read Google Sheet
→ Fetch rows from a specified Google Sheet (e.g., with columns like email, subject, message).

Send Emails via Gmail
→ Loop through each row and send a personalized email using Gmail credentials.






***News Updation Agent***
(Built for collegepur)


This agent automatically scrapes the latest news from CollegeDunia every hour.
It helps track real-time updates in the education sector without manual effort.
The data is cleaned, structured, and stored in Google Sheets for easy access.
Ideal for building dashboards, trend analysis, or sending alerts.
Saves time for research, marketing, and academic teams monitoring edtech news.


![image](https://github.com/user-attachments/assets/16447e06-0b6d-4e3b-a5d6-71bd3c06cb40)


Workflow:

How It Works:
1) Schedule Trigger:

Triggers the agent once every hour.

2) HTTP Request:

Sends a GET request to the CollegeDunia news page to fetch the HTML content.

3) HTML Extract:

Parses the raw HTML content to prepare it for data extraction.

4) Code Node:

Custom JavaScript logic extracts key data fields (news headline, date, source, URL) from the HTML structure.

5) Edit Fields:

Transforms or formats the scraped data manually (e.g., adjusting field names, cleaning strings).

6) Google Sheets:

Appends the final transformed data as a new row in a connected Google Sheet for persistent storage.










***Weekly Business Report Generator***






![image](https://github.com/user-attachments/assets/7722d878-0a0b-4481-8e98-a1f1c0ec252f)




This workflow automates the generation, formatting, and delivery of a weekly business performance report using:

1) Google Sheets (as a data source),

2) GPT-4o or language model (to summarize/analyze),

3) HTML formatting,

4) PDF conversion,

5) Gmail (for delivery)

Workflow Steps Breakdown:

Schedule Trigger – Automatically starts the workflow weekly (e.g., every Monday at 9 AM).

Google Sheets - Read Sheet – Pulls real-time business metrics from a connected spreadsheet.

Code Node – Formats and structures data for effective AI processing.

HTTP Request - GPT-4o – Sends data to GPT-4o to generate summaries, insights, and suggestions.

HTML Node - Generate HTML Template – Converts the AI output into a styled, readable HTML report.

Edit Fields Node – Allows optional manual review or field updates before final formatting.

HTTP Request (PDFLayer) – Transforms the HTML into a shareable and professional PDF report.

Gmail - Send Message – Emails the final report to stakeholders as an attachment or HTML message.










