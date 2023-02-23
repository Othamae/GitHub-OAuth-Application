# To register an OAuth application in GitHub

1. Navigate to your GitHub “Settings” page by clicking on your GitHub icon.

2. Select “Developer settings” in the sidebar.

3. Select “OAuth Apps” in the sidebar of the Developer settings page. Click on the “Register a new application” button.

4. Fill out the form with the following information:

   - Application Name: OAuth Project (or any name for your project)
   - Homepage URL: http://localhost:3000
   - Authorization Callback URL: http://localhost:3000/auth/github/callback

5. Click “Register application”.

6. Take note of the Client ID. Click on “Generate a new client secret” to generate a Client secret. Copy both your Client ID and the Client Secret and paste them into the `.env` file. 

_Note that the secret key is displayed only once—when you navigate away from the GitHub page, you will no longer be able to see the Client Secret._


