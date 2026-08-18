# 📱 Google Sheets → WhatsApp Messaging Automation

An automated WhatsApp messaging workflow built using **n8n**, **Google Sheets**, and the **WhatsApp Cloud API**.

This project demonstrates how a Google Sheet can be used as a simple data source for managing contacts and messages, while n8n handles the automation, processing, and WhatsApp API integration.

---

## 🚀 Project Overview

The goal of this project is to automate WhatsApp messaging using data maintained in a Google Sheet.

Instead of manually copying phone numbers and messages and sending them individually, the workflow reads the required information from Google Sheets and automatically sends WhatsApp messages through the WhatsApp Cloud API.

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



