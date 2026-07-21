# 📘 Day 10/100 – HTTP Headers: The Invisible Part of Every API Call

When an API fails, developers often check:
* ✅ **Endpoint**
* ✅ **Payload**
* ✅ **Apex Code**

But they forget one crucial component...

> 👉 **HTTP Headers**

Headers explicitly tell the receiving system **how to interpret and process your request**. Without the correct headers, an API server may reject your request—even if your Apex code and payload are otherwise flawless.

---

## 💻 Mini Practical

Here's an example of a real HTTP request structure:

```http
POST /customers HTTP/1.1
Host: api.example.com
Content-Type: application/json
Authorization: Bearer eyJhbGciOi...
Accept: application/json
```
🔍 Breakdown of Key Headers:
📦 Content-Type: application/json ──► "The body of data I'm sending to you is formatted as JSON."

🔐 Authorization: Bearer <token> ──► "Here is my access token to prove my identity and permissions."

📥 Accept: application/json ──► "I expect you to send the response back in JSON format."

Simple, but absolutely essential for successful API communication!

💼 Production Lesson
In one of my previous projects, our payload structure was accurate, the endpoint URL was correct, and authentication credentials were valid...

Yet every single request was rejected!

The reason?

We forgot to include the Content-Type: application/json header in our Apex HTTP request. The target API expected JSON, but without that header, it didn't know how to parse the incoming body.

One missing header line caused hours of unnecessary debugging! 😅

🧠 Architect's Tip
Whenever an API integration isn't behaving as expected, verify these three elements first:

✔️ Headers

✔️ Payload

✔️ Status Code

Checking these upfront resolves the vast majority of integration issues before you ever need to refactor Apex code.

⚠️ Common Mistake
Many developers only remember to pass the Authorization header and omit Content-Type or Accept.

Different APIs have strict expectations. Always read the target system's API documentation before building your callout in Salesforce!

📖 Integration Term of the Day
HTTP Header

A key-value pair included in HTTP requests and responses that provides essential metadata and processing instructions about the transmission.

🧪 Quick Challenge
Which header is used to send an OAuth Access Token?

Content-Type

Accept

Authorization

💬 Drop your answer below! I'll reveal it in tomorrow's post before we dive into authentication.

📅 Next Chapter
🔐 Authentication vs Authorization

What's the difference, and why do developers so frequently confuse them?

🏷️ Tags
#Salesforce #SalesforceDeveloper #SalesforceIntegration #RESTAPI #HTTPHeaders #OAuth #Apex #DeveloperCommunity #IntegrationMasterySeries

<img width="598" height="900" alt="1784525611154" src="https://github.com/user-attachments/assets/eb89092d-754a-43e0-a9d1-9bf54ad7eecf" />
