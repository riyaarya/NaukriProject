# NaukriProject
This project will involve complete testing for the Naukri website

# For the repo 
git remote add origin https://github.com/riyaarya/NaukriProject.git
git push -u origin master

# Task for 7 March 2017
1: Accessing Image Links
Image links are the links in web pages represented by an image which when clicked navigates to a different window or page.

Since they are images, we cannot use the By.linkText() and By.partialLinkText() methods because image links basically have no link texts at all.

In this case, we should resort to using either By.cssSelector or By.xpath. The first method is more preferred because of its simplicity.

In the example below, we will access the "Facebook" logo on the upper left portion of Facebook's Password Recovery page.

package newproject;
import org.openqa.selenium.By;		
import org.openqa.selenium.WebDriver;		
import org.openqa.selenium.chrome.ChromeDriver;		

public class MyClass {				
    		
    public static void main(String[] args) {									
        String baseUrl = "https://www.facebook.com/login/identify?ctx=recover";					
        System.setProperty("webdriver.chrome.driver","G:\\chromedriver.exe");					
        WebDriver driver = new ChromeDriver();					
        		
        driver.get(baseUrl);					
        //click on the "Facebook" logo on the upper left portion		
			driver.findElement(By.cssSelector("a[title=\"Go to Facebook home\"]")).click();					

			//verify that we are now back on Facebook's homepage		
			if (driver.getTitle().equals("Facebook - log in or sign up")) {							
            System.out.println("We are back at Facebook's homepage");					
        } else {			
            System.out.println("We are NOT in Facebook's homepage");					
        }		
				driver.close();		

    }		
}



----------------------------------------------------------------------------------------------------------
2: Using Attributes as Predicates

If the element is written deep within the HTML code such that the number to use for the predicate is very difficult to determine, we can use that element's unique attribute instead.

-----------------------------------------------------------------------------------------------
3: Building a Series of Multiple Actions

----------------------------------------------------------------------------------------------------------------------------
Task 
Naukri website signup
--- The drop down selector should be usedthe mouse click and then select valye from the list
--- Add resume or upload resume will cover file upload
--- On education screen add more skill will cover text link
--- other selector or drop down on the page mouse event
---- use image link click mentioned above to go to naukri home page
