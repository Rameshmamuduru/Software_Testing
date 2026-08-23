## Types Of Testing

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

### 4. Testing Based on Code Knowledge

| Type                  | Tester knowledge of code                     |
| --------------------- | -------------------------------------------- |
| **Black Box Testing** | No internal code knowledge required          |
| **White Box Testing** | Full knowledge of internal code              |
| **Grey Box Testing**  | Partial knowledge of internal implementation |

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
