# Selenium-3
Table2
package selpractice;


import java.util.List;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.locators.RelativeLocator;

public class Assignment {

	public static void main(String[] args) throws InterruptedException {
		// TODO Auto-generated method stub
		WebDriver dr = new ChromeDriver();
		dr.get("https://vinothqaacademy.com/webtable/");
		Thread.sleep(10000);
		WebElement dsr = dr.findElement(By.cssSelector("button#deleteBtn"));
		WebElement button = dr.findElement(RelativeLocator.with(By.tagName("table"))
				.below(dsr));
		
		
		List<WebElement> rows = button.findElements(By.tagName("tr"));
		for(WebElement row:rows) {
			List<WebElement> datas = row.findElements(By.tagName("td"));
			for(WebElement data:datas) {
				System.out.print(data.getText()+" ");
			}
			System.out.println();
		}
		dr.quit();
			
		}

}

output:
John Doe Project Manager john.doe@example.com New York Management 
 Jane Smith Software Engineer jane.smith@example.com Manchester Engineering 
 Vinoth R Automation Architect vinoth.r@example.com Chennai Quality Assurance 
 Samuel Johnson UI/UX Designer samuel.johnson@example.com London Design 
 Linda Wilson Business Analyst linda.wilson@example.com Chicago Analysis 
 David Martinez Scrum Master david.martinez@example.com Miami Agile 
 Sarah Lee Database Administrator sarah.lee@example.com Boston Database 
 Anand Jeff DevOps Engineer anand@example.com Toronto Operations 
 Chris Evans Technical Lead chris.evans@example.com Austin Technical 
 Jessica Taylor Product Owner jessica.taylor@example.com Seattle Product 

