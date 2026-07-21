# 📘 Day 9/100 – Your API Didn't Fail... The Status Code Told You Why!

One of the first things I check when an integration fails isn't the Apex code...

> 👉 **It's the HTTP Status Code.**

That one number often tells you exactly where to start debugging.

---

## 📊 HTTP Status Code Cheat Sheet

| Code | Status | Meaning |
| :---: | :--- | :--- |
| 🟢 | **200 OK** | Request was successful. |
| 🟢 | **201 Created** | A new record was created successfully. |
| 🟡 | **400 Bad Request** | The request is invalid (missing required fields, wrong JSON syntax, etc.). |
| 🔒 | **401 Unauthorized** | Authentication failed or token is invalid/expired. |
| 🚫 | **403 Forbidden** | You're authenticated, but don't have permission to access the resource. |
| ❓ | **404 Not Found** | The API endpoint URL doesn't exist or record wasn't found. |
| 🔴 | **500 Internal Server Error** | Something failed on the destination server. |

---

## 💻 Mini Practical

Imagine your Apex callout returns: `HTTP/1.1 401 Unauthorized`

Should you debug your Apex business logic first?

* ❌ **No.**

The first things to check are:
* ✅ **Access Token**
* ✅ **Named Credential configuration**
* ✅ **OAuth/Authentication setup**

> The status code already tells you the precise root domain of the issue!

---

## 💼 Real Project Insight

In one of our integrations, everything looked correct—the endpoint, payload format, and Apex code logic.

However, the API kept returning **401 Unauthorized**.

After troubleshooting, we found that the **OAuth access token had expired**. Refreshing the token resolved the issue immediately.

> **Key takeaway:** Sometimes the problem isn't your code—it's the authentication flow.

---

## 🧠 Architect's Tip

> **Always log both the HTTP Status Code and the Response Body.**

Never log a generic error like:  
❌ `Callout Failed`

Instead, log structured details:  
✅ `Status Code: 401 | Response: Unauthorized`

Good, descriptive logs reduce debugging time dramatically!

---

## ⚠️ Common Mistake

Many developers see a **500 Internal Server Error** and immediately start refactoring their Apex code.

In reality, a `500` status indicates that the error occurred **inside the external system**, not in Salesforce. Always read the response body or check the external system logs before touching your code.

---

## 📖 Integration Term of the Day

> **HTTP Status Code**  
> A standard numeric response code sent by a server that tells you whether your API request succeeded or failed—and gives key details as to why.

---

## 🧪 Quick Challenge

You're getting: **403 Forbidden**

**What would you check first?**

💬 *Share your answer in the comments!*

---

## 📅 Next Chapter

**Headers Explained – What are Authorization, Content-Type, Accept, and why are they so important?**

---

## 🏷️ Tags

`#Salesforce` `#SalesforceDeveloper` `#SalesforceIntegration` `#RESTAPI` `#HTTP` `#NamedCredentials` `#Apex` `#DeveloperCommunity` `#IntegrationMasterySeries`

<img width="753" height="900" alt="SALESFORCE INTEGRATION HANDBOOK" src="https://github.com/user-attachments/assets/54323e22-d09f-4b6b-8ec2-03c0312fc62b" />
