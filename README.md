import org.openqa.selenium.By;
import org.openqa.selenium.JavascriptExecutor;
import org.openqa.selenium.Keys;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.interactions.Actions;
import org.openqa.selenium.support.ui.Select;

public class FinalProject2 {

	public static void main(String[] args)throws InterruptedException {
		System.setProperty("webdriver.chrome.drver", "C:\\Users\\Windows 10\\eclipse-workspace\\Selenuim_Project\\chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.get("https://www.jiomart.com/");
		driver.manage().window().maximize();
		WebElement x = driver.findElement(By.xpath("//*[@id=\"autocomplete-0-input\"]"));
		x.sendKeys("Refrigerator");
		x.sendKeys(Keys.RETURN);
		Thread.sleep(2000);
		driver.findElement(By.xpath("//*[@id=\"algolia_hits\"]/div/div/ol/li[5]/a/div[2]/div[2]/div/div[2]")).click();
		Thread.sleep(1000);
		driver.findElement(By.xpath("/html/body/main/section/section[2]/div[1]/div/div[1]/div/div[3]/div[2]/button")).click();
		Thread.sleep(1000);
		driver.findElement(By.xpath("//*[@id=\"elec_addon_dialog\"]/div[2]/div/div[3]/div[2]/div[1]/button")).click();
		Thread.sleep(3000);
		WebElement m = driver.findElement(By.xpath("//*[@id=\"btn_minicart\"]/img"));
	     m.click();
	    Thread.sleep(3000);
	    driver.findElement(By.xpath("//*[@id=\"page-header\"]/div/div/div[2]/a/img")).click();
	    Thread.sleep(2000);
	    Actions mouse = new Actions(driver);
	    WebElement electronics = driver.findElement(By.xpath("//*[@id=\"nav_link_4\"]"));
	    mouse.moveToElement(electronics).click().build().perform();
	    Thread.sleep(2000);
	    driver.findElement(By.xpath("//*[@id=\"plp-category-desk\"]/div[4]/div/div[1]/div[2]/div/span")).click();
	    Thread.sleep(2000);
	    driver.findElement(By.xpath("//*[@id=\"category-719\"]/div[1]/div/div/a")).click();
	    Thread.sleep(2000);
	    driver.findElement(By.xpath("//*[@id=\"brand_filter\"]/div/ul/li[4]/div/label/span")).click();
	    Thread.sleep(2000);
	    driver.findElement(By.xpath("//*[@id=\"algolia_facet_laptop_display_screen_size_diagonal\"]/div/ul/li[4]/div/label/span")).click();
	    Thread.sleep(3000);
	    driver.findElement(By.xpath("/html/body/main/section/div[1]/div/div[2]/div[2]/div/div/div/ol/li/a/div[2]/div[1]/div/div[1]/img")).click();
	    Thread.sleep(3000);
	    driver.findElement(By.xpath("/html/body/main/section/section[2]/div[1]/div/div[1]/div/div[3]/div[2]/button")).click();
	    Thread.sleep(3000);
	    driver.findElement(By.xpath("//*[@id=\"btn_minicart\"]/img")).click();
	    Thread.sleep(3000);
	    driver.findElement(By.xpath("//*[@id=\"page-header\"]/div/div/div[2]/a/img")).click();
	    WebElement mainMenu = driver.findElement(By.xpath("/html/body/header/section[2]/div/nav/ul/li[3]/a"));
	    Thread.sleep(2000);
	    Actions actions = new Actions(driver);
	    actions.moveToElement(mainMenu);
	    Thread.sleep(2000);
	    WebElement subMenu = driver.findElement(By.xpath("//*[@id=\"nav_link_7489\"]"));
	    actions.moveToElement(subMenu);
	    actions.click().build().perform();
	    Thread.sleep(2000);
	    driver.findElement(By.xpath("//*[@id=\"mstar_box\"]/div[3]/a/div[2]/div[2]/div/div[1]")).click();
	    Thread.sleep(2000);
	    driver.findElement(By.xpath("/html/body/main/section/section[2]/div[1]/div/div[1]/div/div[3]/div/button")).click();
	    Thread.sleep(2000);
		WebElement mainMenu2 = driver.findElement(By.xpath("//*[@id=\"btn_minicart\"]/img"));
        Actions action = new Actions(driver);
        actions.moveToElement(mainMenu2);
        Thread.sleep(2000);
        WebElement subMenu2 = driver.findElement(By.xpath("//*[@id=\"minicart_proceed\"]"));
        actions.moveToElement(subMenu2);
        actions.click().build().perform();
        Thread.sleep(3000);
        ((JavascriptExecutor) driver).executeScript("window.scrollBy(0,500);");
        Thread.sleep(3000);
        driver.close();
	    
	    
	}
}
