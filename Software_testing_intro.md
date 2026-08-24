## Testing:
Testing is a systematic process used to **verify and validate** that a product, its main **purpose** is to **identify errors, bugs, or missing requirements before the product is released**, ensuring reliability, security, and high performance while reducing risks and costs associated with failures.

## modules of manual testing:
```
MANUAL TESTING
│
├── 1. Software Testing Fundamentals
│   ├── What is Testing?
│   ├── QA vs QC vs Testing
│   ├── Verification vs Validation
│   ├── Error / Defect / Bug / Failure
│   └── Severity vs Priority
│
├── 2. SDLC
│   ├── Waterfall
│   ├── Agile
│   └── Scrum
│
├── 3. STLC
│   ├── Requirement Analysis
│   ├── Test Planning
│   ├── Test Case Development
│   ├── Test Environment Setup
│   ├── Test Execution
│   ├── Defect Reporting
│   └── Test Closure
│
├── 4. Testing Levels
│   ├── Unit
│   ├── Integration
│   ├── System
│   └── Acceptance / UAT
│
├── 5. Testing Types
│   ├── Functional
│   └── Non-Functional
│
├── 6. Testing Techniques
│   ├── Black Box
│   ├── White Box
│   ├── Grey Box
│   ├── Equivalence Partitioning
│   ├── Boundary Value Analysis
│   ├── Decision Table
│   └── State Transition
│
├── 7. Test Design & Documentation
│   ├── Test Scenario
│   ├── Test Case
│   ├── Test Data
│   ├── Test Suite
│   ├── Checklist
│   └── RTM
│
├── 8. Defect Management
│   ├── Defect Life Cycle
│   ├── Severity
│   ├── Priority
│   ├── Defect Report
│   └── Retesting
│
├── 9. Important Testing Activities
│   ├── Smoke
│   ├── Sanity
│   ├── Regression
│   ├── Retesting
│   ├── Exploratory Testing
│   └── Ad-hoc Testing
│
├── 10. GUI / Web Testing
│   ├── Forms
│   ├── Buttons
│   ├── Links
│   ├── Browser compatibility
│   ├── Cookies
│   ├── Sessions
│   └── Responsive UI
│
├── 11. API Testing
│   ├── HTTP/HTTPS
│   ├── GET/POST/PUT/PATCH/DELETE
│   ├── Status Codes
│   ├── Headers
│   ├── Request/Response
│   ├── Authentication
│   └── Postman
│
├── 12. Database Testing
│   ├── SQL basics
│   ├── SELECT
│   ├── INSERT/UPDATE/DELETE
│   ├── Joins
│   └── Data validation
│
└── 13. Real-World QA Process
    ├── Jira
    ├── Test Management
    ├── Agile/Scrum ceremonies
    ├── Sprint testing
    ├── Defect tracking
    └── Release testing
```

- software testing concepts
- STLC
- Software testing project templates
- Agile testing and Jira tool
- AI use in manual testing

## What is Software?

**Software is a collection of instructions that allows a computer or device to perform specific tasks.**

###  Types:
```
                         SOFTWARE
                            │
          ┌─────────────────┼─────────────────┐
          │                 │                 │
    SYSTEM SOFTWARE   APPLICATION         SOFTWARE PROGRAMMING /
                                          DEVELOPMENT SOFTWARE
          │                 │                 │
     Windows/Linux      Chrome            IDEs
     Device Drivers     WhatsApp          Compilers
     Firmware           MS Word           Interpreters
     Utilities          Banking Apps      Debuggers
```
### parameters for Quality of product:
- Bug free
- Delivered on time
- within budget
- meet the requirements/expectations
- maintainable

## SDLC:
The Software Development Life Cycle (SDLC) is a structured methodology used by development teams to design, develop, test, deploy, and maintain high-quality software. It provides a systematic framework that ensures software meets customer expectations, adheres to project requirements, and is delivered efficiently. By breaking the development process into distinct phases, SDLC helps manage complexity, reduce risks, and optimize resources.

### Waterfall Model

**The Waterfall Model is a sequential SDLC model where software development is divided into different phases, and each phase is completed before moving to the next phase.**
```
┌──────────────┐    ┌──────────┐    ┌─────────────┐    ┌─────────┐    ┌────────────┐    ┌─────────────┐
│ Requirements │ →  │  Design  │ →  │ Development │ →  │ Testing │ →  │ Deployment │ →  │ Maintenance │
└──────────────┘    └──────────┘    └─────────────┘    └─────────┘    └────────────┘    └─────────────┘
```

#### Advantages:
- **Simple and easy to understand:** The phases are clearly defined.
- **Easy to manage**: Each phase has specific activities and deliverables.
- **Good documentation**: Requirements, design, test documents, etc. are usually well documented
- **Easy to track progress**: Project managers can clearly see which phase is completed.
- **Suitable for stable requirements**: Works well when requirements are known and unlikely to change.

#### Disadvantages
- **Difficult to handle changes**: Changes to requirements later in the project can be expensive.
- **Testing happens late**: Testing generally starts after development is completed.
- **Customer feedback comes late**: Customers may see the working product only near the end.
- **Higher risk if requirements are wrong**: A mistake in requirements can affect design, development, and testing.
- **Working software is delivered late**: Users generally don't get usable software until the later stages.
- **Not suitable for frequently changing requirements**: Projects with rapidly changing business requirements are usually better suited to Agile.

### Spiral Model:
The Spiral Model is a risk-driven SDLC model where the software is developed through repeated cycles (spirals). Each cycle includes planning, risk analysis, development, and evaluation.
```
┌──────────────┐ → ┌──────────────┐ → ┌──────────────┐ → ┌──────────────┐
│   Planning   │   │ Risk Analysis│   │ Development  │   │   Evaluation │
└──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘
        ↑                                                     │
        └────────────────── Next Spiral / Iteration ──────────┘
```
#### Advantages
- **Risk management** – Risks are identified and addressed early.
- **Handles changing requirements** – Requirements can be modified in later cycles.
- **Customer feedback** – Customer feedback is taken at the end of each cycle.
- **Early prototypes** – Prototypes can be created to validate ideas.
- **Suitable for large projects** – Useful for complex and high-risk projects.
  
#### Disadvantages
- **Expensive** – Risk analysis and repeated cycles increase cost.
- **Time-consuming** – Multiple iterations can take longer.
- **Complex to manage** – Requires experienced project management.
- **Not suitable for small projects** – The process may be unnecessarily complicated.
- **Requires strong risk analysis** – Poor risk assessment can negatively affect the project.


### V-Model (Verification and Validation Model)

The V-Model is an SDLC model where development activities and corresponding testing activities are planned in parallel. It is called the V-Model because the process looks like the letter V.
```
Requirements Analysis              Acceptance Testing
        ↓                                  ↑
System Design                     System Testing
        ↓                                  ↑
High-Level Design                Integration Testing
        ↓                                  ↑
Low-Level Design                     Unit Testing
        ↓                                  ↑
               Coding / Implementation
```
#### Advantages
- Testing is planned early.
- Defects can be identified earlier.
- Clear and structured process.
- Good documentation.
- Suitable when requirements are stable and well understood.
- Works well for projects where quality and compliance are important.
  
#### Disadvantages
- Difficult to accommodate changing requirements.
- Working software is generally available late.
- Changes can be expensive.
- Not ideal for highly dynamic projects.
- Requires requirements to be clearly defined at the beginning.

##### Types of testing in V Model:
- Static testing: correctness and completeness
  -  can be done using **review, walkthrough and inspection**
- Dynamic Testing: Unit, Integration, system and UAT testing's
  
=====================================================================================================
## Types Of Testing

### 4. Testing Based on Code Knowledge

| Type                  | Tester knowledge of code                     |
| --------------------- | -------------------------------------------- |
| **Black Box Testing** | No internal code knowledge required          |
| **White Box Testing** | Full knowledge of internal logic code         
| **Grey Box Testing**  | Partial knowledge of internal implementation (DB testing) |  


### 3. Testing Based on Execution

**Manual Testing**

* Tester executes test cases manually.

**Automation Testing**

* Tools/scripts execute test cases automatically.
* Selenium
* Playwright
* Cypress
* Appium
* REST Assured, etc.

### 5. Testing at Different Levels

A useful way to remember it is:

**Unit → Integration → System → E2E → UAT**

For example, in a microservices application:

`Service code → Service-to-service communication → Complete application → Business workflow → Customer acceptance`

```
Don't try to learn every testing type equally. Focus strongly on:

**Functional Testing → API Testing → UI Automation → Integration Testing → E2E → Regression → Performance → Security → CI/CD Test Automation**

And because you're already moving toward **DevOps**, learning how testing fits into **CI/CD pipelines and DevSecOps** will be especially valuable.
```

## QA vs QC vs QE:

| Aspect                | **QA — Quality Assurance**             | **QC — Quality Control**                   | **QE — Quality Engineering**                                                                                 |
| --------------------- | -------------------------------------- | ------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| **Main focus**        | **Process**                            | **Product**                                | **Quality across the engineering lifecycle**                                                                 |
| **Goal**              | Prevent defects                        | Detect defects                             | **Prevent, detect, and continuously improve quality**                                                        |
| **Approach**          | **Proactive**                          | **Reactive**                               | **Proactive + Preventive + Continuous**                                                                      |
| **What it asks**      | "Are we following the right process?"  | "Does the product meet requirements?"      | **"How can we engineer quality into the product from the beginning?"**                                       |
| **Activities**        | Defining standards, processes, reviews | Testing, inspection, defect identification | **Automation, shift-left testing, CI/CD quality gates, performance, security, observability, test strategy** |
| **When**              | Throughout development                 | Mainly during/after product development    | **Throughout the entire SDLC**                                                                               |
| **Example**           | Define coding/testing standards        | Execute test cases and report bugs         | **Automate tests and integrate them into CI/CD so defects are caught early**                                 |
| **Responsibility**    | Process quality                        | Product quality                            | **Engineering quality across development, testing, deployment and production**                               |
| **Typical roles**     | QA Engineer, QA Manager                | QC Inspector, Tester                       | **Quality Engineer, SDET, Senior QA Engineer**                                                               |
| **Automation**        | May use automation                     | Uses testing tools                         | **Strong focus on automation and engineering solutions**                                                     |
| **CI/CD involvement** | Usually defines quality processes      | Executes tests in pipeline                 | **Integrates automated quality checks directly into CI/CD**                                                  |
| **Production focus**  | Process compliance                     | Product defects                            | **Reliability, performance, observability and continuous improvement**                                       |

=======================================================================================
## levels of testing:
- **Unit testing**
  - also known as module testing/component testing
  - test specific part of software (Single component)
  - Unit Testing Techniques:
    - basis path testing: 
    - Controlled structure testing
      - conditional coverage
      - loops coverage (mutation)

```
module testing: related to Code/module
component testing: related to application (on UI)
```

- **Integration testing**
  - conducted on the two or more modules or components (verify the Communication between the two modules)
  - Integration testing techniques:
    - incremental integration
      - top-down
      - bottom-up
    - non-incremental integration
      
- **System testing:**
  - testing functionality as per the client requirements.
  - before system testing, we should know the customer requirements
  - this testing focuses on below aspects:
    - User interphase testing (GUI)
    - functionality testing
    - non-functional testing
    - usability testing
- **user acceptance testing**
  - Done by UAT team
    - in two levels
      - Alpha testing: in the org real data 
      - Beta testing: in the customer environment with customer data


```
SOFTWARE TESTING
│
├── 1. TESTING LEVELS
│   │
│   ├── Unit Testing
│   │   └── Tests individual functions/classes
│   │
│   ├── Integration Testing
│   │   └── Tests interaction between modules/services
│   │
│   ├── System Testing
│   │   └── Tests the complete application
│   │
│   └── Acceptance Testing / UAT
│       └── Validates that the system meets business requirements
│
├── 2. TESTING NATURE
│   │
│   ├── Functional Testing
│   │   └── Checks WHAT the application does
│   │       │
│   │       ├── Object Properties Testing
│   │       ├── Database Testing
│   │       ├── Error Handling Testing
│   │       ├── Calculations / Manipulations Testing
│   │       ├── Links Testing
│   │       └── Cookies & Sessions Testing
│   │
│   └── Non-Functional Testing
│       └── Checks HOW WELL the application works
│           │
│           ├── Performance Testing
│           ├── Security Testing
│           ├── Usability Testing
│           ├── Compatibility Testing
│           ├── Reliability Testing
│           └── Scalability Testing
│
├── 3. TESTING PURPOSE
│   │
│   ├── Smoke Testing
│   │   └── Checks whether the build is stable
│   │
│   ├── Sanity Testing
│   │   └── Checks a specific change/fix
│   │
│   └── Regression Testing
│       └── Checks whether existing functionality is broken
│
└── 4. TESTING APPROACH
    │
    ├── Black Box Testing
    │   └── No knowledge of internal code required
    │
    ├── White Box Testing
    │   └── Knowledge of internal code required
    │
    └── Grey Box Testing
        └── Partial knowledge of internal code
```

```
                                                  SOFTWARE TESTING
                                │
                         TESTING LEVELS
                                │
          ┌─────────────────────┼─────────────────────────┐
          │                     │                         │
        UNIT              INTEGRATION                   SYSTEM
       TESTING               TESTING                    TESTING
                                                           │
                                                           │
                                             Complete Integrated System
                                                           │
                                  ┌────────────────────────┴───────────────────────┐
                                  │                                                │
                           FUNCTIONAL                                      NON-FUNCTIONAL
                             TESTING                                           TESTING
                                  │                                                │
                          "WHAT does it do?"                              "HOW WELL does it work?"
                                  │                                                │
                  ┌───────────────┼────────────────┐              ┌────────────────┼───────────────┐
                  │               │                │              │                │               │
                 GUI             API          Business       Performance        Security        Usability
              Functional      Functional       Workflows          │                │               │
                  │               │                │               ├── Load         ├── Auth        ├── Ease of use
                  │               │                │               ├── Stress       ├── Access      ├── Navigation
                  │               │                │               ├── Spike        └── Vulnerability
                  │               │                │               └── Endurance
                  │               │                │
                  ├── UI behavior ├── Requests     ├── E2E
                  ├── Validation  ├── Responses    ├── Business rules
                  ├── Buttons     ├── Status codes ├── Workflows
                  ├── Forms       └── Data         └── Data flow
                  ├── Links
                  ├── Dropdowns
                  └── Error messages
                                  │
                                  └── Other Functional Checks
                                      ├── Calculations
                                      ├── Data validation
                                      ├── Error handling
                                      ├── Database validation
                                      └── Cookies & Sessions

```

### GUI/UI Testing:

```
GUI / UI TESTING
│
├── Functional UI
│   ├── Buttons
│   ├── Textboxes
│   ├── Checkboxes
│   ├── Radio buttons
│   ├── Dropdowns
│   ├── Links
│   └── Error messages
│
├── Visual UI
│   ├── Size
│   ├── Position
│   ├── Alignment
│   ├── Font
│   ├── Colors
│   └── Images
│
└── Usability / Responsive UI
    ├── Readability
    ├── Navigation
    ├── Scrollbars
    └── Different screen resolutions
```

```
                         SOFTWARE TESTING
                                │
                         HOW TEST IS EXECUTED
                                │
                    ┌───────────┴───────────┐
                    │                       │
              MANUAL TESTING          AUTOMATION TESTING
                    │                       │
          ┌─────────┼─────────┐     ┌───────┼────────┐
          │         │         │     │       │        │
         GUI       API       DB    GUI     API      DB
          │         │         │     │       │        │
       Browser   Postman    SQL  Selenium  RestAssured SQL

```


## Non-Functional Testing:
Non-Functional Testing checks how well the software works rather than what functions it performs.

### Questions:
```
How fast is login?
Can the system handle 1,000 users?
Is the login secure?
```
### Non-Functional Parameters: (Separate Customer Document)
- Performance Testing:
  - Load Testing: Size/traffic by Virtual users using specific tools
    | Tool                                 | Common Use                                      | Popularity   |
    | ------------------------------------ | ----------------------------------------------- | ----------   |
    | **Apache JMeter**                    | Load, stress, API/web performance testing       | ⭐⭐⭐⭐⭐ |
    | **LoadRunner / OpenText LoadRunner** | Enterprise performance testing                  | ⭐⭐⭐⭐⭐ |
    | **Gatling**                          | High-performance load testing, often with CI/CD | ⭐⭐⭐⭐    |
    | **k6**                               | Modern API/load testing, DevOps-friendly        | ⭐⭐⭐⭐⭐  |

    **"The key performance metrics are response time, throughput, concurrent users, error rate, CPU utilization, memory utilization, network utilization, disk I/O, and response-time percentiles such as         P95 and P99."**

  - Stress testing: with unexpected or beyond the load 
  - Endurance testing: Stability of the application for long time (based on time), how much time does application handle the expected load.
  - spike testing: Sudden increasing and decreasing in the load
  - volume testing: related to DB, how much data does DB can handle (on Size of the DB and how much data can hold the DB)

<img width="529" height="185" alt="image" src="https://github.com/user-attachments/assets/abbaa9df-ca96-4a0d-a0b3-408d59ffbdad" />

- Security Testing: (Main aspects in this test **authentication & Authorization**
  - Focus on
    - network security
    - vulnerabilities
    - Data encryption & Decryption
- Recovery testing: back to normal under any abnormal situation without losing Data.
- Compatibility: OS,Browser,H/D - with hardware compatibility/configuration etc. (cross Browser testing)
- Forward and backward compatibilities
- Installation testing: easiness in the installation and for uninstall as well.
- Sanitation/garbage testing: extra feature also considers as bugs and should be removed.





