# HR-System-Okta-SSO-Integration
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



