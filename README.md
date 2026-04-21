# 1 API TESTING
1. Verify body output.
Verify the response body matches the correct format output with all required fields displayed.
2. Verify status code:
 Verify that correct status code is returned when request is sent.
3. Verify repeated generation of users
Verify user is able to make repeated API calls without any error being experienced.
4. Verify Get for a specific user 
Verify user is able to make api call for specific users using the seed info. i.e make a call with the seed parameters i.e randomuser.me/api/?seed=b4fc9867c4df19fe
5. Validate filtering of  results using unsupported queries 
Verify an error is displayed when trying to filter users using an unsupported query type e.g for gender, use special characters
6. Verify status output using a malformed request
Verify user is unable to send a request using a malformed request.


### expected status codes
200 - OK - Confirms successful generation of a user.
404 - NOT FOUND Confirms the request made could not be found due to possible malformed endpoint or connection to the endpoint.
401 - request without auth or with invalid token.
403 - Request with valid auth but no permission.
400 - Invalid JSON or wrong content type.

### validation points
- Response body 
- Reponse time
- Status codes
- Response size
- Request size

### Bonus:
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Returned data is an array", function () {
    let jsonData = pm.response.json();
    pm.expect(Array.isArray(jsonData)).to.eql(false);
});

# 2 CODING TASK



# 3 UI TESTING
 #### Testcase ID: TC001
 Title: Verify User can login with correct credentials.
 Steps:
 - Access the app
 - input the correct email
 - input correct password.
 - Clic on login

 Expected result:
 User is able to login to the app and homepage is displayed

 Actual result:

 #### Testcase ID: TC002
Title: verify validation of Email field
Steps:
 - Access the app
 - input the correct email
 - 

Expected Result: Email is validated correctly and no error is displayed.

Actual Result:

 #### Testcase ID: TC003
 Title: Login with incorrect password
 Steps:
 - Access the app
 - input the correct email
 - Enter incorrect password
 - Click on login button

Expected Result: An error ndicating that email/password is displayed. User is asked to try log in again.

Actual Result:

 #### Testcase ID: TC004
 Title: Login with incorrect email
 Steps:
 - Access the app
 - input the incorrect email
 - Enter correct password 
 - Click on login

Expected Result: An error ndicating that email/password is displayed. User is asked to try log in again

Actual Result:

 #### Testcase ID: TC005
 Title: Login with no credentials/expired credentials
 Steps:
 - Access the app
 - Click on login button

Expected Result: An error ndicating that email/password is displayed. User is asked to try log in again

Actual Result:

### Possible bugs
3. User is able to login with an expired or password that was previously changed.
Login button does not respond when clicked
No validation occurs, users can login with any user.

## Bonus


# 4. BUG REPORT
 Bug ID: BUG001
 Title: Login button does not respond when trying to login.
 Description: When the login button is clicked, nothing happens despite email and password fields being field.
 Steps to reproduce:
  - Access he url
  - input correct email and password
  - Click on the login button
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