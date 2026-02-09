# Postman API Demo – AutomationExercise

This repository contains Postman collections for API testing of the **AutomationExercise demo e-commerce application**.  
It demonstrates real-world API testing scenarios, covering products, brands, user accounts, and authentication.

All requests are based on publicly available endpoints from [AutomationExercise](https://automationexercise.com/), mirroring the manual and UI tests in my QA portfolio.

---

## 🧭 What This Project Demonstrates
- Writing structured API requests in Postman  
- Handling GET, POST, PUT, DELETE requests  
- Validating status codes, response messages, and JSON structure  
- Testing positive and negative scenarios (valid/invalid requests)  
- Using environment variables for dynamic endpoints and data  
- Running collections with Postman or Newman for CI/CD  

---

## 📂 API Coverage

### **Products**
1. **Get All Products List** – `GET /api/productsList` → 200, list of all products  
2. **POST To All Products List** – `POST /api/productsList` → 405, method not allowed  
3. **Search Product (Valid)** – `POST /api/searchProduct` → 200, search results  
4. **Search Product (Missing Parameter)** – `POST /api/searchProduct` → 400, bad request  

### **Brands**
5. **Get All Brands List** – `GET /api/brandsList` → 200, list of all brands  
6. **PUT To All Brands List** – `PUT /api/brandsList` → 405, method not allowed  

### **User Authentication**
7. **Verify Login (Valid Details)** – `POST /api/verifyLogin` → 200, user exists  
8. **Verify Login (Missing Email)** – `POST /api/verifyLogin` → 400, bad request  
9. **Verify Login (Invalid Details)** – `POST /api/verifyLogin` → 404, user not found  
10. **DELETE /api/verifyLogin** → 405, method not allowed  

### **User Account Management**
11. **Create/Register User** – `POST /api/createAccount` → 201, user created  
12. **Update User Account** – `PUT /api/updateAccount` → 200, user updated  
13. **Delete User Account** – `DELETE /api/deleteAccount` → 200, account deleted  
14. **Get User Detail by Email** – `GET /api/getUserDetailByEmail` → 200, user details  

---

## ⚡ How to Use

1. Import the collections from the `collections/` folder into Postman.  
2. Import the environment file from `environments/` (base URL, email, and password variables included).  
3. Run requests individually or as a collection.  
4. Optional: use [Newman](https://www.npmjs.com/package/newman) to run collections in CI/CD pipelines and generate reports.  

---

## 📝 Key Features

- Structured request folders and naming conventions  
- Environment variables for base URL, credentials, and dynamic test data  
- Test scripts for validating response codes, body content, and headers  
- Positive and negative scenario coverage  
- Easy to extend for new APIs or automated CI execution  

---

## 📂 References

- [AutomationExercise API Docs](https://automationexercise.com/)  
- [Postman Documentation](https://learning.postman.com/docs/)  
