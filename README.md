# azure-b2c-aurelia-example
Secure an Aurelia SPA with Azure Active Directory B2C / MSAL

**The explanation of the sample application / setup can be found [on this blog](https://chrisdennig.me/2017/09/06/secure-an-aurelia-single-page-app-with-azure-active-directory-b2c-msal/).**

If you want to run the example backend API with your own B2C directory, you have to adjust the following parameters in Backend/appsettings.json:

* AzureAdB2C:ClientId - the Application ID
* AzureAdB2C:Domain - the B2C domain name
* AzureAdB2C:SignUpSignInPolicyId - the SignUp or SignIn Policy

Furthermore, you also have to change the parameters in the settings.ts file in frontend/src:

* service - the base URI pointing to your API
* clientId - the Application ID from the B2C directory
* authority - authority setting for MSAL

Running the frontend application:

* got to the *frontend* directory
* run ´npm install -g aurelia-cli@latest´ (Aurelia Command Line Interface)
* run ´npm install´ (to install the project dependencies)
* run ´au run --watch´
* open your browser pointing to: http://localhost:9000
