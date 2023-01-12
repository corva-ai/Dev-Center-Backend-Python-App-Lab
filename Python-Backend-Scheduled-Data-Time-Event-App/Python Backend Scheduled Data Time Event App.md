1. Following the Corva Dev Center Backend Getting Started and Python SDK documentation: 
   1. Create, develop, locally test and deploy a Python backend scheduled data time app: 
      1. +App: Backend→ Streaming → App Name: Lab Scheduled Data Time App → Segment: Drilling → Log Type: Time → Scheduler Type: Data Time → Follow: Corva Drilling Enhanced Real-Time → Category: Analytics
   2. Create a dataset:
      1. Dataset Type: Time-Based
      2. Name: {provider}#lab-scheduled-data-time-app
   3. In the manifest.json file, set “read”,”write” permissions for  {provider}#lab-scheduled-data-time-app. 
   4. In the manifest.json file, set the `“app.cron_string”: “/5 * * * *”`
   5. Perform a GET request to `corva#wits` for the following value: “data.rop”
   6. Import the Python statistics library into the app: `import statistics`
   7. Calculate the mean value of the 5 minutes of the "data.rop" data e.g. `mean_rop = statistics.mean(record.get("data", {}).get("rop", 0)`
   8. POST the calculated `"data.mean_rop"` value to {provider}#lab-scheduled-data-time-app.
   9. Test the GET and POST request in the Corva Data API Swagger document or in Postman utilizing your company's API key or your Bearer Token
   10. Locally test the lambda function using the Pytest template within the app directory
   11. Zip up the app and deploy to the Dev Center
   12. Utilizing the App Runner feature, test the app on Production
   13. Confirm no errors in Log Files and that the data is being populated in the {provider}#lab-scheduled-data-time-app dataset