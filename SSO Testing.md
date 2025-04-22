SSO Testing- IdP initiated flow and SP initiated flow


IdP Initiated Flow Testing:
Step 1. Go to Okta -> Directory -> People -> Click Add Person -> Create new user and activate them 
![image](https://github.com/user-attachments/assets/c4d2e72d-277b-4623-8acc-0d76d90534ba)

Step 2. Got to Applications tab -> Applications sub-tab -> Click Salesforce.com
![1707512467880](https://github.com/user-attachments/assets/9278a5c3-e2dd-4953-aec5-dc2acc22326e)

Step 3. Go to Assignments -> Assign -> Assign to People
![1707512221346](https://github.com/user-attachments/assets/596a33f5-0d54-49c9-8607-eb35f0793ba7)

Step 4. Find newly created user -> Click Assign
![image](https://github.com/user-attachments/assets/8ade1646-2a17-43a6-acf6-ce70fac76dc6)

Step 5a. When Assigning user make this change: the Profile URL = Chatter Free User 
![image](https://github.com/user-attachments/assets/61af9849-8729-42df-a138-14111413a24a)

Step 5b. When Assigning user make this change: Role = No Role

![image](https://github.com/user-attachments/assets/1aedcda8-1531-4525-841b-4215594ca9be)

Step 6. Click Save and the User should show up under Assignments 
![image](https://github.com/user-attachments/assets/acc3dc02-0350-4774-87c3-03687f67b802)

Step 7. Go to Salesforce.com and login with your credentials -> Go to Administration -> Users tab  -> Users sub-tab -> make sure the new user was synced to salesforce.com with all the credentials from okta. **
![image](https://github.com/user-attachments/assets/3126d4bd-ba45-4483-aa67-e0c70370fd2d)

Step 8a. Go to user Dashboard (Not Admin) -> login using the new user credentials
![image](https://github.com/user-attachments/assets/e9e6f0fe-e423-4c6d-960f-6984d196e1d8)

Step 8b. After logging in, you should see the salesforce.com tile on the dashboard under My Apps
![image](https://github.com/user-attachments/assets/941c888a-e4ee-4f8a-9c70-37aebe3aec3d)

Step 9. Click on the Salesforce tile -> click Launch App on the side panel
![image](https://github.com/user-attachments/assets/52c8b5a9-c199-4be8-9acc-68da64647434)


Step 10. You will now be logged into the Salesforce Instance automatically. You should see the starting page as seen below.
![image](https://github.com/user-attachments/assets/e24db6e6-97c3-4130-bfbb-036872e9634c)

