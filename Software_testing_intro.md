## Types Of Testing

### 4. Testing Based on Code Knowledge

| Type                  | Tester knowledge of code                     |
| --------------------- | -------------------------------------------- |
| **Black Box Testing** | No internal code knowledge required          |
| **White Box Testing** | Full knowledge of internal logic code         
| **Grey Box Testing**  | Partial knowledge of internal implementation (DB testing) |  

### 1. Functional Testing

Checks whether the application works according to requirements.

* **Unit Testing** – Tests individual functions/classes.
* **Integration Testing** – Tests interaction between modules/services.
* **System Testing** – Tests the complete application.
* **End-to-End (E2E) Testing** – Tests the complete business flow.
* **Smoke Testing** – Quick check that the build is stable enough for further testing.
* **Sanity Testing** – Focused testing after a small change/fix.
* **Regression Testing** – Ensures existing functionality still works after changes.
* **UAT (User Acceptance Testing)** – Validates that the system meets business requirements.

### 2. Non-Functional Testing

Checks **how well** the application works.

* **Performance Testing**

  * Load Testing
  * Stress Testing
  * Spike Testing
  * Endurance/Soak Testing
* **Security Testing**
* **Usability Testing**
* **Compatibility Testing**
* **Accessibility Testing**
* **Reliability Testing**
* **Scalability Testing**

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
===============================================================

## levels of testing:
- Unit testing
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

- Integration testing
  - conducted on the two or more modules or components (verify the Communication between the two modules)
  - Integration testing techniques:
    - incremental integration
      - top-down
      - bottom-up
    - non-incremental integration
- System testing:
  - testing functionality as per the client requirements.
  - before system testing, we should know the customer requirements
  - this testing focuses on below aspects:
    - User interphase testing (GUI)
    - functionality testing
    - non-functional testing
    - usability testing
- user acceptance testing





















