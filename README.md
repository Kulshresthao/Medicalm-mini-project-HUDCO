Okay, here's a rewrite of that text, making it sound more human and less AI-generated.

**Mediclaim Analytics Dashboard – HUDCO PSU Case Story**

**1️⃣ The Story: Why We Built This Thing**

I put together a Mediclaim Analytics Dashboard to help a government/PSU health setup (think HUDCO) keep tabs on medical claims from employees and beneficiaries.

The point was to give decision-makers an easy way to see what's going on with claims, so they could:

*   See how fast claims are being settled.
*   Keep an eye on healthcare costs.
*   See how well hospitals are doing.
*   Find any holdups or possible fraud.

It's all about good governance, being open, and keeping an eye on the money – things PSUs really care about.

**2️⃣ Who Was Involved (The People Who Used It)**

The dashboard was made with typical PSU folks in mind:

*   Big bosses / admin heads
*   Finance people
*   Audit folks
*   Insurance companies / TPAs
*   Hospital and HR teams

Each of these folks needed to see the important stuff without getting bogged down in confusing reports.

**3️⃣ Where the Data Came From**

I grabbed data from open government sources and made-up sample data that looks like what you'd see in public-sector health insurance.

Data came from:

*   Ayushman Bharat (PM-JAY) – open claim info
*   State Health Insurance schemes
*   CGHS / ESIC sample claims
*   NIC / Data.gov.in health info

To make it real, I also faked some data using real claim forms, just with the names and personal stuff taken out. That's how these PSU projects usually go – using real formats, but with private info hidden.

**4️⃣ How the Data Was Set Up**

🟦 **Claims Table**

This was the main table with all the transactions.

| Column          | Description                      |
| --------------- | -------------------------------- |
| Claim\_ID       | Unique claim number              |
| Beneficiary\_ID | Employee/beneficiary ID          |
| Scheme\_Name    | CGHS / PM-JAY / ESIC             |
| Hospital\_ID    | Hospital code                    |
| Admission\_Date  | Date patient was admitted        |
| Discharge\_Date | Date patient left the hospital   |
| Claim\_Amount   | Amount of the claim              |
| Approved\_Amount | Amount that was approved       |
| Claim\_Status   | Approved / Denied / Still waiting |
| Rejection\_Reason | Why the claim was turned down   |
| TAT\_Days       | How long it took to settle       |

🟦 **Hospital Master**

| Column          | Description                |
| --------------- | -------------------------- |
| Hospital\_ID    | Unique hospital code       |
| Hospital\_Name  | Hospital name              |
| Hospital\_Type  | Government or Private      |
| City            | Where it's located         |
| Empanelment\_Status | Okay to use / Suspended |

🟦 **Beneficiary Master**

| Column          | Description            |
| --------------- | ---------------------- |
| Beneficiary\_ID | Beneficiary ID         |
| Age             | Age                    |
| Gender          | Gender                 |
| State           | State                  |
| Category        | Employee / Dependent / BPL |

**5️⃣ Getting the Data Ready (Power Query)**

I used Power Query to clean things up:

*   Got rid of duplicate claims
*   Made hospital names and IDs consistent
*   Filled in missing discharge dates
*   Made sure all the dates looked the same
*   Made some new fields for the analysis
*   Set up a star schema to make things run faster

Example Calculations:

*   Claim Duration: How long someone was in the hospital
*   Approval Rate: How much of the claimed amount got approved

**6️⃣ What We Kept an Eye On (KPIs)**

| KPI                      | Why It Matters in a PSU                  |
| ------------------------ | ---------------------------------------- |
| Total Claims             | How busy things are                       |
| Total Claim Amount       | Are we staying on budget?                |
| Approved vs Denied %      | Is our policy working?                  |
| Average TAT (Days)       | How fast are we processing claims?        |
| Average Claim Value      | How much are claims costing?             |
| Suspected Fraud %        | Are we catching bad actors?             |
| Top 10 Most Expensive Hospitals | Where's the money going?               |
| Claims &gt; 30 Days Old    | Are we meeting our service agreement?    |

These things help with keeping track of money, planning audits, and seeing how things are going.

**7️⃣ DAX Measures Used**

*   Total claims
*   Total amount claimed and approved
*   Approval rate (with error checking)
*   Average turnaround time

We kept it simple. No crazy formulas, just easy-to-understand numbers.

**8️⃣ Dashboard Design (Power BI)**

📊 **Page 1: Quick Look**

*   KPIs for claims, amounts, approval rate
*   Claims and spending over time
*   Claim status breakdown

*Who Used It:* Big Bosses

📊 **Page 2: How Hospitals Are Doing**

*   Hospitals with the most claims
*   Which hospitals deny the most claims
*   Comparing government and private hospitals
*   Where the hospitals are

📊 **Page 3: Money and Audits**

*   Difference between claimed and approved amounts
*   Really expensive claims
*   Same people filing claims over and over
*   Possible signs of fraud

📊 **Page 4: Operations &amp; Turnaround Time**

*   How old are the pending claims?
*   Turnaround time by insurance type
*   Claims that are taking too long

**9️⃣ What We Learned**

*   A lot of claims were taking longer than they should.
*   A few hospitals were racking up most of the costs.
*   Private hospitals were turning down more claims than government ones.
*   Some areas had a lot of repeat claims.

After using the dashboard, it was easier to see delays and problems.

**1️⃣0️⃣ The Big Picture (What HUDCO / PSU Cares About)**

This dashboard helped them:

*   Settle claims faster
*   Find expensive or risky hospitals
*   Keep a better handle on the budget
*   Plan audits better
*   Be more open and responsible

