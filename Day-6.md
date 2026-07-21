# 📘 Day 6/100 – How Does a REST API Actually Work?

Yesterday we learned **REST vs SOAP**.  
Today, let's see how a REST API works with a real Salesforce example.

Imagine a customer submits this form on your website:

* **Name:** John Smith
* **Email:** john@test.com
* **Phone:** +1 987654321

---

## 🔄 What Happens Behind the Scenes?

```text
Website
   │
   ▼ POST Request
   │
Salesforce (Creates Lead)
   │
   ▼ JSON Response
   │
Website

```
Every REST API follows this same simple flow:

```text
Request ──► Process ──► Response
```

💻 Mini Practical
This is what the JSON Request Body looks like:
```text
JSON
{
  "FirstName": "John",
  "LastName": "Smith",
  "Email": "john@test.com"
}
```

And Salesforce might send back this JSON Response:

```text
JSON
{
  "success": true,
  "leadId": "00QXXXXXXXXXXXX"
}
```
👉 That's it! No complex theory. One system sends data, and the other system processes it and responds.

💼 Real Project Insight
In one of my projects, Salesforce sent approved customer records to Microsoft Dynamics 365 Business Central.

The response returned a Customer Number, which we stored in Salesforce and later used to synchronize invoices and payments.

One response field... but it became the primary key for the entire integration.

🧠 Architect's Tip
Don't design APIs around Salesforce objects. Design them around business processes.

The external system doesn't care about every Salesforce field—it only needs the data required to complete its job.

⚠️ Common Mistake
Many developers send 50+ fields simply because they are available in the object schema.

Instead, send only the fields the external system actually needs.

Your APIs will be:

✅ Faster

✅ Easier to debug

✅ Easier to maintain

📅 Next Chapter
GET vs POST vs PUT vs PATCH vs DELETE — Which HTTP method should you actually use?

💬 Question of the Day
Have you ever tested a REST API using Postman?

🏷️ Tags
#Salesforce #SalesforceDeveloper #SalesforceIntegration #RESTAPI #Apex #DeveloperCommunity #IntegrationMasterySeries

<img width="755" height="897" alt="SALESFORCE INTEGRATION HANDBOOK" src="https://github.com/user-attachments/assets/175176c1-ee93-4d2f-b82e-a58f92c3d83a" />
