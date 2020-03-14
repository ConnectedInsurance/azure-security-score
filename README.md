#Azure Secure Scores

To run the completed project in this folder, you need the following:
1) Node.js installed on your development machine. If you do not have Node.js, visit the previous link for download options. (Note: This tutorial was written with Node version 12 The steps in this guide may work with other versions, but that has not been tested.) 

2) Either a personal Microsoft account with a mailbox on Outlook.com, or a Microsoft work or school account.

If you don't have a Microsoft account, there are a couple of options to get a free account:
1) You can [sign up for a new personal Microsoft account](https://signup.live.com/signup?wa=wsignin1.0&rpsnv=12&ct=1454618383&rver=6.4.6456.0&wp=MBI_SSL_SHARED&wreply=https://mail.live.com/default.aspx&id=64855&cbcxt=mai&bk=1454618383&uiflavor=web&uaid=b213a65b4fdc484382b6622b3ecaa547&mkt=E-US&lc=1033&lic=1)
2) You can [sign up for the Office 365 Developer Program](https://developer.microsoft.com/office/dev-program) to get a free Office 365 subscription.


##Prerequisites
Please follow following steps to configure web app.
1) Open a browser and navigate to the Azure [Active Directory admin center](https://aad.portal.azure.com/). Login using a personal account (aka: Microsoft Account) or Work or School Account.

2) Select Azure Active Directory in the left-hand navigation, then select App registrations under Manage.
   ![step2]
3) Select New registration. On the Register an application page, set the values as follows.
   
   3a. Set Name. 
   
   3b. Set Supported account types to Accounts in any organizational directory.
   
   3c. Under Redirect URI, set the first drop-down to Web and set the value to http://localhost:3000/auth/callback.
    
4) Select Register. On the Node.js Graph Tutorial page, copy the value of the Application (client) ID and save it, you will need it in the next step.
    ![step4]
5) Select Authentication under Manage. Locate the Implicit grant section and enable ID tokens. Select Save.
    ![step5]
6) Select Certificates & secrets under Manage. Select the New client secret button. Enter a value in Description and select one of the options for Expires and select Add.
   ![step6]
7) Copy the client secret value before you leave this page. You will need it in the next step.

##Configure the Node App


1) Rename the .env.example file to .env.

2) Edit the .env file and make the following changes.
3) Replace YOUR_APP_ID_HERE with the Application Id you got from the App Registration Portal (step # 4 in Prerequisites).
4) Replace YOUR_APP_PASSWORD_HERE with the password you got from the App Registration Portal (step # 7 in Prerequisites).
5) In your command-line interface (CLI), navigate to this directory and run the following command to install requirements.

`npm install
`

## Run 
1) Run the following command in your CLI to start the application.
`npm start`

2) Open a browser and browse to http://localhost:3000

---
###NginX
nginx sample configuration can be found in **nginx-sample**.

####Having any problem with following above steps?
Please dont hesitate to contact me at msmanzoor91@gmail.com


[step2]: https://docs.microsoft.com/en-us/graph/tutorials/node/tutorial/images/aad-portal-app-registrations.png
[step4]: https://docs.microsoft.com/en-us/graph/tutorials/node/tutorial/images/aad-application-id.png 
[step5]: https://docs.microsoft.com/en-us/graph/tutorials/node/tutorial/images/aad-implicit-grant.png
[step6]: https://docs.microsoft.com/en-us/graph/tutorials/node/tutorial/images/aad-new-client-secret.png
