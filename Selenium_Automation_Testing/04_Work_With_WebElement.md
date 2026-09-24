## Web-UI Elements to know

**Must Master**
| UI / Concept          | Level |
| --------------------- | ----- |
| Text fields / Input   | ⭐⭐⭐⭐⭐ |
| Buttons               | ⭐⭐⭐⭐⭐ |
| Links                 | ⭐⭐⭐⭐⭐ |
| Checkboxes            | ⭐⭐⭐⭐⭐ |
| Radio buttons         | ⭐⭐⭐⭐⭐ |
| Dropdowns             | ⭐⭐⭐⭐⭐ |
| Web tables            | ⭐⭐⭐⭐⭐ |
| Waits                 | ⭐⭐⭐⭐⭐ |
| Dynamic elements      | ⭐⭐⭐⭐⭐ |
| Mouse actions         | ⭐⭐⭐⭐  |
| Keyboard actions      | ⭐⭐⭐⭐  |
| Alerts                | ⭐⭐⭐⭐  |
| Frames / iFrames      | ⭐⭐⭐⭐  |
| Multiple windows/tabs | ⭐⭐⭐⭐  |

**Need to Know**
| UI / Concept       | Level |
| ------------------ | ----- |
| Date pickers       | ⭐⭐⭐⭐  |
| Auto-suggest       | ⭐⭐⭐⭐  |
| Pagination         | ⭐⭐⭐   |
| Modals/Popups      | ⭐⭐⭐   |
| Menus/Submenus     | ⭐⭐⭐   |
| Loading indicators | ⭐⭐⭐   |
| Tooltips           | ⭐⭐⭐   |
| File upload        | ⭐⭐⭐   |
| File download      | ⭐⭐⭐   |
| Browser scrolling  | ⭐⭐⭐   |
| Sliders            | ⭐⭐    |
| Drag & drop        | ⭐⭐    |


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

**Confirmation Alert**
```JAVA
WebElement obj = driver.findElement(By.xpath("//button[normalize-space()='Click for JS Confirm']"));
		obj.click();
		Alert alert = driver.switchTo().alert();
		// alert.dismiss();
		
		alert.accept();
```

**Prompt Alert**
```JAVA
WebElement obj = driver.findElement(By.xpath("//button[normalize-space()='Click for JS Prompt']"));
		obj.click();
		Alert alert = driver.switchTo().alert();
			
		alert.sendKeys("Welcome");
		alert.accept();

```


**Frames / iFrames**
HTML document embedded inside another HTML page.
```
Main Page
│
├── Login
├── Search
└── Payment
      │
      └── iframe
          ├── Card Number
          ├── Expiry
          └── CVV
```
```JAVA
package selenium_project;

import java.time.Duration;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.edge.EdgeDriver;

public class FramesDemo {

	public static void main(String[] args) {
		WebDriver driver = new EdgeDriver();
		
		driver.get("https://ui.vision/demo/webtest/frames/");
		
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(10));
		
		WebElement frame1 = driver.findElement(By.xpath("//frame[@src='frame_1.html']"));
		driver.switchTo().frame(frame1);
		driver.findElement(By.xpath("//input[@name='mytext1']")).sendKeys("Welcome");
		
		driver.switchTo().defaultContent();
		
		WebElement frame2 = driver.findElement(By.xpath("//frame[@src='frame_2.html']"));
		driver.switchTo().frame(frame2);
		driver.findElement(By.xpath("//input[@name='mytext2']")).sendKeys("Welcome");
		
		driver.switchTo().defaultContent();
		
		
		WebElement frame3 = driver.findElement(By.xpath("//frame[@src='frame_3.html']"));
		driver.switchTo().frame(frame3);
		driver.switchTo().frame(0);
		driver.findElement(By.xpath("//div[@id='i6']//div[@class='AB7Lab Id5V1']")).click();
		

	}

}

```

**Drop-Downs**

1. Select Dropdowns
2. bootstrap dropdowns
3. hidden dropdowns

**1. Select Dropdowns**
- it will have the html select tag.
```JAVA
WebDriver driver = new EdgeDriver();
		driver.get("https://testautomationpractice.blogspot.com/");
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(10));
		
		WebElement country = driver.findElement(By.xpath("//select[@id='country']"));
		
		Select select = new Select(country);
		// select.selectByVisibleText("India");
		select.selectByIndex(1);
```

**2. bootstrap dropdowns**

1) Handle country dropdown with/without using Select class:
   https://phppot.com/demo/jquery-dependent-dropdown-list-countries-and-states/
   a) count total number of options
   b) print all the options
   c) select one option

2) Hidden dropdown
   Login to OrangeHRM --> pim --> employee status

3) https://testautomationpractice.blogspot.com/
   colors mult select box















