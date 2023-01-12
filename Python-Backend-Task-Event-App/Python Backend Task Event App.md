1. Following the Corva Dev Center Backend Getting Started and Python SDK documentation: 
   1. Create, develop, locally test and deploy a Python backend task time app: 
      1. +App: Backend→ On-Demand → App Name: Lab Task App → Segment: Drilling → Log Type: Time → Category: Analytics
   2. Create a dataset:
      1. Dataset Type: Time-Based
      2. Name: {provider}#lab-task-time-app
   3. In the manifest.json file, set “read”,”write” permissions for  {provider}#lab-task-time-app. 
   4. POST a payload from either Swagger or Postman that includes a {provider} asset_id, company_id, timestamp, provider, app_key, properties { "key1": "value1","key2": "value2" } object
   5. You decide on the key values to send in "properties": { }. 
   6. Get the required fields from the TaskEvent: `“properties”: { }` object
   7. Perform a simple calculation from the values of the `“properties”: { }` object
   8. Post the calculated values to {provider}#lab-task-time-app.
   9.  Test the POST request in the Corva Data API Swagger document or in Postman utilizing your company's API key or your Bearer Token
   10. Locally test the lambda function using the Pytest template within the app directory
   11. Zip up the app and deploy to the Dev Center
   12. Utilizing the App Runner feature, test the app on Production
   13. Confirm no errors in Log Files and that the data is being populated in the {provider}#lab-task-time-app dataset