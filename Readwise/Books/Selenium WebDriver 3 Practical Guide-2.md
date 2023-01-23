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
- id:: 63c66a23-5f8c-4f51-af8e-8710fc369090
  
  Selenium WebDriver accepts commands using the JSON-Wire protocol (also called Client API) and sends them to a browser launched by the specific driver class (such as ChromeDriver, FirefoxDriver, or IEDriver). This is implemented through a browser-specific browser driver. It works with the following sequence:
     The driver listens to the commands from Selenium
     It converts these commands into the browser's native API
     The driver takes the result of native commands and sends the result back to Selenium: #flashcard
-
### Selenium Server
- id:: 63c66a23-4c4b-42c5-9e43-1c04a7701da4
   What does Selenium Server do? #flashcard 
    Selenium Server allows us to run tests on browser instances running on remote machines and in parallel, thus spreading a load of testing across several machines.
-
### Selenium IDE
- id:: 63c66a23-d28f-40d7-beb0-c6f3831b0486
   What is Selenium IDE? #flashcard 
    Selenium IDE is a Firefox add-on that allows users to record, edit, debug, and play back tests captured in the Selenese format, which was introduced in the Selenium Core version.
-
### WebElements
- id:: 63c66a23-0e88-407a-aa33-80a4d72a770d
   What are the WebElements? #flashcard 
    A web page is composed of many different types of HTML elements, such as links, textboxes, dropdown buttons, a body, labels, and forms. These are called WebElements in the context of WebDriver.
-
### The findElement method
- id:: 63c66a23-0e9f-42ae-b984-f60d54081fd7
   Declaration of function to get a WebElement. #flashcard 
    WebElement findElement(By by)
-
### Using the By locating mechanism
- id:: 63c66a23-487b-4fc5-ba0a-aeddc953b519
   What are the eight different ways to identify a WebElement in Selenium? #flashcard 
    There are eight different locating mechanisms; that is, eight different ways to identify
     an HTML element on a web page. They are located by ID, Name, ClassName, TagName, LinkText, PartialLinkText, XPath, and CSS Selector.
-
### The By.xpath() method
- id:: 63c66a23-45f3-463b-8327-37132e60d77b
   What does XPath stand for? #flashcard 
    XPath is a short name for the XML path, the query language used for searching XML documents. The HTML for our web page is also one form of the XML document. So, in order to identify an element on an HTML page, we need to use a specific XPath syntax
-
- id:: 63c66a23-b81f-4391-95e4-b659019fb193
   Syntax of XPath in Selenium #flashcard 
    in order to identify an element on an HTML page, we need to use a specific XPath syntax:
     The root element is identified as //.
     To identify all the div elements, the syntax will be //div.
     To identify the link tags that are within the div element, the syntax will be //div/a.
     To identify all the elements with a tag, we use *. The syntax will be //div/*.
     To identify all the div elements that are at three levels down from the root, we can use //*/*/div.
     To identify specific elements, we use attribute values of those elements, such as //*/div/a[@id='attrValue'], which will return the anchor element. This element is at the third level from the root within a div element and has an id value of attrValue
-
- id:: 63c66a23-8835-430c-8b95-c7dc58adcc71
   Drawbacks of XPath #flashcard 
    One disadvantage of using XPath is that it is costly in terms of time. For every element to be identified, WebDriver actually scans through the entire page, which is very time consuming, and too much usage of XPath in your test script will actually make it too slow to execute.
-
### The sendKeys() method
- id:: 63c66a23-8ba2-4582-af06-11b10680c470
   How can you type a special key in WebElement.sendKeys() ? #flashcard 
    if you want to type in some special keys, such as Backspace, Enter, Tab, or Shift, we need to use a special enum class of WebDriver, named Keys.
-
### Using Headless Mode
- id:: 63c66a23-f500-4336-9308-0113f573eae1
   How can you silence the UI in Firefox browser using Selenium? #flashcard 
    FirefoxOptions firefoxOptions = new FirefoxOptions();
     firefoxOptions.setHeadless(true);
     driver = new FirefoxDriver(firefoxOptions);
-
### Stream.filter()
- id:: 63c66a23-9de6-4520-a65a-9539335dd655
  
  stream.filter( item -> item.startsWith("E") ); #flashcard
-
### Stream.sort()
- id:: 63c66a23-f40a-4142-bc62-5997e8f67c9f
  
  languages.stream().sorted(); #flashcard
-
### Stream.map()
- id:: 63c66a23-8253-431d-9998-011387ddd10c
  
  languages.stream().map(item -> item.toUpperCase()); #flashcard
-
### Stream.collect()
- id:: 63c66a23-bc0b-4716-97af-01ee28f8c5c3
   About collect( ) #flashcard 
    When the collect() method is invoked, filtering and mapping will take place, and the object resulting from those actions will be collected.
-
- id:: 63c66a23-edd9-434e-a5b3-ebab99434ddd
   Example of map and collect #flashcard 
    List<String> upperCaseLanguages = languages.stream()
     .map(item -> item.toUpperCase())
     .collect(Collectors.toList());
     System.out.println(upperCaseLanguages);
-
### Stream.min() and Stream.max()
- id:: 63c66a23-9869-41b9-8307-c13537a2db95
   Example of comparing a stream #flashcard 
    Product product = searchResult.stream()
     .min(Comparator.comparing(item -> item.getPrice()))
     .get();
     System.out.println("The product with lowest price is " + product.getName());
-
### Filtering and counting WebElements
- id:: 63c66a23-fbbb-48e6-a08e-55104bb34cb7
   Print the number of displayed items using streams #flashcard 
    long count = links.stream().filter(item -> item.isDisplayed()).count();
-
### Using the Map function to get the text value from elements
- id:: 63c66a23-1c86-42bc-a54e-eb62d51bcc17
   A way of getting text from WebElements with streams. #flashcard 
    List<String> productNames = searchItems.stream()
     .map(WebElement::getText)
     .collect(Collectors.toList());
-
### Filtering and performing actions on WebElements
- id:: 63c66a23-dcd3-4dc5-9c2b-f8c08fc05511
   Find the first item using streams #flashcard 
    WebElement product = searchItems.stream()
     .filter(item -> item.getText().equalsIgnoreCase("MADISON EARBUDS"))
     .findFirst()
     .get();
-
### Taking screenshots
- id:: 63c66a23-6d8d-4450-bd5c-530b2bfe7098
   How to make a screenshot in Selenium #flashcard 
    File scrFile = ((TakesScreenshot) driver).getScreenshotAs(OutputType.FILE);
     FileUtils.copyFile(scrFile, new File("./target/screenshot.png"));
-
### Switching among windows
- id:: 63c66a23-8e75-4e5d-a181-1bcfaaec041b
   How to change to #flashcard 
    driver.switchTo().window(firstWindow);
-
### Switching between frames
- id:: 63c66a23-60bf-4453-a943-edc715a73e36
  
  // First Frame
     driver.switchTo().frame(0); #flashcard  #code
-
- id:: 63c66a23-7080-42f1-872b-be49477014e1
  
  driver.switchTo().defaultContent(); #flashcard
-
### Waiting for WebElements to load
- id:: 63c66a23-b71c-4d38-abb3-8cff1a094509
  
  There are two ways by which you can make the WebDriver wait for WebElement. They are Implicit Wait Time and Explicit Wait Time. Implicit timeouts are common to all the WebElements and have a global timeout period associated with them, but the explicit timeouts can be configured to individual WebElements. Let's discuss each of them here. #flashcard
-
### Implicit wait time
### Explicit wait time
- id:: 63c66a23-c677-4fa5-a7df-0620a2391895
  
  WebElement searchBox = (new WebDriverWait(driver, 20))
     .until((ExpectedCondition<WebElement>) d -> d.findElement(By.name("q"))); #flashcard
-
### Using cloud-based grids for cross-browser testing
- id:: 63c66a23-07e5-42db-9e0f-a072cfd6db3e
   To use it in cloud #flashcard 
    Let's set up and run a test with Sauce Labs. You need a free Sauce Labs account, to begin with. Register for a free account on Sauce Labs at https://saucelabs.com/
-
### Using the @FindBy annotation
- id:: 63c66a23-6069-4ae0-96c0-24c426ceeba0
  
  @FindBy(id="user_login")
     WebElement userId; #flashcard
-
### Understanding PageFactory
### Always look for implied services
- id:: 63c66a23-8c65-415e-8eed-f84a2bc8ab4b
  
  Some of a page's services can be identified very clearly on it. And there are some services that are not visible on the page but that are implied. For example, in the All Posts page, we have identified five services just by looking at the page. But let's say your test case wants to know the count of existing posts #flashcard
-
### The AllPostsPage PageObject
- id:: 63c66a23-3ce6-4a23-be20-2caa8c97a140
  
  Now, as you can see in the AllPostsPage PageObject, we have instantiated the AddNewPage PageObject in the createNewPost() method. Thus, we are using one PageObject with another and keeping the behavior as close as possible to the target application. #flashcard
-
### Understanding loadable components
- id:: 63c66a23-87c4-4a1c-9a52-5a2f72effa99
  
  @Override
     protected void load() {
     driver.get("http://demo-blog.seleniumacademy.com/wp/wp-admin");
     }
     @Override
     protected void isLoaded() throws Error {
     Assert.assertTrue(driver.getCurrentUrl().contains("wp-admin"));
     } #flashcard
-
- id:: 63c66a23-8638-43b4-90a0-cda71349f254
   Get() of loadable page #flashcard 
    AdminLoginPageUsingLoadableComponent loginPage = new AdminLoginPageUsingLoadableComponent(driver).get();
     The get() method from the LoadableComponent class will make sure the component is loaded by invoking the isLoaded() method
-
### Automating iOS Application tests
- id:: 63c66a23-880e-4776-8c1c-5182aab58588
  
  After the command is executed against your app on the simulator or device, the target app sends the response to XCTest or UI Automation Instrument, which is transferred to Appium in the JavaScript response format. Appium translates the responses into Selenium WebDriver JSON wire protocol responses and sends them back to your test script. #flashcard
-