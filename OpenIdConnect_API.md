Use this API to retrieve the subscriber's identity information.  
The API format is: http://52.28.29.68:1081/rest/OpenIdConnect/v1/userinfo?ownerId={userId}

This API need to involve the Oauth authorization code flow to exchange token, so to user the API, Oauth flow is needed.  

To test the API, follow the following procedure to get the Oauth Token:

Step 1: Open http://52.28.29.68:1082/oauth2/playground/

Step 2: Set the Client drop down to "ESIF_Identity_OAUTH_APP"

Step 3: Select the Scopes you want to access

Step 4: Set the redirect URL to: http://52.28.29.68:1082/oauth2/playground/callback/ESIF_Identity_OAUTH_APP

Step 5: Click the "Send Authorization Request" button

Step 6: Simulate the user login (use username/password: usera/usera) and authorization process

Step 7: Click "Exchange Token"

Step 8: Copy the token in the "Token validation" section and put it into the Authorization Bear and test the API 
