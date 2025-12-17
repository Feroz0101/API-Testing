# Student API Testing using Postman & Newman

This repository provides a complete example of **API testing automation** using **Postman** and **Newman**.  
It explains how to execute API tests in Postman and how to generate **HTML API test reports** using Newman from the command line.

---

## Project Description

- REST API testing for Student Management APIs
- Test cases written in Postman
- Automated execution using Newman
- HTML test report generation using Newman Reporter
- Suitable for beginners and CI/CD integration

---

## API Details

### Base URL: https://thetestingworldapi.com/

### APIs Tested
- Create Student
- Get All Students
- Get Student by ID
- Create Technical Skills
- Create Student Address
- Get Final Student Details

---

## Tools Used

| Tool | Purpose |
|-----|--------|
| Postman | API testing & assertions |
| Node.js | Required for Newman |
| Newman | CLI runner for Postman |
| Newman HTML Extra Reporter | HTML test reports |

---

## Running API Tests in Postman

### Step 1: Import Collection & Environment
1. Open **Postman**
2. Click **Import**
3. Import:
   - `Student API testing.postman_collection.json`
   - `Student ENV.postman_environment.json`

### Step 2: Select Environment
- Select **Student ENV** from the environment dropdown

### Step 3: Run API Manually
- Open any request
- Click **Send**
- Validate:
  - Status Code
  - Response Body
  - Test Assertions

### Step 4: Run Collection using Collection Runner
1. Click the collection name
2. Click **Run Collection**
3. Choose environment: `Student ENV`
4. Click **Run**

---

## Sample Postman Test Script

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Response time is less than 1000ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(1000);
});


