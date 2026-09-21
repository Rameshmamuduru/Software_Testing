# Selenium Methods — Real-Time SDET Categories

## 1. 🌐 Browser / Navigation

Used to control where the browser goes.

| Method                 | Use             |
| ---------------------- | --------------- |
| `get()`                | Open URL        |
| `getTitle()`           | Get page title  |
| `getCurrentUrl()`      | Get current URL |
| `navigate().to()`      | Navigate to URL |
| `navigate().back()`    | Go back         |
| `navigate().forward()` | Go forward      |
| `navigate().refresh()` | Refresh page    |

Example:

```java
driver.get("https://example.com");

System.out.println(driver.getTitle());
System.out.println(driver.getCurrentUrl());

driver.navigate().refresh();
```

**Priority: ⭐⭐⭐⭐⭐**

---

# 2. 🔎 Finding Web Elements

This is one of the **most important areas for SDET**.

| Method           | Use                    |
| ---------------- | ---------------------- |
| `findElement()`  | Find one element       |
| `findElements()` | Find multiple elements |

Example:

```java
WebElement username = driver.findElement(By.id("username"));

List<WebElement> products =
        driver.findElements(By.className("product"));
```

You'll combine these with:

```java
By.id()
By.name()
By.className()
By.tagName()
By.linkText()
By.partialLinkText()
By.cssSelector()
By.xpath()
```

**Priority: ⭐⭐⭐⭐⭐**

---

# 3. 🖱️ WebElement Interaction

Once you find an element, you interact with it.

This is actually **WebElement**, not WebDriver.

| Method           | Use                            |
| ---------------- | ------------------------------ |
| `click()`        | Click element                  |
| `sendKeys()`     | Enter text                     |
| `clear()`        | Clear input                    |
| `getText()`      | Get visible text               |
| `getAttribute()` | Get HTML attribute             |
| `isDisplayed()`  | Check visibility               |
| `isEnabled()`    | Check enabled/disabled         |
| `isSelected()`   | Check checkbox/radio selection |

Example:

```java
WebElement username = driver.findElement(By.id("username"));

username.clear();
username.sendKeys("Ramesh");

System.out.println(username.getAttribute("value"));
System.out.println(username.isDisplayed());
System.out.println(username.isEnabled());
```

**Priority: ⭐⭐⭐⭐⭐**

---

# 4. 🪟 Browser Window Management

Used to control browser size/window.

| Method                  | Use                   |
| ----------------------- | --------------------- |
| `manage()`              | Browser management    |
| `window().maximize()`   | Maximize              |
| `window().minimize()`   | Minimize              |
| `window().fullscreen()` | Full screen           |
| `getWindowHandle()`     | Get current window ID |
| `getWindowHandles()`    | Get all window IDs    |

Example:

```java
driver.manage().window().maximize();
```

For multiple tabs/windows:

```java
String parent = driver.getWindowHandle();

Set<String> windows = driver.getWindowHandles();
```

**Priority: ⭐⭐⭐⭐**

---

# 5. 🔄 Switching

Very important in real applications because you may have **iframes, tabs, windows and alerts**.

### Frame

```java
driver.switchTo().frame(frame);
driver.switchTo().parentFrame();
driver.switchTo().defaultContent();
```

### Window/Tab

```java
driver.switchTo().window(windowId);
```

### Alert

```java
driver.switchTo().alert();
```

**Priority: ⭐⭐⭐⭐⭐**

---

# 6. ⚠️ Alert Methods

After:

```java
Alert alert = driver.switchTo().alert();
```

You commonly use:

| Method       | Use                    |
| ------------ | ---------------------- |
| `accept()`   | Click OK               |
| `dismiss()`  | Click Cancel           |
| `getText()`  | Read alert message     |
| `sendKeys()` | Enter text into prompt |

Example:

```java
Alert alert = driver.switchTo().alert();

System.out.println(alert.getText());

alert.accept();
```

**Priority: ⭐⭐⭐⭐**

---

# 7. ⏳ Waits

**Extremely important for real-time automation.**

You will use waits because web applications don't always load elements immediately.

Main categories:

### Implicit Wait

```java
driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(10));
```

### Explicit Wait

Usually the more important one for modern automation:

```java
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));

wait.until(ExpectedConditions.visibilityOfElementLocated(
        By.id("username")));
```

Common `ExpectedConditions`:

| Condition                        | Use                          |
| -------------------------------- | ---------------------------- |
| `visibilityOfElementLocated()`   | Element visible              |
| `elementToBeClickable()`         | Element clickable            |
| `presenceOfElementLocated()`     | Element exists in DOM        |
| `invisibilityOfElementLocated()` | Element disappears           |
| `textToBePresentInElement()`     | Expected text appears        |
| `urlContains()`                  | URL contains expected text   |
| `titleContains()`                | Title contains expected text |

**Priority: ⭐⭐⭐⭐⭐**

---

# 8. 🖱️ Mouse & Keyboard Actions

For advanced user interactions.

Main class:

```java
Actions
```

Frequently used:

| Method            | Use             |
| ----------------- | --------------- |
| `click()`         | Click           |
| `doubleClick()`   | Double click    |
| `contextClick()`  | Right click     |
| `moveToElement()` | Hover           |
| `dragAndDrop()`   | Drag and drop   |
| `clickAndHold()`  | Hold mouse      |
| `release()`       | Release         |
| `sendKeys()`      | Keyboard action |

Example:

```java
Actions actions = new Actions(driver);

actions.moveToElement(menu).perform();
```

**Priority: ⭐⭐⭐⭐**

---

# 9. 📋 Dropdowns

For standard HTML `<select>` dropdowns.

Class:

```java
Select
```

Methods:

| Method                     | Use                 |
| -------------------------- | ------------------- |
| `selectByVisibleText()`    | Select by text      |
| `selectByValue()`          | Select by value     |
| `selectByIndex()`          | Select by index     |
| `getOptions()`             | Get all options     |
| `getFirstSelectedOption()` | Get selected option |
| `isMultiple()`             | Check multi-select  |

Example:

```java
Select country = new Select(
        driver.findElement(By.id("country")));

country.selectByVisibleText("India");
```

**Priority: ⭐⭐⭐⭐**

---

# 10. 📸 Screenshots

Frequently used for failure debugging.

```java
TakesScreenshot
```

Common method:

```java
getScreenshotAs()
```

Example:

```java
TakesScreenshot screenshot = (TakesScreenshot) driver;

File source = screenshot.getScreenshotAs(OutputType.FILE);
```

In a framework, screenshots are commonly captured when a test fails.

**Priority: ⭐⭐⭐⭐**

---

# 11. 📜 JavaScript Execution

Used when normal Selenium interaction isn't sufficient.

Class:

```java
JavascriptExecutor
```

Common method:

```java
executeScript()
```

Example:

```java
JavascriptExecutor js = (JavascriptExecutor) driver;

js.executeScript("arguments[0].click();", element);
```

Other common uses:

```java
js.executeScript("window.scrollBy(0,500);");
```

```java
js.executeScript("arguments[0].scrollIntoView(true);", element);
```

**Priority: ⭐⭐⭐**

Don't use JavaScript as the first solution. Normal Selenium interaction should generally be tried first.

---

# 12. 🗂️ Cookies

Used for browser/session-related testing.

| Method                | Use                    |
| --------------------- | ---------------------- |
| `getCookies()`        | Get all cookies        |
| `getCookieNamed()`    | Get specific cookie    |
| `addCookie()`         | Add cookie             |
| `deleteCookie()`      | Delete cookie          |
| `deleteCookieNamed()` | Delete specific cookie |
| `deleteAllCookies()`  | Delete all cookies     |

Example:

```java
driver.manage().deleteAllCookies();
```

**Priority: ⭐⭐⭐**

---

# 13. 🔚 Closing Browser

Very common.

| Method    | Use                                             |
| --------- | ----------------------------------------------- |
| `close()` | Close current window/tab                        |
| `quit()`  | End WebDriver session and close browser windows |

Example:

```java
driver.quit();
```

**Priority: ⭐⭐⭐⭐⭐**

---

# 14. 📍 Relative Locators

Useful when an element doesn't have a convenient unique locator.

```java
above()
below()
toLeftOf()
toRightOf()
near()
```

Example:

```java
driver.findElement(
    with(By.tagName("input"))
    .above(passwordField)
);
```

**Priority: ⭐⭐**

Know it, but don't make this your first priority.

---

# 🎯 Your SDET Learning Priority

I would learn them in this order:

| Priority | Category                   | Importance |
| -------- | -------------------------- | ---------- |
| 🔴 1     | Locators + `findElement()` | ⭐⭐⭐⭐⭐      |
| 🔴 2     | WebElement methods         | ⭐⭐⭐⭐⭐      |
| 🔴 3     | Browser/navigation         | ⭐⭐⭐⭐⭐      |
| 🔴 4     | Explicit waits             | ⭐⭐⭐⭐⭐      |
| 🔴 5     | Frames/windows/alerts      | ⭐⭐⭐⭐⭐      |
| 🟠 6     | Dropdowns                  | ⭐⭐⭐⭐       |
| 🟠 7     | Actions                    | ⭐⭐⭐⭐       |
| 🟠 8     | Screenshots                | ⭐⭐⭐⭐       |
| 🟡 9     | JavaScriptExecutor         | ⭐⭐⭐        |
| 🟡 10    | Cookies                    | ⭐⭐⭐        |
| 🟢 11    | Relative Locators          | ⭐⭐         |

### The core Selenium you should become very comfortable with

```text
Selenium
│
├── WebDriver
│   ├── get()
│   ├── getTitle()
│   ├── getCurrentUrl()
│   ├── navigate()
│   ├── findElement()
│   ├── findElements()
│   ├── switchTo()
│   ├── manage()
│   ├── getWindowHandle()
│   ├── getWindowHandles()
│   ├── close()
│   └── quit()
│
├── WebElement
│   ├── click()
│   ├── sendKeys()
│   ├── clear()
│   ├── getText()
│   ├── getAttribute()
│   ├── isDisplayed()
│   ├── isEnabled()
│   └── isSelected()
│
├── WebDriverWait
│   └── ExpectedConditions
│
├── Actions
│
├── Select
│
├── Alert
│
├── TakesScreenshot
│
└── JavascriptExecutor
```

**For your current stage, don't try to memorize all of these at once.** The natural next progression is **WebDriver → WebElement → Locators → Waits → Actions/Select → Alerts/Frames/Windows → Screenshots/JS**.
