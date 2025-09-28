AWS Budgets CloudFormation Template
Description
This CloudFormation template creates AWS Budgets with alarms for daily, weekly, and monthly cost thresholds. It allows you to set custom thresholds and receive email notifications when your costs approach or exceed these thresholds.

Parameters
The template accepts the following parameters:

DailyThreshold: The daily budget threshold in USD.
WeeklyThreshold: The weekly budget threshold in USD.
MonthlyThreshold: The monthly budget threshold in USD.
Email: The email address to receive budget alerts.
AlertType: The type of alert to receive. Allowed values are ACTUAL, FORECASTED, or BOTH.
Resources
The template creates the following resources:

DailyBudget: An AWS Budget for daily cost monitoring.
WeeklyBudget: An AWS Budget for weekly cost monitoring.
MonthlyBudget: An AWS Budget for monthly cost monitoring.
Conditions
The template uses the following condition:

IsBoth: A condition that checks if the AlertType is set to BOTH. If true, it allows both actual and forecasted alerts; otherwise, it uses the specified AlertType.

Usage
To use this template, follow these steps:

Create a CloudFormation Stack:

Navigate to the CloudFormation service in the AWS Management Console.
Click on "Create stack" and select "With new resources (standard)".
Choose "Template body" and paste the YAML code from above.
Click "Next".
Specify Stack Details:

Provide a stack name.
Enter the parameters:
DailyThreshold: Your daily budget threshold in USD.
WeeklyThreshold: Your weekly budget threshold in USD.
MonthlyThreshold: Your monthly budget threshold in USD.
Email: The email address to receive budget alerts.
AlertType: The type of alert to receive (ACTUAL, FORECASTED, or BOTH).
Click "Next".
Configure Stack Options (optional):

You can add tags or set other options if needed.
Click "Next".
Review and Create:

Review the stack details.
Check the box to acknowledge that AWS CloudFormation might create IAM resources.
Click "Create stack".
After the stack is created, you will receive email notifications when your AWS costs approach or exceed the specified thresholds.
