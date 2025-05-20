# AirborneX Website

This repository contains the website for AirborneX, a company developing next-generation crash-proof drones.

## Contact Form Integration with Google Sheets

The contact form has been integrated with Google Sheets using sheet2api. The form shows a thank you message on the same page after submission.

### 1. Prepare Your Google Sheet

1. Create a new Google Sheet
2. Add the following column headers in the first row:
   - `name`
   - `email`
   - `message`
   - `timestamp` (optional)

Example:

| name | email | message | timestamp |
|------|-------|---------|-----------|
|      |       |         |           |

### 2. Create Your sheet2api Integration

1. Go to [sheet2api.com](https://sheet2api.com/) and sign up or log in
2. Share your Google Sheet with the email provided by sheet2api
3. Create a new API using the shared Google Sheet URL
4. In the sheet2api dashboard, click on "Website Form to Sheet"
5. Copy the endpoint URL provided

### 3. Update the Website Form

1. Open `index.html`
2. Find the form tag: `<form id="contact-form" class="contact-form" action="https://sheet2api.com/v1/YOUR_SHEET2API_ENDPOINT_URL_HERE" method="post">`
3. Replace `YOUR_SHEET2API_ENDPOINT_URL_HERE` with the actual endpoint URL you copied from sheet2api

### 4. Form Functionality

The form has the following features:
- Submits data to Google Sheets via sheet2api
- Shows a thank you message on the same page after successful submission
- Provides a "Send Another Message" button to allow users to submit multiple messages
- Handles errors and displays appropriate messages

### 5. Testing the Form

1. Fill out the form on your website
2. Submit the form
3. You should see the thank you message appear on the same page
4. Check your Google Sheet to confirm the data was received
5. Click "Send Another Message" to test the form again

## Additional Configuration Options

- **Form Validation**: sheet2api provides additional validation options in their dashboard
- **Spam Protection**: Consider adding reCAPTCHA through sheet2api's integrations
- **Custom Styling**: You can modify the styling of the form and thank you message in the CSS

For more information, visit [sheet2api's documentation](https://sheet2api.com/website-form-to-google-sheets/). 