# API Testing with Postman – Reqres Demo

This folder demonstrates API testing performed on the [Reqres](https://reqres.in/) demo API using Postman.

---

## Files in This Folder

- **API_Test_Scenarios.xlsx** → Test cases in Excel format  
- **API Testing-Reqres.postman_collection.json** → Postman collection  
- **API Testing-Reqres.postman_test_run.json** → Postman Runner execution result  
- **README.md** → Documentation  

---

## Test Scenarios

Prepared in **Excel** (`API_Test_Scenarios.xlsx`):

1. **GET Users** – Verify user list retrieval.(Executed ) 
2. **POST Login Successful** – Verify login with valid credentials.(Executed)  
3. **POST Login Unsuccessful (Missing Password)** – Verify login failure when the password is missing.(Executed)
4. **POST Create User** – *Planned (not implemented)*  
5. **PUT Update User** – *Planned (not implemented)*  
6. **DELETE User** – *Planned (not implemented)*  

---

## Tools & Setup

- **Postman** → for request creation and execution  
- **Excel** → for test scenario design and documentation  

> No Postman environment was used – requests are configured directly in the collection.

---

## How to Run

1. Open **Postman**.  
2. Import `API Testing-Reqres.postman_collection.json`.  
3. Run the collection manually or via **Collection Runner**.  
4. Check execution results in:  
   `API Testing-Reqres.postman_test_run.json`

---

## Notes

- Only the **first three test scenarios** were executed.  
- The remaining scenarios are listed for documentation purposes.  
- Excel file provides the link between test design and execution.  

---
