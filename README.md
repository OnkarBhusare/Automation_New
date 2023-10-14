# Automation_New
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class EmailAutomationTest {
    public static void main(String[] args) {
        // Set the path to the ChromeDriver executable
        System.setProperty("webdriver.chrome.driver", "path_to_chromedriver/chromedriver.exe");

        // Create a new instance of the ChromeDriver
        WebDriver driver = new ChromeDriver();

        // Navigate to a website with an email input form
        driver.get("https://www.example.com");

        // Find the email input field by its name attribute
        WebElement emailInput = driver.findElement(By.name("email"));

        // Enter an email address into the input field
        emailInput.sendKeys("your.email@example.com");

        // Find and click the submit button
        WebElement submitButton = driver.findElement(By.id("submit-button"));
        submitButton.click();

        // Close the browser
        driver.quit();
    }
}
