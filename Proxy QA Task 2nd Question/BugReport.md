Bug Ticket : Dashboard Fails to Load API Keys for Large Accounts

**Title**

[Team API Keys - Keys List] View API Keys List Never Finishes Loading for Accounts with 10k+ Keys


**Severity / Priority**

Severity: Critical
Priority: P0 :  Blocking Release as large customers (10k–150k keys) cannot manage keys, rotate keys, or monitor usage via the dashboard.


**Customer Impact**

Enterprise proxy customers cannot load or manage API keys.
Key rotation becomes impossible → security risk.
Support received multiple complaints of “blank page / infinite loading” after release.
Users cannot revoke, regenerate, or audit keys → may lead to proxy abuse or billing issues.


**Environment**

Stage (reproducible), Prod (reported by "number of" customers)
Browser: Chrome 120+, Firefox 116
Account Type: Workspace with ≥10,000 API keys


**Preconditions**

A workspace containing 10k+ API keys.


**Steps to Reproduce**

1. Log into any workspace containing 10k+ API keys.

2. Navigate to Team Settings: API Keys.

3. Observe the loading spinner on the keys table for 30 : 60 seconds.
   

**Expected Result**

Keys list should load within 2–5 seconds, using pagination or batch-loading.
UI should display the first 50–100 keys with working pagination.
Filtering & search should remain responsive.


**Actual Result**

The dashboard never finishes loading.
Spinner stays indefinitely (30+ seconds).
No API keys are displayed.
Browser DevTools shows the page consuming increasing memory.


**Logs / Evidence**
"The request and response curl."
"Satge: Screen record of the steps and the issue"
"Prod: Customer defect evidence"


