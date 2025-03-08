# Job Application Pipeline Automation

## Overview

This project automates the processing of job application submissions by integrating a live web form with Google Sheets, Google Drive, and external APIs. It streamlines the process of collecting candidate data, processing CV links, triggering webhook notifications, and scheduling follow-up emails.

## Features

- **Live Hosted Form:**  
  A fully functional form that allows candidates to submit their name, email, phone number, and CV link.

- **Google API Integration:**  
  Uses Google Sheets API to fetch submission data and Google Drive API to process CV links.

- **CV Processing:**  
  Extracts file IDs from various Google Drive URL formats and simulates CV parsing (education, qualifications, projects).

- **Webhook Notification:**  
  Sends a JSON payload containing processed data to a specified webhook URL.

- **Email Automation:**  
  Schedules and sends follow-up emails using APScheduler and SMTP.

## Architecture

![Job Application Pipeline Automation -Architecture](https://github.com/user-attachments/assets/7f8f4b6c-219c-44ec-85c2-b0cbc19d365c)


1. **Data Collection:**  
   Candidates submit their details through a live web form.
   
2. **Data Storage:**  
   Submissions are stored in a publicly accessible Google Sheet.
   
3. **Data Processing:**  
   A Python script:
   - Retrieves submission data from the Google Sheet.
   - Extracts the file ID from the provided CV link.
   - Simulates CV processing (dummy data extraction).
   - Sends a webhook notification with the processed data.
   
4. **Automation:**  
   Schedules follow-up emails to be sent at a predetermined time.


## Installation & Setup

### Prerequisites

- Python 3.7+
- Pip (Python package manager)

### Dependencies

Install the required packages with:

```bash
pip install google-api-python-client apscheduler requests
