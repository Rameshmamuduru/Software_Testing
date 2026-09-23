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

**findElement vs findElements**

findElement(loc) Vs findElements(loc)
--------------------------------------

**Scenario 1: Locator is matching with single web element**

- findElement(loc)  ----> single web element ----> WebElement
- findElements(loc) ----> single web element ----> List<WebElement>

**Scenario 2: Locator is matching with multiple web elements**

- findElement(loc)  ----> single web element ----> WebElement
- findElements(loc) ----> multiple web elements ----> List<WebElement>

**Scenario 3: Locator is not matching with any element**

- findElement(loc)  ----> NoSuchElementException
- findElements(loc) ----> will not throw any exception. Returns 0


**Mind Map**
| Locator               | HTML Example             | Selenium                         |
| --------------------- | ------------------------ | -------------------------------- |
| **ID**                | `id="username"`          | `By.id("username")`              |
| **Name**              | `name="email"`           | `By.name("email")`               |
| **Tag**               | `<button>`               | `By.tagName("button")`           |
| **Class**             | `class="login-btn"`      | `By.className("login-btn")`      |
| **Link Text**         | `>Products</a>`          | `By.linkText("Products")`        |
| **Partial Link Text** | `>View All Products</a>` | `By.partialLinkText("Products")` |


## CSS Selector:

CSS Selector is a way to tell Selenium exactly which HTML element you want to find by using CSS rules. In real automation, CSS selectors are used very frequently, especially when ID, name, or class alone is not enough.

**Combination Options we have**

**Most Used**
| CSS Selector                | Syntax                     | Full HTML Example                                    | Selenium Example                                        |
| --------------------------- | -------------------------- | ---------------------------------------------------- | ------------------------------------------------------- |
| **Tag**                     | `tag`                      | `<input type="text">`                                | `By.cssSelector("input")`                               |
| **ID**                      | `#id`                      | `<input id="username">`                              | `By.cssSelector("#username")`                           |
| **Class**                   | `.class`                   | `<button class="login">Login</button>`               | `By.cssSelector(".login")`                              |
| **Tag + Class**             | `tag.class`                | `<button class="login">Login</button>`               | `By.cssSelector("button.login")`                        |
| **Tag + ID**                | `tag#id`                   | `<input id="username">`                              | `By.cssSelector("input#username")`                      |
| **Attribute**               | `[attribute='value']`      | `<input name="username">`                            | `By.cssSelector("[name='username']")`                   |
| **Tag + Attribute**         | `tag[attribute='value']`   | `<input name="username">`                            | `By.cssSelector("input[name='username']")`              |
| **Multiple Attributes**     | `[attr1='v1'][attr2='v2']` | `<input type="text" name="username">`                | `By.cssSelector("input[type='text'][name='username']")` |
| **Tag + Class + Attribute** | `tag.class[attr='value']`  | `<button class="login" type="submit">Login</button>` | `By.cssSelector("button.login[type='submit']")`         |
| **Multiple Classes**        | `.class1.class2`           | `<button class="btn login">Login</button>`           | `By.cssSelector(".btn.login")`                          |
| **Parent → Child**          | `parent child`             | `<form><input name="user"></form>`                   | `By.cssSelector("form input")`                          |
| **Direct Child**            | `parent > child`           | `<form><input name="user"></form>`                   | `By.cssSelector("form > input")`                        |

**Other Usefull**

| CSS Selector                          | Syntax                         | Full HTML Example                            | Selenium Example                                  |
| ------------------------------------- | ------------------------------ | -------------------------------------------- | ------------------------------------------------- |
| **Attribute Starts With**             | `[attr^='value']`              | `<input id="user_12345">`                    | `By.cssSelector("[id^='user_']")`                 |
| **Attribute Contains**                | `[attr*='value']`              | `<input id="user_12345">`                    | `By.cssSelector("[id*='user']")`                  |
| **Attribute Ends With**               | `[attr$='value']`              | `<input id="username_field">`                | `By.cssSelector("[id$='field']")`                 |
| **Exact Attribute**                   | `[attr='value']`               | `<input name="username">`                    | `By.cssSelector("[name='username']")`             |
| **Parent + Attribute**                | `parent [attr='value']`        | `<form><input name="username"></form>`       | `By.cssSelector("form [name='username']")`        |
| **Parent + Direct Child + Attribute** | `parent > child[attr='value']` | `<form><input name="username"></form>`       | `By.cssSelector("form > input[name='username']")` |
| **Immediately Following Sibling**     | `element + sibling`            | `<label>Username</label><input type="text">` | `By.cssSelector("label + input")`                 |
| **First Child**                       | `parent :first-child`          | `<div><input><input></div>`                  | `By.cssSelector("div input:first-child")`         |
| **Last Child**                        | `parent :last-child`           | `<div><input><input></div>`                  | `By.cssSelector("div input:last-child")`          |



**Learning Flow**

```
LEVEL 1 — Basic
│
├── tag
├── #id
└── .class


LEVEL 2 — Attributes
│
├── [attribute='value']
├── tag[attribute='value']
└── multiple attributes


LEVEL 3 — Combination
│
├── tag.class
├── tag#id
├── .class[attribute='value']
└── tag.class[attribute='value']


LEVEL 4 — Relationships
│
├── parent child
├── parent > child
├── +
└── ~


LEVEL 5 — Dynamic attributes
│
├── [attribute^='value']   starts with
├── [attribute$='value']   ends with
└── [attribute*='value']   contains


LEVEL 6 — Position
│
├── :first-child
├── :last-child
└── :nth-child()
```


## XPath

- XPath stands for XML Path Language, XPath is a way to locate an element in the HTML/DOM
- it will work on the Document Object Model (DOM)

**Xpath Types**

1. Absolutute XPath - loaded from root of the html
2. Relative Xpath - directly find the element attribute

**Absolute vs Relative Xpaths**

1) Absolute XPath starts with /       ---> represents root node
   Relative XPath starts with //

2) Absolute XPath do not use attributes
   Relative XPath works with attribute

3) Absolute XPath traverse through each node till it finds element
   Relative XPath directly jump and find the element by using attribute

**Ways to generate relative Xpaths**
**1. Automative**

- Using Devtools/SelectorHub
  
**3. Manual**

```
//tagName[@attribute='value']                          //Single Attribute
//*[@attribute='value']

//*[@attribute='value'][@attribute='value']            //Multiple Attributr

// Using And/or operator
//*[@attribute='value' and @attribute='value']
//*[@attribute='value' or @attribute='value']

// Using inner Text
//tagName[text()='value']
//*[text()='value']

```

**Mosu Used**
```
| XPath Selector              | Syntax                                    | Full HTML Example                                    | Selenium Example                                          |
| --------------------------- | ----------------------------------------- | ---------------------------------------------------- | --------------------------------------------------------- |
| **Tag**                     | `//tag`                                   | `<input type="text">`                                | `By.xpath("//input")`                                     |
| **ID**                      | `//*[@id='value']`                        | `<input id="username">`                              | `By.xpath("//*[@id='username']")`                         |
| **Class**                   | `//*[@class='value']`                     | `<button class="login">Login</button>`               | `By.xpath("//*[@class='login']")`                         |
| **Tag + Class**             | `//tag[@class='value']`                   | `<button class="login">Login</button>`               | `By.xpath("//button[@class='login']")`                    |
| **Tag + ID**                | `//tag[@id='value']`                      | `<input id="username">`                              | `By.xpath("//input[@id='username']")`                     |
| **Attribute**               | `//*[@attribute='value']`                 | `<input name="username">`                            | `By.xpath("//*[@name='username']")`                       |
| **Tag + Attribute**         | `//tag[@attribute='value']`               | `<input name="username">`                            | `By.xpath("//input[@name='username']")`                   |
| **Multiple Attributes**     | `//tag[@attr1='v1' and @attr2='v2']`      | `<input type="text" name="username">`                | `By.xpath("//input[@type='text' and @name='username']")`  |
| **Tag + Class + Attribute** | `//tag[@class='value' and @attr='value']` | `<button class="login" type="submit">Login</button>` | `By.xpath("//button[@class='login' and @type='submit']")` |
| **Multiple Classes**        | `//tag[@class='class1 class2']`           | `<button class="btn login">Login</button>`           | `By.xpath("//button[@class='btn login']")`                |
| **Parent → Child**          | `//parent/child`                          | `<form><input name="user"></form>`                   | `By.xpath("//form/input")`                                |
| **Any Descendant**          | `//parent//child`                         | `<form><div><input name="user"></div></form>`        | `By.xpath("//form//input")`                               |
| **Direct Child**            | `//parent/child`                          | `<form><input name="user"></form>`                   | `By.xpath("//form/input")`                                |
```

**Other Paths**

| XPath Selector                        | Syntax                                 | Full HTML Example                                 | Selenium Example                                |
| ------------------------------------- | -------------------------------------- | ------------------------------------------------- | ----------------------------------------------- |
| **Attribute Starts With**             | `//tag[starts-with(@attr,'value')]`    | `<input id="user_12345">`                         | `By.xpath("//input[starts-with(@id,'user_')]")` |
| **Attribute Contains**                | `//tag[contains(@attr,'value')]`       | `<input id="user_12345">`                         | `By.xpath("//input[contains(@id,'user')]")`     |
| **Exact Attribute**                   | `//tag[@attr='value']`                 | `<input name="username">`                         | `By.xpath("//input[@name='username']")`         |
| **Parent + Attribute**                | `//parent//child[@attr='value']`       | `<form><div><input name="username"></div></form>` | `By.xpath("//form//input[@name='username']")`   |
| **Parent + Direct Child + Attribute** | `//parent/child[@attr='value']`        | `<form><input name="username"></form>`            | `By.xpath("//form/input[@name='username']")`    |
| **Following Sibling**                 | `//element/following-sibling::sibling` | `<label>Username</label><input type="text">`      | `By.xpath("//label/following-sibling::input")`  |
| **First Child**                       | `(//tag)[1]`                           | `<div><input><input></div>`                       | `By.xpath("(//input)[1]")`                      |
| **Last Child**                        | `(//tag)[last()]`                      | `<div><input><input></div>`                       | `By.xpath("(//input)[last()]")`                 |
| **Parent**                            | `//child/..`                           | `<div><input id="user"></div>`                    | `By.xpath("//input[@id='user']/..")`            |
| **Ancestor**                          | `//child/ancestor::tag`                | `<form><div><input></div></form>`                 | `By.xpath("//input/ancestor::form")`            |


**Css Must Master**
```
tag
#id
.class
tag.class
tag#id
[attribute='value']
tag[attribute='value']
[attribute1='value1'][attribute2='value2']
tag.class[attribute='value']
.class1.class2
parent child
parent > child
[attr^='value']
[attr*='value']
[attr$='value']
```

**Xpath Must Master**
```
//tag
//*[@id='value']
//tag[@id='value']
//tag[@class='value']
//tag[@attribute='value']
//tag[@attr1='v1' and @attr2='v2']
//parent/child
//parent//child
//tag[text()='text']
//tag[contains(text(),'text')]
//tag[contains(@attribute,'value')]
```













