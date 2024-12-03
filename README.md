# demoISGeneric
demo to show a basic IS capabilities:
- Appications and Connections
- Authentication (simple, MFA, conditional)
- User management and user portal
## Pre requisites
1. Install IS (7.0 is used currently)
2. Set up the PetCare App
   - download the IAM tutorial (https://github.com/wso2con2024/iam-tutorial/tree/main)
   -  run the App (npm start)
   -  Create the PetCare App in IS (with default Login flow)
3. Create Google connection
   - an account in the Google Developer Console is needed
4. enable TOTP with Goofle Authenticator (or any other authenticator)
## Use Cases
### Create a SPA App and show Authentication
1. Show the main apps you can create. Create a Single Page App. Go through the different tabs
2. Show the Connections
3. Show the pre built App PetCare
4. Execute different log in use cases
   - Simple U/P
      - Go to the login flow and show the default
      - Open a browser tab and go to localhost:3000
      - Login with user name and pwd (StefanoIS/****)
   - U/P + social login (Google)
      - Go to the login flow and add Google as log in option
      - Open a browser tab and go to localhost:3000
      - Login with Google (stene19692@gmail.com/****)
  - 2FA
      - Go to the login flow and add TOTP as second step
      - Open a browser tab and go to localhost:3000
      - Login u/p (StefanoIS/****)
      - Complete the 2nd step authentication
  - Conditional authentication
     - Go to the login flow and enable conditional authentication
     - Go to the predefined flows/conditional login flow and add 'IP based'
        - explain what it does, click over the info label
        - modify the script, adding 127.0.0.1 in the list of corporate network: var corpNetwork = ['192.168.1.0/24', '10.100.0.0/16', 127.0.0.1/1]; update
     - Open a browser tab and go to localhost:3000
     - Login with u/p (StefanoIS/****)
     - 2nd step authentication doesn't occur

