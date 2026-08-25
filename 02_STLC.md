## STLC- Software Testing Life Cycle:
It is the step-by-step process followed by the testing team to plan, design, execute, and complete testing.
```
Requirements Analysis
        ↓
Test Planning
        ↓
Test Case Development
        ↓
Test Environment Setup
        ↓
Test Execution
        ↓
Defect Reporting & Tracking
        ↓
Test Closure
```
<img width="990" height="466" alt="image" src="https://github.com/user-attachments/assets/77cd1ff4-1bbe-4c05-8c2c-f6fcb4cb9315" />

<img width="1081" height="538" alt="image" src="https://github.com/user-attachments/assets/7a53c266-b69e-4fe9-9097-c421867bf3b1" />

## During the test development phase:

<img width="576" height="244" alt="image" src="https://github.com/user-attachments/assets/2410e7e2-184b-46a2-84ba-4d0b78bd5edf" />  <img width="576" height="285" alt="image" src="https://github.com/user-attachments/assets/5b825527-db34-4384-8a02-0bc83fd04aed" /> <img width="576" height="290" alt="image" src="https://github.com/user-attachments/assets/44dba610-64a7-44bf-b770-293627ff1341" /> <img width="573" height="301" alt="image" src="https://github.com/user-attachments/assets/2da1dd05-16d5-4612-b0ee-13503c208919" />

**Note**
```
smoke and sanity - **p0**
regression test - **p1**
functionality test - **p2** 
UI test - **p3**
```
- **IF any defect**:
```
Severity = How badly the defect affects the application. this will have levels
        - Critical → System/application is unusable
        - High     → Major functionality is broken
        - Medium   → Functionality is partially affected
        - Low      → Minor issue
Priority = How quickly the defect should be fixed.
        - P1 → Fix immediately
        - P2 → Fix soon
        - P3 → Can be fixed later
```
## test case template:
<img width="1099" height="474" alt="image" src="https://github.com/user-attachments/assets/333443d0-d987-4c63-bf0c-d11d217d2d21" />

## RTM:
<img width="1128" height="541" alt="image" src="https://github.com/user-attachments/assets/ca6d9930-66ea-4766-a269-979769058119" /> <img width="569" height="227" alt="image" src="https://github.com/user-attachments/assets/8641d139-9226-4661-877a-715428397160" />


## Test Execution:

```
                    LOGIN TEST CASE
                           │
             ┌─────────────┼─────────────┐
             ↓             ↓             ↓
          Works         Doesn't       Cannot
         correctly       work         execute
             ↓             ↓             ↓
          PASS ✅        FAIL ❌      BLOCKED 🚫
                           ↓
                    Investigate issue
                           ↓
                       BUG 🐞
```

<img width="573" height="192" alt="image" src="https://github.com/user-attachments/assets/eafa2530-be58-4a4f-b84b-0d108c8d3e50" />

## Defect Reporting and Tracking:
### Severity: 
- How badly does this defect affect the application
  
| Severity        | Meaning                               | Example                        |
| --------------- | ------------------------------------- | ------------------------------ |
| 🔴 **Critical** | System/core functionality is unusable | Payment completely unavailable |
| 🟠 **High**     | Major functionality is broken         | User cannot log in             |
| 🟡 **Medium**   | Functionality is partially affected   | Search filter doesn't work     |
| 🟢 **Low**      | Minor issue                           | UI alignment/spelling issue    |


### Priority:
- How urgently does the business need this fixed

| Priority        | Meaning            | Example                        |
| --------------- | ------------------ | ------------------------------ |
| **P1 – High**   | Fix immediately    | Payment failure before release |
| **P2 – Medium** | Fix soon           | Important search issue         |
| **P3 – Low**    | Can be fixed later | Minor UI alignment             |

### mind Map:
```
                    DEFECT
                       │
                       ↓
             Is core business flow
                  affected?
                  /       \
                YES        NO
                 │          │
                 ↓          ↓
        Is it completely   Minor/UI/
          prevented?       cosmetic?
          /       \          │
        YES        NO        ↓
         │          │      LOW
         ↓          ↓
 Serious data/   Significant
 security/       functional
 financial       impact?
 impact?         /     \
   /   \        YES     NO
 YES    NO       │       │
  │      │       ↓       ↓
  ↓      ↓      HIGH    MEDIUM
CRITICAL
```
| Severity        | Think                                                       |
| --------------- | ----------------------------------------------------------- |
| 🔴 **Critical** | **Core flow completely broken + severe/widespread impact**  |
| 🟠 **High**     | **Major functionality significantly broken**                |
| 🟡 **Medium**   | **Functionality partially affected / workaround available** |
| 🟢 **Low**      | **Minor/cosmetic issue**                                    |



