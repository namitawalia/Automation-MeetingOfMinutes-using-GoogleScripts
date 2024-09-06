# Minutes of Meeting Automation Script

This Google Apps Script automates the process of sharing **Minutes of Meeting (MoM)** via email and records the details for future reference. It uses data from Google Sheets and sends the formatted MoM to a list of recipients specified in the sheet. The script also logs the details in a historical database and tracks incremental IDs for the emails. The sheet names have been generalised to ensure data security for the organisation.

## Features
- **Automates email distribution**: Sends MoM to a list of recipients with an organized HTML table format.
- **Logs email details**: Records the subject, timestamp, and sender information in a tracking sheet for future reference.
- **Incremental tracking**: Assigns an incrementing number for each MoM email.
- **Handles multiple meeting types**: Customizes the email subject based on the type of meeting (e.g., Weekly Call, Other Call).
- **Data management**: Logs meeting data in a historical database and resets the working sheet for the next meeting.

## How It Works

1. **Main Sheet**: Stores the meeting details (e.g., agenda, discussion points) that need to be processed and sent.
2. **POC Sheet**: Contains the list of email recipients.
3. **Tracking Sheet**: Keeps a record of the sent emails (subject, timestamp, sender) and maintains the increment number for MoM emails.
4. **Document Sheet**: Stores historical data for future reference, including meeting timestamps and subjects.

### Process Overview:
- The script extracts meeting details from the **Main Sheet**.
- It sorts the data, formats it into an HTML table, and sends an email to the recipients listed in the **POC Sheet**.
- The subject of the email is dynamically generated based on meeting type and increment number.
- The script logs the sent email details in the **Tracking Sheet** and stores the data in the **Document Sheet**.
- After sending, it resets the main sheet's content while keeping formulas intact.

## Setup Instructions

1. **Google Sheet Structure**:
   - **Main Sheet**: Contains meeting data starting from cell `B2` to `F`.
   - **POC Sheet**: Column `B` contains email addresses of the recipients.
   - **Tracking Sheet**: Keeps logs of sent emails and tracks the increment number in cell `Z1`.
   - **Document Sheet**: Stores the historical data of MoM.

2. **Google Apps Script**:
   - Copy and paste the provided Google Apps Script into your Google Sheet's Apps Script editor.
   - Ensure your Google Sheet has the required sheets named appropriately (or modify the script to match your sheet names).
   - Run the script manually or set up a time-based trigger to automate the process.

## Script Execution

To execute the script:
1. Open the Google Sheet.
2. Go to `Extensions > Apps Script`.
3. Paste the script and save it.
4. Run the function `processMinutesOfMeeting()` to send the MoM and log the details.
5. Optionally, set a trigger to run the script at regular intervals (e.g., after each meeting).

---

## 🔥 How It Helped 🔥

This automation script has significantly reduced the **Turnaround Time (TAT) by 70%** and improved overall communication. By streamlining the process of sharing minutes of meetings, we ensure that tasks are communicated to the correct **Point of Contact (POC)**, driving the tasks towards **closure** more effectively. This has resulted in **better outcomes** and greater efficiency in task management.

---


