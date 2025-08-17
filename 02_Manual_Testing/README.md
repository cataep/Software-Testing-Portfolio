# 02 – Manual Testing (BankApp)

This folder contains the manual test scenarios prepared for the BankApp application.  
## Transparency Note
All manual test cases listed here are **simulation-based** for portfolio purposes.  
There is **no real execution**; any Pass/Fail examples shown are illustrative.

### Relation to Test Plan
This section implements the approach described in **01_Test_Plan → 1.8 Assumptions & Limitations**, where all manual tests are defined as **simulation**.


## File
- [→ Test_Scenarios.xlsx](./Test_Scenarios.xlsx)

## Covered Test Types
- Functional Tests  
- Positive and Negative Tests  
- Equivalence Partitioning  
- State Transition Testing  

## Number of Scenarios: 10

Each test scenario includes the following information:  
- Test ID  
- Test Scenario  
- Preconditions  
- Steps  
- Expected Result  
- Test Type  
- Test Technique  
- Status
- Priority
- Execution Type

> These test scenarios are based on ISTQB test design techniques and created for portfolio purposes.
>
# Test Scenarios – BankApp  

Some of these scenarios were actually executed on the application (Real), while others were prepared as simulations (Simulation) for portfolio purposes. This approach demonstrates both real-world testing experience and the application of different ISTQB-aligned test design techniques.  

| Test ID | Test Scenario | Precondition | Steps | Expected Result | Test Type | Test Technique | Priority | Status | Execution Type |
|---------|---------------|--------------|-------|-----------------|-----------|----------------|----------|--------|----------------|
| TC01 | Login with valid credentials | User has a valid account | 1. Open app <br> 2. Enter valid username & password <br> 3. Click login | User is successfully logged in | Functional | Positive | High | Not Executed | Real |
| TC02 | Login with invalid credentials | User has a valid account | 1. Open app <br> 2. Enter wrong password <br> 3. Click login | Error message is displayed | Functional | Negative | High | Not Executed | Real |
| TC03 | Create new account | User is not registered | 1. Open app <br> 2. Click “Sign Up” <br> 3. Enter details <br> 4. Submit | New account is created | Functional | Equivalence Partitioning | High | Not Executed | Real |
| TC04 | Transfer money with sufficient balance | User has balance ≥ transfer amount | 1. Login <br> 2. Go to Transfer <br> 3. Enter amount <br> 4. Confirm | Transfer is successful | Functional | Positive | Medium | Not Executed | Real |
| TC05 | Transfer money with insufficient balance | User balance < transfer amount | 1. Login <br> 2. Go to Transfer <br> 3. Enter higher amount <br> 4. Confirm | Error message: insufficient funds | Functional | Negative | Medium | Not Executed | Real |
| TC06 | View account balance | User has logged in | 1. Login <br> 2. Click “Balance” | Account balance is displayed correctly | Functional | State Transition Testing | Medium | Not Executed | Real |
| TC07 | Logout from the system | User is logged in | 1. Login <br> 2. Click “Logout” | User is logged out, session ends | Functional | Positive | Low | Not Executed | Real |
| TC08 | Password reset with valid email | User has a registered email | 1. Open app <br> 2. Click “Forgot Password” <br> 3. Enter valid email | Reset link is sent | Functional | Positive | High | Not Executed | Real |
| TC09 | Load test with 1000 users | Test environment prepared | 1. Simulate 1000 users logging in simultaneously | System performance under load | Non-functional | Load Testing | Medium | Not Executed | Simulation |
| TC10 | Session timeout after inactivity | User is logged in | 1. Login <br> 2. Stay inactive <br> 3. Wait 15 min | System logs user out automatically | Functional | State Transition Testing | Low | Not Executed | Simulation |

---


 Note: Defect reports generated from these scenarios will be presented in the **09_Bug_Reports** section of the portfolio.
