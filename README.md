package Salenium.it;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

  public class E_Commerce {
	
	WebDriver driver;
	
	public void LaunchAut() throws InterruptedException
	{
		driver=new ChromeDriver();
		
		driver.get("https://signin.ebay.com/ws/eBayISAPI.dll?SignIn&sgfl=gh&ru=https%3A%2F%2Fwww.ebay.com%2F");
		
		Thread.sleep(2000);
		
		driver.manage().window().maximize();
	}
	
    public void Sendkeys() throws InterruptedException
	
	{
		
		driver.findElement(By.id("userid")).sendKeys("anilyadavcse104@gmail.com");
		
	    Thread.sleep(2000);
	     
	    driver.findElement(By.id("signin-continue-btn")).click();
	     
	    Thread.sleep(2000);
		
		driver.findElement(By.id("pass")).sendKeys("Anilyadav@1989");
		
		Thread.sleep(2000);
		
		driver.findElement(By.id("sgnBt")).click();
	}

      public void CurrentUrl()
   {
    	  
	     String url= driver.getCurrentUrl();
	
	     System.out.println("The Url is :"+url);
   }
      
      public void GetTitle()
  	
  	{
  		String title = driver.getTitle();
  		
  		System.out.println("The title is :" +title);
  		
  	}
      
      public void Senddata()
  	
  	{
  		driver.findElement(By.id("gh-ac")).sendKeys("iphone 15 pro max");
  		
  		driver.findElement(By.id("gh-btn")).click();
  	}
      
    

	
	public static void main(String[] args) throws InterruptedException {
		
		E_Commerce obj= new E_Commerce();
		
		obj.LaunchAut();
		
		obj.Sendkeys();
		
		obj.CurrentUrl();
		
		obj.GetTitle();
		
		obj.Senddata();
		
