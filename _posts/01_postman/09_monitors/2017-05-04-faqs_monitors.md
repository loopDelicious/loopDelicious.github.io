---
categories:
  - "postman"
  - "monitors"
title: "FAQs for monitors"
page_id: "faqs_monitors"
warning: false
---

### General questions

##### **What can I test with Monitors?**

You can use Postman Monitors for simple uptime monitoring (to make sure your servers are online) or performance monitoring (to make sure your servers are responding promptly), or you can write detailed [test suites](/docs/postman/scripts/test_scripts) to check for proper behavior, business logic, error handling, etc.

##### **What restrictions apply?**

Review [differences between monitors and the Postman app](/docs/postman/monitors/intro_monitors).

##### **How many monitors can I create?**

There is no limit to the number of monitors you can create. You can have any number of collections, each with any number of monitors. And each monitor can run on a different schedule.

##### **How long can a monitor run?**

Monitors are currently limited to 5 minutes for each run. This includes all HTTP requests, responses, and test scripts.

##### **How many HTTP requests can a monitor send?**

There is no limit to the number of requests, although the total run-time cannot exceed 5 minutes.

##### **How much data can a monitor send/receive?**

There is no limit to the amount of data that can be sent or received per request. However, large requests or responses will take longer to send and receive, so be sure that you can do everything within the 5-minute time limit.

##### **How do I troubleshoot problems?**

You can view the full console output for every monitor run, including any errors that occurred. You can also use methods such as `console.log()`, `console.warn()`, etc. to output your own debugging information. Learn more about [troubleshooting monitors](/docs/postman/monitors/troubleshooting_monitors).

### Security

##### **Who can see my Monitors?**

Monitors have the same permissions as Postman Collections. By default, your collections are private, so only you can see the collection and its monitors. If you share a collection, then other members of your Postman Pro or Enterprise team will be able to see the collection and its monitors. If you grant ``View & Edit`` permissions, then your team members will also be able to add monitors to your collection.

Each collection can have different permissions, so you can choose to have some private, some shared but view-only, and some shared and editable.

##### **Can I delete a Monitor?**

Yes. You can delete a monitor at any time. Once deleted, all run history for the monitor is deleted as well. If you want _keep_ the history, then you should pause the monitor instead of deleting it.

##### **Where do Monitors run?**

Monitors run on our cloud infrastructure, which is hosted by Amazon Web Services (AWS). More information about our cloud infrastructure is available at [our Security page](https://www.getpostman.com/security){:target="_blank"}.

##### **Can Monitors access private networks?**

No. Monitors can only connect to URLs that are publicly-available on the Internet. You cannot monitor APIs running on private networks, VPNs, or corporate intranets.

##### **Will Monitors impact my API performance?**

You have full control over the behavior of your monitors. You determine which of your API endpoints are called, how many, and how often. In addition, we restrict each monitor’s total run-time to 5 minutes, to limit the number of requests it can perform.
