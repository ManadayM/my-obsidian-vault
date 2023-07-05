---
template: note
---
![tp.web.random_picture](https://images.unsplash.com/photo-1471260246432-c58c1afceb0c?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjc0ODI0Mjcx&ixlib=rb-4.0.3&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2023-01-27) | (time:: 18:27) | (weather:: Vadodara: ☀️   +30°C ↓17km/h)

# Salesforce - Introduction

- Salesforce is a CRM that comes with a lot of **standard functionality** that you can use to run your business.
- Common activities for which businesses can utilize the Salesforce platform
	- **Sell to prospects and customers**: Salesforce gives you **Leads and Opportunities** to manage sales.
	- **Help customers after the sale**: Salesforce gives you **Cases and Communities** for customer engagement.
	- **Work on the go**: Salesforce provides a customizable Salesforce Mobile App.
	- **Collaborate with coworkers, partners, and customers**: Salesforce offers Slack, Chatter, and Communities to connect your company.
	- **Market to your audience**: Salesforce offers **Marketing Cloud** to manage your customer journeys.
- Salesforce comes with standard functionality for tracking common sales objects like *Accounts*, *Contacts*, and *Leads*.

## Salesforce Database
It’s important to understand what a **database** is in the context of Salesforce. When we talk about the database, think of a giant spreadsheet. When you put information into Salesforce, it gets stored in the database so you can access it again later.

## Salesforce App
**An app is a set of objects, fields, and other functionality** that supports a business process. You can see which app you’re using and switch between apps using the App Launcher.

## Salesforce Objects
- **An object is a database table that stores information about a specific type of item or data**, such as accounts, contacts, leads, opportunities, and cases. 
- **Objects have a set of fields**, which are similar to columns in a database table and hold specific information such as a name, email, phone number, and so on. 
- **Each object also has a set of relationships to other objects**, which can be used to link data together. For example, an Account object might have a relationship to a Contact object, so that all the contacts associated with an account can be easily accessed and viewed. Similarly, an Opportunity object might have a relationship to an Account object and a Contact object, so that the account and primary contact associated with an opportunity can be easily accessed and viewed.
- There are **two types of objects** in Salesforce: **standard objects**, which come with the Salesforce platform, and **custom objects**, which can be created by users to store information specific to their business needs.

## Salesforce Records & Fields
- Records are acutal data associated with an object.
- Fields are columns in object database tables. Both standard and custom objects have fields.



## Accounts, Contacts, and Leads Objects
In Salesforce, Accounts, Contacts, and Leads are objects that represent different types of people or organizations that a business interacts with.

- **Accounts** represent the *companies or organizations* that a business deals with. They can include information such as the company name, industry, and number of employees.
- **Contacts** are the *people associated with an account*, such as employees, decision-makers, or other key individuals. They can include information such as name, title, email address, and phone number.
- Leads are *potential customers or clients that have expressed interest in a business's products or services*. They can include information such as name, contact information, and the source of the lead (e.g. website, trade show, referral). Leads can be converted to Accounts and Contacts in Salesforce once an opportunity is identified.

In summary, Accounts represents the company, Contacts represent the people, and Leads are the potential customers.

---
## Internal Links
[[2023-01-27]], [[Salesforce - 001 Platform Basics|Salesforce Platform Basics]]