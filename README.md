# Python-for-Azure
Helpful Python based explorations on Microsoft Azure

Dynamic Cost Analysis and Alert (DCAA)

this works o, EA subscription (tested on VCF DEV)
this doesnot work on CSP subscription (tested on OCBPS) 

https://medium.com/python-for-azure/python-for-azure-dynamic-cost-analysis-alerts-dcaa-in-azure-cost-management-b05ab632e4a4

pip install -r requirements.txt

There is also a forecasted projection provided via Azure cost management but that is again based on “historical trends”, the main challenge here is to have “dynamic monitoring and alerts” for some unexpected, random and sudden high Azure resource “utilization spike” that can increases the cost of Azure consumption drastically.

In order to tackle this challenge, I have developed a custom solution via Python SDK for Azure especially using “Cost Management API” to make this cost management either for a list of “Resource Groups” or “Subscriptions” dynamic; so that some sudden high utilization abnormalities of Azure resources can be first identified and later handled via condition based alerting mechanism. In this workflow demo threshold-value is set to +20% i.e., if the current cost is 20% more than the total-cost of the cost incurred for the last-week, then the script will generate an exception with message, ‘“Cost Exceeded! Take Action!”

Workflow
1. The script below demonstrates the usage of Python SDK for Azure for implementing the above said workflow i.e., setting up dynamic cost analysis and alert (DCAA) for the two scenarios as listed below:

Scenario I: Setting up DCAA for specific resource-groups under a similar or different subscription [Python Script]
Scenario II: Setting up DCAA for a subscription or a list of subscriptions that we want to monitor [Python Script]


