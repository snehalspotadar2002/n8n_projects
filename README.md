# Lead Form Automation using Email (n8n)

## 📌 Project Overview

This project is an **n8n workflow automation** that captures lead data from a form, stores it in Google Sheets, and sends automated emails based on the lead's profession.

The workflow performs the following actions:

1. Collects lead information through an n8n form.
2. Appends lead data to Google Sheets.
3. Filters and routes leads based on profession.
4. Sends personalized welcome emails.
5. Sends a notification email to the manager.

---

## 🚀 Features

- Web-based Lead Generation Form
- Automatic Data Storage in Google Sheets
- Conditional Email Routing (Client / Student / Employee)
- Personalized Email Templates
- Manager Notification for New Leads
- Fully Automated Workflow

---

## 🧩 Form Fields

The form collects the following information:

- First Name
- Last Name
- Coder (Yes / No)
- Email Id
- Profession  
  - Client  
  - Student  
  - Employee  

---

## 🔄 Workflow Architecture

### 1️⃣ Form Trigger
- Node: `On form submission`
- Captures lead data when the form is submitted.

### 2️⃣ Google Sheets Integration
- Node: `Append row in sheet`
- Appends lead details to a connected Google Sheet.

### 3️⃣ Filter Node
- Ensures only valid Profession values:
  - Client
  - Student
  - Employee

### 4️⃣ Switch Node
Routes leads based on Profession:

| Profession | Email Sent |
|------------|------------|
| Client     | Service Welcome Email |
| Student    | Course Welcome Email |
| Employee   | Organization Welcome Email |

### 5️⃣ Email Automation (Gmail Nodes)

- `client_mail`
- `Student_mail`
- `Employee_mail`

Each lead receives a personalized email using dynamic fields:
