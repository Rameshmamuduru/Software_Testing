## WebDriver Methods:

**1. Get Methods**

**2. conditional Methods**

**3. browser methids**

**4. navigational methods**

**5. wait methods**

**1. Get Methods**
1. get("url"  - open url in the browser
2. getTitle()  - get title name of the page
3. getCurrentUrl()  - return url of the page
4. getPageSource()  - get source code of the page
5. getWindowHandle()  - return ID of the single browser windows
6. getWindowHandles()  - return ID of the multiple browser windows

**2. conditional methods** - access these commands thorugh WebElement

1. isDisplayed()
2. isEnabled()
3. isSelected()

**3. Browser Methods**

| Method                 | Purpose           |
| ---------------------- | ----------------- |
| `get(url)`             | Open a URL        |
| `navigate().to(url)`   | Navigate to a URL |
| `navigate().back()`    | Go back           |
| `navigate().forward()` | Go forward        |
| `navigate().refresh()` | Refresh the page  |

** 5.Wait Methods**

| Wait          | Method/Class       | Usage                             |
| ------------- | ------------------ | --------------------------------- |
| Implicit Wait | `implicitlyWait()` | Global wait for finding elements  |
| Explicit Wait | `WebDriverWait`    | Wait for a specific condition     |
| Fluent Wait   | `FluentWait`       | Custom polling/exception handling |


**Implicit Wait**


**Explicit Wait**
```
Create WebDriverWait
       ↓
Set maximum time = 10 seconds
       ↓
Tell Selenium what condition to wait for
       ↓
Condition satisfied?
   ↓             ↓
 YES            NO
  ↓              ↓
Continue      TimeoutException
```
```JAVA
//Creation of WebDriverWait object
WebDriverWait mywait = new WebDriverWait(driver, Duration.ofSeconds(10));

//Usage of object for the elements

WebElement cli = mywait.until(ExpectedConditions.visibilityOfElementLocated(By.xpath("//a[normalize-space()='OrangeHRM, Inc']")));
cli.click();
System.out.println(cli.isDisplayed());
```





















