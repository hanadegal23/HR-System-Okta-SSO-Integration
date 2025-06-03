# Okta-SSO-Configuration-with-Salesforce
Login in to Salesforce
![1707506593286](https://github.com/user-attachments/assets/25a7450e-f187-4a3d-be61-c2b122a1ea8b)

Search App Manager
![Search App Manager Screenshot](https://github.com/user-attachments/assets/58f20c68-67dd-46f1-ab36-98f0315ad537)

Select "New Connected App"
![New Connected App](https://github.com/user-attachments/assets/e99aa720-1648-4bad-bd4b-432f6c6ca2a2)

Click Connected App
![Click contniue on connected app](https://github.com/user-attachments/assets/30f5a744-9d2e-4fe9-af4b-560c60f72140)

Continue New App Configuration- Fill out the application information seen below. For the callback URL use the one provided above and enable OAuth Settings.
![New Connected App configuration](https://github.com/user-attachments/assets/fc03eadd-3e65-4484-9cce-d939fc4f260f)
In the Select OAuth Scopes section, please select "Manage user data via APIs (api)" and "Perform requests at any time (refresh_token, offline_access)" and also DESELECT the "Require Proof Key for Code Exchange (PKCE)" option. Make sure it matches the setup below. 
![Continued Configuration screenshot](https://github.com/user-attachments/assets/63a0c477-f8c3-4f7b-95d2-9069f08560f5)

 After creating your new app, Go to API(Enable OAuth Setting) section -> Consumer Key and Secret -> Click Manage Consumer Details
![Manage Consumer Details Screenshot](https://github.com/user-attachments/assets/3f9c0b65-e74d-4827-ac7f-d71b040cb112)

 Copy the Consumer Key and Consumer Secret into a separate notepad. We will be using these two pieces of info. later in the lab. 
![Consumer Key Highlighted ScreenShot](https://github.com/user-attachments/assets/eae66514-2157-4c3a-a957-c229321d0012)


Go back to SalesForce main page -> Search for "My Domain" -> save the entire Current My Domain URL into a notepad. 
![My Domain URL Screenshot](https://github.com/user-attachments/assets/c4320d64-6ea7-4bd2-9f33-e8e38e91669a)

Have your Key, Secret, and Domain URL on a Notepad:
![image](https://github.com/user-attachments/assets/c94786f7-ce5e-4e93-8426-bfb0ab3d4901)


In Okta Admin Console go to Applications Tab -> Applications Sub-tab -> Click Browse App Catalog
![image](https://github.com/user-attachments/assets/74d9c7df-ca22-4ceb-aff2-68357e201199)

Click on SalesForce.com as seen below if its not there use the search bar to search for the SalesForce app. See Below.
![image](https://github.com/user-attachments/assets/c5ccbc28-8409-42cb-8179-13f8c3144dd1)

Once SalesForce.com is selected -> Click Add Integration**
![image](https://github.com/user-attachments/assets/779c6a5a-df86-461a-bfcd-6ed621bfdc76)

From your SalesForce Account -> Go to My Domain page -> copy the domain name INCLUDE .DEVELOP at the end  -> Paste it on the okta-side under Custom Domain (follow directions from the okta-side for custom domain). See Below
![image](https://github.com/user-attachments/assets/ae69fdbe-5673-49bd-8a3c-57520edcf66b)
![image](https://github.com/user-attachments/assets/4fcdd99e-6bff-4bba-8236-32f3e6b04994)

On Okta-side -> go to Sign-On options -> Select SAML
![image](https://github.com/user-attachments/assets/6c508961-2734-4536-923b-4ac9120d190c)

Go to your SalesForce Account -> Identity -> Single Sign-On Settings - Click Edit.
![image](https://github.com/user-attachments/assets/f13bea07-7a97-4114-bb3d-50efa7e5853b)

Click SAML Enabled and Save
![image](https://github.com/user-attachments/assets/bad001f0-0a79-4c84-86d7-9b08c28cdf05)

Go to your Okta instance -> under your SAML settings -> Metadata details -> Expand More Details
![image](https://github.com/user-attachments/assets/cad62abe-42e8-4438-88e2-3155774079a4)


On the Salesforce-side insert all the metadata details we got from the Okta-side. See below. Create any Name and API Name. Entity ID is your salesforce domain name (we saved the custom domain url in a notepad from when we created SalesForce acct.) with "https://" added in the beginning. See Below for reference. 
![image](https://github.com/user-attachments/assets/957d9cde-5e3c-476d-ada2-4208b97dcdbb)


On the SalesForce-side -> Click Save once all the details have been copied from Okta properly. Go to Okta and scroll down to see the Advanced Sign-On Settings. Copy the Login Url and Logout URL from Salesforce-side to the Okta-Side. The Login Url and Logout URL from Salesforce-side will get generated once you save all the details we have copied from Okta from previous step.
![image](https://github.com/user-attachments/assets/759c1b82-2e76-47a4-9799-6f43d6361f1f)

On the Okta-side -> Click Done. SalesForce Integration with Okta has been setup BUT NOT COMPLETED!!
![image](https://github.com/user-attachments/assets/2484305e-2a4a-47d5-90aa-0a53f0f3f9ef)

For Reference, these configurations were done on the SP-side (SalesForce) when integrating with Okta.
![image](https://github.com/user-attachments/assets/157da1c3-81ab-492d-acbf-2238aac426a7)

Go to Okta -> Applications Tab -> Applications sub-tab -> You should see SalesForce.com as an option and select it. -> Select Provisioning tab under Salesforce.com app -> Click Configure API Integration.
![1707511488167](https://github.com/user-attachments/assets/4a657b9f-6d4f-4419-ab05-e0140d2a9621)

Click Enable API Integration -> Copy and Past your Key and Secret from SalesForce into Okta -> Click Authenticate with Salesforce.com 
![1707511587156](https://github.com/user-attachments/assets/e56f8186-2f20-4acd-b40a-20a34c71dc0b)

You will get a pop-up window with salesforce login page -> Insert your login credentials and Log In
![image](https://github.com/user-attachments/assets/868184b5-603f-4d81-a56b-ffb37c25933a)


Once Salesforce verifies successfully -> Click Done
![image](https://github.com/user-attachments/assets/33d32592-be61-4804-b319-93f3ca81f815)

In the Provisioning tab for Salesforce -> Click Edit
![1707511871427](https://github.com/user-attachments/assets/83dcf3a5-9185-400d-8ce9-1f16a55ef9bc)

Enable the following options: Create Users, Update User Attributes, Delete Users -> Click Save 
![1707511910131](https://github.com/user-attachments/assets/284893b9-b90a-419f-8dfb-9aa82aa7504e)


