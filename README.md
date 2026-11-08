# ⚡ LeadFlow — Smart Lead Capture Automation

<p align="center">
  <strong>Capture Leads. Detect Opportunities. Automate Follow-ups.</strong>
  <br/>
  An intelligent lead management workflow built with <strong>n8n</strong>, Google Sheets & Telegram.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Automation-n8n-FF6D5A?style=for-the-badge&logo=n8n&logoColor=white" />
  <img src="https://img.shields.io/badge/Database-Google%20Sheets-34A853?style=for-the-badge&logo=googlesheets&logoColor=white" />
  <img src="https://img.shields.io/badge/Notifications-Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" />
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge" />
</p>

---

## ◈ Overview

**LeadFlow** is an automated lead capture and notification system designed to simplify enquiry management.

Whenever someone submits an enquiry form, the workflow automatically collects their information, stores it in Google Sheets, evaluates their budget, and sends an instant Telegram notification.

No manual sorting. No missed enquiries. Just smarter lead management.

## ◈ How It Works

```text
       ┌──────────────────┐
       │   Enquiry Form   │
       └────────┬─────────┘
                │
                ▼
       ┌──────────────────┐
       │  Google Sheets   │
       │   Store Lead     │
       └────────┬─────────┘
                │
                ▼
       ┌──────────────────┐
       │   IF Condition   │
       │ Budget >= 20000? │
       └────────┬─────────┘
                │
          ┌─────┴─────┐
          ▼           ▼
     ┌─────────┐ ┌──────────┐
     │   YES   │ │    NO    │
     └────┬────┘ └─────┬────┘
          ▼            ▼
    🔥 Hot Lead    🔔 Normal
      Telegram      Telegram
       Alert          Alert

       ┌──────────────────┐
       │   Error Trigger  │
       └────────┬─────────┘
                ▼
       ⚠️ Telegram Error Alert
```

## ◈ Key Features

| Feature | Description |
|---|---|
| 📩 Automated Capture | Collects enquiry details through a form |
| 📊 Lead Storage | Saves submissions in Google Sheets |
| 🔥 Smart Classification | Identifies leads with a budget of ₹20,000 or more |
| ⚡ Instant Alerts | Sends real-time Telegram notifications |
| ⚠️ Error Handling | Separate workflow for failure notifications |
| 🚀 Live Automation | Runs automatically after publishing |

## ◈ Tech Stack

- **n8n Cloud** — Workflow automation platform
- **Google Sheets** — Lead database and storage
- **Telegram Bot API** — Instant notifications
- **Expressions** — Dynamic data mapping
- **IF Node** — Conditional lead classification
- **Error Trigger** — Workflow failure monitoring

## ◈ Project Structure

```text
LeadFlow/
│
├── workflows/
│   ├── lead-capture-workflow.json
│   └── error-workflow.json
│
├── screenshots/
│   ├── workflow-canvas.png
│   └── error-workflow.png
│
└── README.md
```

## ◈ Workflow Screenshots

### Main Automation
![Main Workflow](<img width="1666" height="758" alt="Screenshot 2026-11-08 190205" src="https://github.com/user-attachments/assets/2467006b-16e3-4704-9ced-3a53c3ba172c" />
)

### Error Handling Workflow
![Error Workflow](<img width="1668" height="756" alt="Screenshot 2026-11-08 190254" src="https://github.com/user-attachments/assets/3b62724f-2f57-4ad5-a29e-9ad048b22d86" />
)

## ◈ Setup & Installation

1. Download or clone this repository.
2. Open your n8n workspace.
3. Import the main workflow JSON.
4. Connect your Google Sheets credentials.
5. Configure your Telegram Bot credentials.
6. Import and configure the Error Workflow.
7. Test the workflow using the form's test URL.
8. Publish the workflow to activate production automation.

**Note:** Credentials, spreadsheet references, and form URLs must be configured for your own environment. Never commit API tokens or private credentials.

## ◈ Real-World Applications

- Freelancers managing client enquiries
- Small businesses tracking potential customers
- Coaching institutes handling admissions
- College clubs managing registrations
- Service providers qualifying incoming leads

## ◈ Future Improvements

- [ ] Email notifications for high-priority leads
- [ ] Automatic follow-up reminders
- [ ] Lead status tracking
- [ ] Daily and weekly lead reports
- [ ] AI-powered lead scoring

## ◈ What I Learned

Through this project, I explored:

- Building automated workflows using n8n
- Integrating third-party services
- Working with dynamic JSON expressions
- Implementing conditional logic
- Managing API credentials
- Designing error-handling workflows
- Deploying and publishing live automations

---

<p align="center">
  <strong>⚡ Built to automate. Designed to simplify.</strong>
  <br/><br/>
  Made with ❤️ using n8n
</p>
