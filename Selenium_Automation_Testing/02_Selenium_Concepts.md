## Selenium Concepts:

### Selenium Locators;

Selenium provides multiple locator strategies to identify and interact with elements in the DOM. These locators are essential for automating web applications effectively. Below are the key locator strategies supported by Selenium:

```TABLE
| # | Locator               | Example                               |
| - | --------------------- | ------------------------------------- |
| 1 | **ID**                | `By.id("username")`                   |
| 2 | **Name**              | `By.name("email")`                    |
| 3 | **Class Name**        | `By.className("login-btn")`           |
| 4 | **Tag Name**          | `By.tagName("input")`                 |
| 5 | **Link Text**         | `By.linkText("Login")`                |
| 6 | **Partial Link Text** | `By.partialLinkText("Log")`           |
| 7 | **CSS Selector**      | `By.cssSelector("#username")`         |
| 8 | **XPath**             | `By.xpath("//input[@id='username']")` |
| 8 | **Relative Locators   |  locate elements based on their spatial relationship to other elements
```

<img width="1189" height="490" alt="image" src="https://github.com/user-attachments/assets/8400729b-4f7e-4942-babc-c43e15d85173" />

**Mind Map**
| Locator               | HTML Example             | Selenium                         |
| --------------------- | ------------------------ | -------------------------------- |
| **ID**                | `id="username"`          | `By.id("username")`              |
| **Name**              | `name="email"`           | `By.name("email")`               |
| **Tag**               | `<button>`               | `By.tagName("button")`           |
| **Class**             | `class="login-btn"`      | `By.className("login-btn")`      |
| **Link Text**         | `>Products</a>`          | `By.linkText("Products")`        |
| **Partial Link Text** | `>View All Products</a>` | `By.partialLinkText("Products")` |


