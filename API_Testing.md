# REST API Collection Documentation

### 1. GET /api/v1/restaurants
* **Description:** Retrieve operational restaurants list.
* **Expected Response:** `200 OK` | **Status:** Not Executed

### 2. POST /api/v1/auth/login
* **Description:** Authenticate user and issue JWT token.
* **Request Body:**
  ```json
  {
    "email": "standard.user@foodore.test",
    "password": "P@ssword2026!"
  }
3. POST /api/v1/orders
Description: Submit new food order.

Headers: Authorization: Bearer <token>

Expected Response: 201 Created | Status: Not Executed

4. POST /api/v1/orders (Negative Verification)
Description: Order placement without Authorization header.

Expected Response: 401 Unauthorized | Status: Not Executed
### 7. `automation/FoodoreLoginTest.java`

```java
package com.foodore.qa.tests;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.testng.Assert;
import org.testng.annotations.AfterMethod;
import org.testng.annotations.BeforeMethod;
import org.testng.annotations.Test;
import java.time.Duration;

public class FoodoreLoginTest {

    private WebDriver driver;
    private final String BASE_URL = "https://example.test"; 

    @BeforeMethod
    public void setUp() {
        driver = new ChromeDriver();
        driver.manage().window().maximize();
        driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(10));
    }

    @Test(description = "TC-004: Validate user login with valid credentials")
    public void testValidUserLogin() {
        driver.get(BASE_URL + "/login");

        WebElement emailInput = driver.findElement(By.id("email"));
        WebElement passwordInput = driver.findElement(By.id("password"));
        WebElement loginButton = driver.findElement(By.id("login-submit"));

        emailInput.sendKeys("standard.user@foodore.test");
        passwordInput.sendKeys("P@ssword2026!");
        loginButton.click();

        WebElement profileHeader = driver.findElement(By.id("user-profile-header"));
        Assert.assertTrue(profileHeader.isDisplayed(), "Login failed: User profile header not displayed.");
    }

    @AfterMethod
    public void tearDown() {
        if (driver != null) {
            driver.quit();
        }
    }
}
