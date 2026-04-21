# API TESTING
1. Verify body output.
2. Verify status code
3. Verify repeated generation of users
4. Verify Get for a specific user using the seed information. i.e randomuser.me/api/?seed=b4fc9867c4df19fe
5. Update info 
6. 


200 - OK - Confirms successful generation of a user.


### Bonus:
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Returned data is an array", function () {
    let jsonData = pm.response.json();
    pm.expect(Array.isArray(jsonData)).to.eql(false);
});

# CODING TASK

# UI TESTING
- Login with correct email and password
- Validaation of Email field
- Login with incorrect password
- Login with incorrect email
- Login with no credentials/expired credentials

3. User is able to login with an expired or password that was previously changed.
Login button does not respond when clicked
No validation occurs, users can login with any user.

## Bonus


# 4. BUG REPORT
 Title: Login button does not respond when trying to login.
 Description: When the login button is clicked, nothing happens despite email and password fields being field.
 Expected Result: When click, the login button should be responsive and user is navigated to the homepage.
 Actual Result: Nothing happens when the login button is clicked.
 Environment Used: iphone 16 Pro Max, iOS 26
 App Version: 1.9.8
 Attachments: --Attach logs, screenshots, videos and device information --


## SIT QUESTION
### Root Cause Analysis:
- I would validate that the amounts in the transaction query match the postings on the core banking system including charges. I would then validate from the db the specific transaction and validate it is reflecting correctly. Once EOD reconciliation is complete, I would review the logs to confirm that the transaction was reflected correctly.

## Specific checks to perform
- Verify charges on transactions and commisions are well calaculated in the core banking system.
- Database checks to verify that the transactions made are accurately captured in the database.
- Validate the calculation of transactions during reconciliation.