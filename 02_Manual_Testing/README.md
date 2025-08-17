# 02 – Manual Testing (BankApp)

This folder contains the manual test scenarios prepared for the BankApp application.  

## Transparency Note
All manual test cases listed here are **simulation-based** for portfolio purposes.  
There is **no real execution**; any Pass/Fail examples shown are illustrative.

### Relation to Test Plan
This section implements the approach described in **01_Test_Plan → 1.8 Assumptions & Limitations**,  
where all manual tests are defined as **simulation**.

## File
[Manual_Test_Scenarios_with_Status.xlsx](./Manual_Test_Scenarios_with_Status.xlsx)


## Covered Test Types
- Functional Tests  
- Positive and Negative Tests  
- Equivalence Partitioning  
- State Transition Testing  
- Load Testing  

## Number of Scenarios: 11

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

---

### Test Scenarios – BankApp (Simulation)

| Test ID | Test Scenario | Precondition | Steps | Expected Result | Test Type | Test Technique | Priority | Status | Execution Type |
|---------|---------------|--------------|-------|-----------------|-----------|----------------|----------|--------|----------------|
| TC01 | Login with valid credentials | User has a (dummy) valid account | 1. Open app <br> 2. Enter valid username & password <br> 3. Click Login | User is redirected to dashboard | Functional | Positive, Equivalence Partitioning | High | Not Executed (Simulation) | Simulation |
| TC02 | Login with invalid credentials | Dummy account exists | 1. Open app <br> 2. Enter valid email + wrong password <br> 3. Click Login | Error message is displayed | Functional | Negative, Equivalence Partitioning | High | Not Executed (Simulation) | Simulation |
| TC03 | Create new account | User is not registered | 1. Click “Sign Up” <br> 2. Enter details <br> 3. Submit | Account created successfully | Functional | Equivalence Partitioning | High | Not Executed (Simulation) | Simulation |
| TC04 | Transfer with sufficient balance | Balance ≥ amount | 1. Go to Transfer <br> 2. Select recipient <br> 3. Enter amount <br> 4. Confirm | Transfer succeeds | Functional | Positive, State Transition | High | Not Executed (Simulation) | Simulation |
| TC05 | Transfer with insufficient balance | Balance < amount | 1. Go to Transfer <br> 2. Enter higher amount <br> 3. Confirm | “Insufficient funds” error | Functional | Negative, Equivalence Partitioning | High | **Fail (Simulation)** | Simulation |
| TC06 | View account balance | User logged in | 1. Login <br> 2. Open “Balance” | Correct balance displayed | Functional | State Transition Testing | Medium | Not Executed (Simulation) | Simulation |
| TC07 | Logout from the system | User logged in | 1. Click “Logout” | Session ends; user redirected to login | Functional | Positive | Medium | Not Executed (Simulation) | Simulation |
| TC08 | Password reset with valid email | Registered email exists | 1. Click “Forgot Password” <br> 2. Enter valid email | Reset link is sent | Functional | Positive | Medium | **Fail (Simulation)** | Simulation |
| TC09 | Load test with 1000 users | N/A | 1. Simulate 1000 concurrent logins | System remains responsive | Non-functional | Load Testing | Medium | Not Executed (Simulation) | Simulation |
| TC10 | Session timeout after inactivity | User logged in | 1. Stay idle 15 min | Auto logout occurs | Functional | State Transition Testing | Low | **Fail (Simulation)** | Simulation |
| TC11 | Transfer with invalid recipient account number | User logged in, dummy account exists | 1. Go to Transfer <br> 2. Enter invalid recipient account number <br> 3. Enter amount <br> 4. Confirm | Error message: “Invalid account number” | Functional | Negative, Boundary Value | High | Not Executed (Simulation) | Simulation |

---

### Fail Summary
Out of 11 test scenarios, **3 scenarios failed** in simulation:  
- **TC05** – Transfer with insufficient balance  
- **TC08** – Password reset with valid email  
- **TC10** – Session timeout after inactivity  

The rest are **Not Executed (Simulation)**.  

---

**Note:** Defect reports generated from these scenarios will be presented in the **09_Bug_Reports** section of the portfolio.
