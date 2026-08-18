# 📱 Google Sheets → WhatsApp Messaging Automation

An automated WhatsApp messaging workflow built using **n8n**, **Google Sheets**, and the **WhatsApp Cloud API**.

This project demonstrates how a Google Sheet can be used as a simple data source for managing contacts and messages, while n8n handles the automation, processing, and WhatsApp API integration.

---

## 🚀 Project Overview

The goal of this project is to automate WhatsApp messaging using data maintained in a Google Sheet.

Instead of manually copying phone numbers and messages and sending them individually, the workflow reads the required information from Google Sheets and automatically sends WhatsApp messages through the WhatsApp Cloud API.

# 📱 Google Sheets → WhatsApp Messaging Automation

An automated WhatsApp messaging workflow built using **n8n**, **Google Sheets**, and the **WhatsApp Cloud API**.

This project demonstrates how a Google Sheet can be used as a simple data source for managing contacts and messages, while n8n handles the automation, processing, and WhatsApp API integration.

---

## 🚀 Project Overview

The goal of this project is to automate WhatsApp messaging using data maintained in a Google Sheet.

Instead of manually copying phone numbers and messages and sending them individually, the workflow reads the required information from Google Sheets and automatically sends WhatsApp messages through the WhatsApp Cloud API.

## 🚀 Features

Read WhatsApp recipient information from Google Sheets.
Process multiple contacts using n8n.
Dynamically generate WhatsApp messages.
Send messages through WhatsApp Cloud API.
Use API authentication securely through n8n credentials.
Automate repetitive WhatsApp communication.
Build a reusable automation workflow.
Can be extended with status tracking and error handling.

**Technologies Used
Technology	Purpose**
n8n:	Workflow automation
Google Sheets:	Contact/message data source
WhatsApp Cloud API:	WhatsApp messaging
Meta Graph API:	API communication
HTTP Request:	Send API requests
JSON:	           Data exchange
Google Sheets API:	Read/write spreadsheet data

📊 Google Sheet Structure

The Google Sheet acts as the data source for the workflow.

Example:

Name	Phone	Message	Status
Ram	+919XXXXXXXXX	Hello John!	Pending
Rams	+919XXXXXXXXX	Your order is confirmed.	Pending
John	+919XXXXXXXXX	Your appointment is confirmed.	Pending

The workflow can read each row and process the records automatically.

🔄 How the Automation Works
Step 1 — Google Sheets

The workflow reads the messaging information from Google Sheets.

The sheet contains information such as:

Name
Phone
Message
Status

### Workflow

```text
┌──────────────────────┐
│    Google Sheets     │
│                      │
│ Phone Number         │
│ Message              │
│ Status               │
└──────────┬───────────┘
           │
           │ Read Data
           ▼
┌──────────────────────┐
│         n8n          │
│                      │
│ Read & Process Data  │
│ Validate Information │
│ Prepare Message      │
└──────────┬───────────┘
           │
           │ API Request
           ▼
┌──────────────────────┐
│ WhatsApp Cloud API   │
│       (Meta)         │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│ WhatsApp Recipient   │
└──────────────────────┘ 
