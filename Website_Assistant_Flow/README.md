# Website AI Assistant - N8N Workflow

## Overview

This n8n workflow automates contact form submissions on your website by capturing user inputs and routing the data to Gmail, Google Sheets, & Telegram.

## Features

- Receives contact form data via webhook.
- Extracts and stores user details: name, email, message, phone, session ID, and timestamp.
- Maintains conversation memory for AI enhancements.
- Sends notifications via Telegram.
- Logs submissions in Google Sheets for easy tracking.
- Sends admin copy and auto-reply emails using Gmail.
- Responds to the webhook with a success message.

## Prerequisites

- n8n instance with Docker or other hosting.
- Google Sheets account with API credentials.
- Telegram bot API token.
- Gmail account with OAuth2 credentials.
- OpenAI API key.
- Your n8n instance domain with valid webhook URL.

## Installation

1. **Import Workflow:**
   
   - Export this workflow JSON from your current n8n or use the attached JSON file.
   - Go to your n8n editor → Menu → Import → Upload JSON.

2. **Configure Credentials:**
   
   - Set up the following credentials in n8n:
     - **Telegram API**
     - **Google Sheets OAuth2**
     - **Gmail OAuth2**
     - **OpenAI API**

3. **Update Workflow Settings:**
   
   - Replace placeholder values such as Google Sheets document ID, Telegram chat ID, Gmail sender details, and OpenAI model parameters.
   - Set your webhook URL in your website/contact form to point to the n8n webhook node path.

## Usage

- When a user submits the contact form, the data is processed and saved across various channels.
- The Telegram node sends you a notification.
- The Google Sheets node logs the submission.
- Admin receives an email copy; the user receives an auto-reply.
- AI Agent node powers any smart responses or automation linked to OpenAI.

## Notes

- Create your own email message templates and Telegram notifications as needed.

- Ensure the webhook URL path remains consistent.

- Keep API keys secure; do not expose them publicly.

- Maintain your OpenAI model usage limits to avoid overages.

## Support

For questions or issues, please open an issue on the GitHub repository or contact the workflow creator.

---

Thank you for using this n8n Workflow. Feel free to fork, modify, and share.
