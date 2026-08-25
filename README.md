## When you find a defect, go through these 5 questions: for Severity:

|     # | Question                                  | What you are determining   |
| ----: | ----------------------------------------- | -------------------------- |
| **1** | What functionality is broken?             | Understand the defect      |
| **2** | Is it a core/important business function? | Business importance        |
| **3** | What happens if users encounter it?       | Actual impact              |
| **4** | Is there a workaround?                    | Whether users can continue |
| **5** | How many users/transactions are affected? | Scope of impact            |

## For Priority:
### How to determine Priority

| Question                                                   | What are you checking?                        |
| ---------------------------------------------------------- | --------------------------------------------- |
| **1. Does it affect an important business goal?**          | Revenue, customers, critical feature, release |
| **2. How many users are affected?**                        | One user vs. most/all users                   |
| **3. Is the affected functionality currently being used?** | Frequently used vs. rarely used               |
| **4. Is there a deadline/release dependency?**             | Must be fixed before release?                 |
| **5. Is there a workaround?**                              | Easy workaround vs. no workaround             |
| **6. Is there customer/reputation impact?**                | Complaints, bad user experience, brand impact |
| **7. Is the defect blocking other work?**                  | Testing/development/release blocked?          |


## Example 1 — High Severity + High Priority

**Bug:** Customers are charged twice for one payment.

* Financial impact → Yes
* Core business flow → Yes
* Customer impact → High
* Workaround → No
* Release concern → Immediate

➡️ **Severity: Critical**
➡️ **Priority: P1 / High**

This needs to be fixed immediately.

---

## Example 2 — Low Severity + High Priority

**Bug:** Company logo is incorrect on the homepage.

Technically:

* No functional failure
* No data loss
* No financial impact

➡️ **Severity: Low**

But suppose:

> The company is launching a major marketing campaign tomorrow.

Now the business may say:

> "This must be fixed before release."

➡️ **Priority: High**

So:

**Low Severity + High Priority**

is completely possible.

---

## Example 3 — High Severity + Low Priority

Suppose there is a serious defect in an **admin report that only one internal employee uses**, and the report is needed only once every six months.

* Functional impact → High
* But very few users
* Not currently required
* No immediate business deadline
* Workaround exists

➡️ **Severity: High**
➡️ **Priority: Low/Medium**

This is another important example showing that **Severity and Priority are independent**.

---

# A simple Priority decision tree

Think:

**How urgently does the business need this fixed?**

### 🔴 P1 — Critical / Immediate

Use when:

* Release is blocked
* Major customer impact
* Revenue is affected
* Critical business operation is affected
* No workaround
* Large number of users affected
* Production incident

➡️ **Fix immediately**

### 🟠 P2 — High

Use when:

* Important functionality affected
* Significant number of users affected
* Workaround exists
* Important feature but release can continue
* Should be fixed soon

➡️ **Fix before/early in release**

### 🟡 P3 — Medium

Use when:

* Limited business impact
* Smaller number of users
* Workaround available
* Non-critical functionality

➡️ **Fix in normal development cycle**

### 🟢 P4 — Low

Use when:

* Cosmetic issue
* Minor usability problem
* Very little business impact
* Can be fixed when time/resources are available
