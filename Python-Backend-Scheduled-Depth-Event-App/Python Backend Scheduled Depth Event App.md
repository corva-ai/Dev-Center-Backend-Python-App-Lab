1. Following the Corva Dev Center Backend Getting Started and Python SDK documentation: 
   1. Create, develop, locally test and deploy a Python backend scheduled depth app: 
      1. +App: Backend→ Scheduler → App Name: Lab Scheduled Depth App → Segment: Drilling → Log Type: Depth → Scheduler Type: Data Depth → Follow: Drilling Enhanced Real-Time Depth→ Category: Analytics
   2. Create a dataset:
      1. Dataset Type: Depth-Based
      2. Name: {provider}#lab-scheduled-depth-app
   3. In the manifest.json file, set “read”,”write” permissions for  {provider}#lab-scheduled-depth-app. 
   4. In the manifest.json file, set the `“app.depth_milestone”: 5 `
   5. Perform a GET request to `corva#drilling.wits.depth` for the following value: `“data.dep`
   6. Import the Python statistics library into the app: `import statistics`
   7. Calculate the mean value of the 5 minutes of the "data.dep" data e.g. `mean_dep = statistics.mean(record.get("data", {}).get("dep", 0)`
   8. POST the calculated `"data.mean_dep"` value to {provider}#lab-scheduled-depth-app.
   9. Test the GET and POST request in the Corva Data API Swagger document or in Postman utilizing your company's API key or your Bearer Token
   10. Locally test the lambda function using the Pytest template within the app directory
   11. Zip up the app and deploy to the Dev Center
   12. Utilizing the App Runner feature, test the app on Production
   13. Confirm no errors in Log Files and that the data is being populated in the {provider}#lab-scheduled-depth-app dataset