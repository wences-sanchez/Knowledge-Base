# Selenium WebDriver 3 Practical Guide

deck:: [[O'Reilly-Learning::Selenium WebDriver 3 Practical Guide]]\
author:: [[None]]\
full-title:: "Selenium WebDriver 3 Practical Guide"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/covers/9781788999762/)

## Highlights
### Selenium WebDriver
- 

Selenium WebDriver accepts commands using the JSON-Wire protocol (also called Client API) and sends them to a browser launched by the specific driver class (such as ChromeDriver, FirefoxDriver, or IEDriver). This is implemented through a browser-specific browser driver. It works with the following sequence:
     The driver listens to the commands from Selenium
     It converts these commands into the browser's native API
     The driver takes the result of native commands and sends the result back to Selenium: #flashcard 


    
-
### Selenium Server
- 
 What does Selenium Server do? #flashcard 
    Selenium Server allows us to run tests on browser instances running on remote machines and in parallel, thus spreading a load of testing across several machines.

    
-
### Selenium IDE
- 
 What is Selenium IDE? #flashcard 
    Selenium IDE is a Firefox add-on that allows users to record, edit, debug, and play back tests captured in the Selenese format, which was introduced in the Selenium Core version.

    
-
### WebElements
- 
 What are the WebElements? #flashcard 
    A web page is composed of many different types of HTML elements, such as links, textboxes, dropdown buttons, a body, labels, and forms. These are called WebElements in the context of WebDriver.

    
-
### The findElement method
- 
 Declaration of function to get a WebElement. #flashcard 
    WebElement findElement(By by)

    
-
### Using the By locating mechanism
- 
 What are the eight different ways to identify a WebElement in Selenium? #flashcard 
    There are eight different locating mechanisms; that is, eight different ways to identify
     an HTML element on a web page. They are located by ID, Name, ClassName, TagName, LinkText, PartialLinkText, XPath, and CSS Selector.

    
-
### The By.xpath() method
- 
 What does XPath stand for? #flashcard 
    XPath is a short name for the XML path, the query language used for searching XML documents. The HTML for our web page is also one form of the XML document. So, in order to identify an element on an HTML page, we need to use a specific XPath syntax

    
-
- 
 Syntax of XPath in Selenium #flashcard 
    in order to identify an element on an HTML page, we need to use a specific XPath syntax:
     The root element is identified as //.
     To identify all the div elements, the syntax will be //div.
     To identify the link tags that are within the div element, the syntax will be //div/a.
     To identify all the elements with a tag, we use *. The syntax will be //div/*.
     To identify all the div elements that are at three levels down from the root, we can use //*/*/div.
     To identify specific elements, we use attribute values of those elements, such as //*/div/a[@id='attrValue'], which will return the anchor element. This element is at the third level from the root within a div element and has an id value of attrValue

    
-
- 
 Drawbacks of XPath #flashcard 
    One disadvantage of using XPath is that it is costly in terms of time. For every element to be identified, WebDriver actually scans through the entire page, which is very time consuming, and too much usage of XPath in your test script will actually make it too slow to execute.

    
-
### The sendKeys() method
- 
 How can you type a special key in WebElement.sendKeys() ? #flashcard 
    if you want to type in some special keys, such as Backspace, Enter, Tab, or Shift, we need to use a special enum class of WebDriver, named Keys.

    
-
### Using Headless Mode
- 
 How can you silence the UI in Firefox browser using Selenium? #flashcard 
    FirefoxOptions firefoxOptions = new FirefoxOptions();
     firefoxOptions.setHeadless(true);
     driver = new FirefoxDriver(firefoxOptions);

    
-
### Stream.filter()
- 

stream.filter( item -> item.startsWith("E") ); #flashcard 


    
-
### Stream.sort()
- 

languages.stream().sorted(); #flashcard 


    
-
### Stream.map()
- 

languages.stream().map(item -> item.toUpperCase()); #flashcard 


    
-
### Stream.collect()
- 
 About collect( ) #flashcard 
    When the collect() method is invoked, filtering and mapping will take place, and the object resulting from those actions will be collected.

    
-
- 
 Example of map and collect #flashcard 
    List<String> upperCaseLanguages = languages.stream()
     .map(item -> item.toUpperCase())
     .collect(Collectors.toList());
     System.out.println(upperCaseLanguages);

    
-
### Stream.min() and Stream.max()
- 
 Example of comparing a stream #flashcard 
    Product product = searchResult.stream()
     .min(Comparator.comparing(item -> item.getPrice()))
     .get();
     System.out.println("The product with lowest price is " + product.getName());

    
-
### Filtering and counting WebElements
- 
 Print the number of displayed items using streams #flashcard 
    long count = links.stream().filter(item -> item.isDisplayed()).count();

    
-
### Using the Map function to get the text value from elements
- 
 A way of getting text from WebElements with streams. #flashcard 
    List<String> productNames = searchItems.stream()
     .map(WebElement::getText)
     .collect(Collectors.toList());

    
-
### Filtering and performing actions on WebElements
- 
 Find the first item using streams #flashcard 
    WebElement product = searchItems.stream()
     .filter(item -> item.getText().equalsIgnoreCase("MADISON EARBUDS"))
     .findFirst()
     .get();

    
-
### Taking screenshots
- 
 How to make a screenshot in Selenium #flashcard 
    File scrFile = ((TakesScreenshot) driver).getScreenshotAs(OutputType.FILE);
     FileUtils.copyFile(scrFile, new File("./target/screenshot.png"));

    
-
### Switching among windows
- 
 How to change to #flashcard 
    driver.switchTo().window(firstWindow);

    
-
### Switching between frames
- 

// First Frame
     driver.switchTo().frame(0); #flashcard  #code 


    
-
- 

driver.switchTo().defaultContent(); #flashcard 


    
-
### Waiting for WebElements to load
- 

There are two ways by which you can make the WebDriver wait for WebElement. They are Implicit Wait Time and Explicit Wait Time. Implicit timeouts are common to all the WebElements and have a global timeout period associated with them, but the explicit timeouts can be configured to individual WebElements. Let's discuss each of them here. #flashcard 


    
-
### Implicit wait time
- 

driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS); #flashcard 


    
-
### Explicit wait time
- 

WebElement searchBox = (new WebDriverWait(driver, 20))
     .until((ExpectedCondition<WebElement>) d -> d.findElement(By.name("q"))); #flashcard 


    
-
### Using cloud-based grids for cross-browser testing
- 
 To use it in cloud #flashcard 
    Let's set up and run a test with Sauce Labs. You need a free Sauce Labs account, to begin with. Register for a free account on Sauce Labs at https://saucelabs.com/

    
-
### Using the @FindBy annotation
- 

@FindBy(id="user_login")
     WebElement userId; #flashcard 


    
-
### Understanding PageFactory
### Always look for implied services
- 

Some of a page's services can be identified very clearly on it. And there are some services that are not visible on the page but that are implied. For example, in the All Posts page, we have identified five services just by looking at the page. But let's say your test case wants to know the count of existing posts #flashcard 


    
-
### The AllPostsPage PageObject
- 

Now, as you can see in the AllPostsPage PageObject, we have instantiated the AddNewPage PageObject in the createNewPost() method. Thus, we are using one PageObject with another and keeping the behavior as close as possible to the target application. #flashcard 


    
-
### Understanding loadable components
- 

@Override
     protected void load() {
     driver.get("http://demo-blog.seleniumacademy.com/wp/wp-admin");
     }
     @Override
     protected void isLoaded() throws Error {
     Assert.assertTrue(driver.getCurrentUrl().contains("wp-admin"));
     } #flashcard 


    
-
- 
 Get() of loadable page #flashcard 
    AdminLoginPageUsingLoadableComponent loginPage = new AdminLoginPageUsingLoadableComponent(driver).get();
     The get() method from the LoadableComponent class will make sure the component is loaded by invoking the isLoaded() method

    
-
### Automating iOS Application tests
- 

After the command is executed against your app on the simulator or device, the target app sends the response to XCTest or UI Automation Instrument, which is transferred to Appium in the JavaScript response format. Appium translates the responses into Selenium WebDriver JSON wire protocol responses and sends them back to your test script. #flashcard 


    
-
