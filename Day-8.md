# 📘 Day 8/100 – GET vs POST vs PUT vs PATCH vs DELETE

Before we jump into today's topic...

## 🏆 Yesterday's Challenge Answer

The correct answer was **C: A combination of Real-Time, Batch & Event-Driven**.

> Different business processes have different needs. There is no one-size-fits-all integration pattern!

---

## 🤔 Why Do APIs Have GET, POST, PUT, PATCH, and DELETE?

Each HTTP method has a specific, well-defined purpose in API communication.

| Method | What It Does | Salesforce Example |
| :--- | :--- | :--- |
| **GET** | Retrieve data | Get Account details |
| **POST** | Create new data | Create a Lead |
| **PUT** | Replace an entire record | Replace all Contact details |
| **PATCH** | Update specific fields | Update only Email or Phone |
| **DELETE** | Remove data | Delete a temporary record |

---

## 💻 Mini Practical

Imagine you need to update **only a customer's phone number**. Which method would you choose?

* ❌ **PUT**
* ✅ **PATCH**

> **Why?** Because you're updating only one specific field, not replacing the entire record structure!

---

## 💼 Real Project Insight

In one of my projects, Salesforce updated only the **Customer Status** and **Credit Limit** in **Microsoft Dynamics 365 Business Central**.

Instead of sending the complete customer record every time, we used **PATCH** to update only the changed fields.

> **Result:** Reduced payload size, improved performance, and avoided unnecessary field updates.

---

## 🧠 Architect's Tip

> **Don't use POST for everything.**

Choosing the correct HTTP method makes your APIs significantly easier to understand, maintain, and integrate with external systems.

---

## ⚠️ Common Mistake

A common mistake is using **PUT** when you only need to update one or two fields.

If the external API supports **PATCH**, always use it for partial updates.

---

## 📖 Integration Term of the Day

> **HTTP Method**  
> An action verb that explicitly tells an API what operation you want to perform—such as retrieve, create, update, or delete data.

---

## 🧪 Try It Yourself

If you've used Postman, answer this:  
**Which HTTP method have you used the most?**

* 🟢 **GET**
* 🔵 **POST**
* 🟠 **PATCH**
* 🔴 **PUT**

💬 *Let me know in the comments!*

---

## 📅 Next Chapter

**What are HTTP Status Codes?**  
`200`, `201`, `400`, `401`, `403`, `404`, `500`... What do they actually mean?

---

## 🏷️ Tags

`#Salesforce` `#SalesforceDeveloper` `#SalesforceIntegration` `#RESTAPI` `#HTTP` `#Apex` `#DeveloperCommunity` `#IntegrationMasterySeries`

<img width="753" height="898" alt="SALESFORCE INTEGRATION HANDBOOK" src="https://github.com/user-attachments/assets/5ff4dd7b-cddd-4629-b6d2-11d2eccda0ce" />
