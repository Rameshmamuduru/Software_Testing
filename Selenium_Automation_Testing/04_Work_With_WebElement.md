**Web-UI Elements to know**

| Priority | UI Element                | What you should practice                     |
| -------- | ------------------------- | -------------------------------------------- |
| ⭐⭐⭐⭐⭐    | **Text fields / Input**   | `sendKeys()`, `clear()`, get value           |
| ⭐⭐⭐⭐⭐    | **Buttons**               | click, enabled/disabled, text                |
| ⭐⭐⭐⭐⭐    | **Links**                 | click, text, URL/navigation                  |
| ⭐⭐⭐⭐⭐    | **Checkboxes**            | select, deselect, multiple selection         |
| ⭐⭐⭐⭐⭐    | **Radio buttons**         | select one, verify selected                  |
| ⭐⭐⭐⭐⭐    | **Dropdowns**             | select by text/value/index, verify selection |
| ⭐⭐⭐⭐⭐    | **Web tables**            | rows, columns, specific cell, dynamic data   |
| ⭐⭐⭐⭐⭐    | **Waits**                 | visible, clickable, presence, disappearance  |
| ⭐⭐⭐⭐     | **Alerts**                | accept, dismiss, get text, send text         |
| ⭐⭐⭐⭐     | **Frames / iFrames**      | switch into/out of frame                     |
| ⭐⭐⭐⭐     | **Multiple windows/tabs** | switch between windows                       |
| ⭐⭐⭐⭐     | **Date pickers**          | select current/future/past dates             |
| ⭐⭐⭐⭐     | **Auto-suggest**          | type → suggestions → select desired value    |
| ⭐⭐⭐⭐     | **Dynamic elements**      | changing IDs, dynamic lists, AJAX elements   |
| ⭐⭐⭐⭐     | **Mouse actions**         | hover, right-click, drag & drop              |
| ⭐⭐⭐⭐     | **Keyboard actions**      | Enter, Tab, Ctrl+A, Escape, etc.             |
| ⭐⭐⭐      | **Tooltips**              | hover and verify tooltip                     |
| ⭐⭐⭐      | **Pagination**            | next/previous, page numbers, dynamic pages   |
| ⭐⭐⭐      | **Sliders**               | move and verify value                        |
| ⭐⭐⭐      | **File upload**           | upload a file                                |
| ⭐⭐⭐      | **File download**         | trigger and verify download                  |
| ⭐⭐⭐      | **Browser scrolling**     | scroll to element/page                       |
| ⭐⭐⭐      | **Menus**                 | navigation menus, submenus                   |
| ⭐⭐⭐      | **Modals/Popups**         | open, interact, close                        |
| ⭐⭐⭐      | **Loading indicators**    | wait for spinner to disappear                |


## Alerts:

**Types of alerts windows we have**

| Alert type             | Purpose                      | Buttons             | Selenium method                         |
| ---------------------- | ---------------------------- | ------------------- | --------------------------------------- |
| **Simple Alert**       | Shows an information/message | OK                  | `accept()`                              |
| **Confirmation Alert** | Asks user to confirm/cancel  | OK + Cancel         | `accept()` / `dismiss()`                |
| **Prompt Alert**       | Asks user to enter input     | Input + OK + Cancel | `sendKeys()` + `accept()` / `dismiss()` |

**Simple Alert**

- Example:
```
Are you sure?
        [ OK ]

```

```JAVA
package selenium_project;

import org.openqa.selenium.Alert;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.edge.EdgeDriver;

public class AlertsDemo {

	public static void main(String[] args) throws InterruptedException {
		WebDriver driver = new EdgeDriver();
		
		driver.get("https://the-internet.herokuapp.com/javascript_alerts");
		driver.manage().window().maximize();
		
		Thread.sleep(10);
		
		WebElement myalert = driver.findElement(By.xpath("//button[normalize-space()='Click for JS Alert']"));
		
		myalert.click();
		
		Alert alert = driver.switchTo().alert();
		
		alert.accept();
		
		WebElement result = driver.findElement(By.id("result"));
		String Actualresult = result.getText();
		String Expectedresult = "You successfully clicked an alert";
		
		if (Actualresult.equals(Expectedresult)) {
			System.out.println("Test Case Passed");
		}
		else {
			System.out.println("Test Case Failed");
		}
		

	}

}

```






















