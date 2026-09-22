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


## CSS Selector:

CSS Selector is a way to tell Selenium exactly which HTML element you want to find by using CSS rules. In real automation, CSS selectors are used very frequently, especially when ID, name, or class alone is not enough.

**Combination Options we have**
- Tag
- ID
- class
- tag + class
- tag + ID
- Attribute
- Tag+Attribute
- Multiple Attributes
- Tag+class+attributes
- multiple classes
- Parent ---> child
- Direct child
- Attribute starts with ^=
- Attribute starts with ^=
- Attribute contains *=
- Attribute contains *=
- Exact attribute =
- Combining parent + attribute
- Parent + direct child + attribute
- + — immediately following sibling
- :first-child
- :last-child
- :first-child

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

<img width="1173" height="301" alt="image" src="https://github.com/user-attachments/assets/d60948e0-381b-4c2f-873a-d9c620919dbb" />

**Ways to generate relative Xpaths**
**1. Automative**

- Using Devtools/SelectorHub
  
**3. Manual**

```
//tagName[@attribute='value']                          //Single Attribute
//*[@attribute='value']

//*[@attribute='value'][@attribute='value']            //Multiple Attributr
```


















