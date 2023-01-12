1. Following the Corva Dev Center Backend Getting Started and Python SDK documentation: 
   1. Create, develop, locally test and deploy a Python backend stream time app: 
      1. +App: Backend→ Streaming → App Name: Lab Stream Time App → Segment: Drilling → Log Type: Time → Follow: Corva Drilling Enhanced Real-Time → Category: Analytics
   2. Create a dataset:
      1. Dataset Type: Time-Based
      2. Name: {provider}#lab-stream-time-app
   3. In the manifest.json file, set “read”,”write” permissions for  {provider}#lab-stream-time-app. 
   4. Get the following fields from the StreamTimeEvent: `“data.pump_spm_1”`, `“data.pump_spm_2”`
   5. Calculate the total pump_spm values of `data.pump_spm_1 + data.pump_spm_2`
   6. Post the calculated total pump_spm values to {provider}#lab-stream-time-app.
   7. Test the POST request in the Corva Data API Swagger document or in Postman utilizing your company's API key or your Bearer Token
   8. Locally test the lambda function using the Pytest template within the app directory
   9. Zip up the app and deploy to the Dev Center
   10. Utilizing the App Runner feature, test the app on Production
   11. Confirm no errors in Log Files and that the data is being populated in the {provider}#lab-stream-time-app dataset
