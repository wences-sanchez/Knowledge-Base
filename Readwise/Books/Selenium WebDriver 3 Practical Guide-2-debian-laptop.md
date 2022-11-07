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
- id:: 63639930-5d2a-46e4-8570-46d72f7c8d62
  
  Selenium WebDriver accepts commands using the JSON-Wire protocol (also called Client API) and sends them to a browser launched by the specific driver class (such as ChromeDriver, FirefoxDriver, or IEDriver). This is implemented through a browser-specific browser driver. It works with the following sequence:
     The driver listens to the commands from Selenium
     It converts these commands into the browser's native API
     The driver takes the result of native commands and sends the result back to Selenium: #flashcard
-
### Selenium Server
- id:: 63639930-713b-4ac0-bfe4-5d3a56d71549
   What does Selenium Server do? #flashcard 
    Selenium Server allows us to run tests on browser instances running on remote machines and in parallel, thus spreading a load of testing across several machines.
-
### Selenium IDE
- id:: 63639930-c5c5-4ef3-ad01-e9586ba4f116
   What is Selenium IDE? #flashcard 
    Selenium IDE is a Firefox add-on that allows users to record, edit, debug, and play back tests captured in the Selenese format, which was introduced in the Selenium Core version.
-
### WebElements
- id:: 63639930-a149-47e3-9709-ae4b0a7abcce
   What are the WebElements? #flashcard 
    A web page is composed of many different types of HTML elements, such as links, textboxes, dropdown buttons, a body, labels, and forms. These are called WebElements in the context of WebDriver.
-
### The findElement method
- id:: 63639930-6e6a-4806-98cd-f227c54159e6
   Declaration of function to get a WebElement. #flashcard 
    WebElement findElement(By by)
-
### Using the By locating mechanism
- id:: 63639930-92c7-40bd-8bee-536d52f3bf53
   What are the eight different ways to identify a WebElement in Selenium? #flashcard 
    There are eight different locating mechanisms; that is, eight different ways to identify
     an HTML element on a web page. They are located by ID, Name, ClassName, TagName, LinkText, PartialLinkText, XPath, and CSS Selector.
-
### The By.xpath() method
- id:: 63639930-72ff-4cd8-8bb9-da82e1a9bf58
   What does XPath stand for? #flashcard 
    XPath is a short name for the XML path, the query language used for searching XML documents. The HTML for our web page is also one form of the XML document. So, in order to identify an element on an HTML page, we need to use a specific XPath syntax
-
- id:: 63639930-001f-4cf6-979d-b6a4ba3d81c5
   Syntax of XPath in Selenium #flashcard 
    in order to identify an element on an HTML page, we need to use a specific XPath syntax:
     The root element is identified as //.
     To identify all the div elements, the syntax will be //div.
     To identify the link tags that are within the div element, the syntax will be //div/a.
     To identify all the elements with a tag, we use *. The syntax will be //div/*.
     To identify all the div elements that are at three levels down from the root, we can use //*/*/div.
     To identify specific elements, we use attribute values of those elements, such as //*/div/a[@id='attrValue'], which will return the anchor element. This element is at the third level from the root within a div element and has an id value of attrValue
-
- id:: 63639930-e909-4be3-b5a3-58d39ac62e4f
   Drawbacks of XPath #flashcard 
    One disadvantage of using XPath is that it is costly in terms of time. For every element to be identified, WebDriver actually scans through the entire page, which is very time consuming, and too much usage of XPath in your test script will actually make it too slow to execute.
-
### The sendKeys() method
- id:: 63639930-bcb2-4ce1-94cf-2cc0608fbd9a
   How can you type a special key in WebElement.sendKeys() ? #flashcard 
    if you want to type in some special keys, such as Backspace, Enter, Tab, or Shift, we need to use a special enum class of WebDriver, named Keys.
-
### Using Headless Mode
- id:: 63639930-33e7-4117-88c2-95662391a10a
   How can you silence the UI in Firefox browser using Selenium? #flashcard 
    FirefoxOptions firefoxOptions = new FirefoxOptions();
     firefoxOptions.setHeadless(true);
     driver = new FirefoxDriver(firefoxOptions);
-
### Stream.filter()
- id:: 63639930-7748-43f8-aa91-291a52210a20
  
  stream.filter( item -> item.startsWith("E") ); #flashcard
-
### Stream.sort()
- id:: 63639930-bbcb-43be-865c-edd7ec63b435
  
  languages.stream().sorted(); #flashcard
-
### Stream.map()
- id:: 63639930-df79-4cef-bd79-8b62ff68d88e
  
  languages.stream().map(item -> item.toUpperCase()); #flashcard
-
### Stream.collect()
- id:: 63639930-ae93-45ba-ae88-882565b4ae7c
   About collect( ) #flashcard 
    When the collect() method is invoked, filtering and mapping will take place, and the object resulting from those actions will be collected.
-
- id:: 63639930-043d-4949-9008-14a89f8c7e3a
   Example of map and collect #flashcard 
    List<String> upperCaseLanguages = languages.stream()
     .map(item -> item.toUpperCase())
     .collect(Collectors.toList());
     System.out.println(upperCaseLanguages);
-
### Stream.min() and Stream.max()
- id:: 63639930-1994-4d0c-9abb-76e9eb88db80
   Example of comparing a stream #flashcard 
    Product product = searchResult.stream()
     .min(Comparator.comparing(item -> item.getPrice()))
     .get();
     System.out.println("The product with lowest price is " + product.getName());
-
### Filtering and counting WebElements
- id:: 63639930-cc8a-49c6-b7c5-ca873c89d5a6
   Print the number of displayed items using streams #flashcard 
    long count = links.stream().filter(item -> item.isDisplayed()).count();
-
### Using the Map function to get the text value from elements
- id:: 63639930-38ff-44b5-99e5-fe8bb7e84739
   A way of getting text from WebElements with streams. #flashcard 
    List<String> productNames = searchItems.stream()
     .map(WebElement::getText)
     .collect(Collectors.toList());
-
### Filtering and performing actions on WebElements
- id:: 63639930-13c4-4c11-b75d-b26d9ca1ea00
   Find the first item using streams #flashcard 
    WebElement product = searchItems.stream()
     .filter(item -> item.getText().equalsIgnoreCase("MADISON EARBUDS"))
     .findFirst()
     .get();
-
### Taking screenshots
- id:: 63639930-a522-4971-aca7-0cf21f4f3175
   How to make a screenshot in Selenium #flashcard 
    File scrFile = ((TakesScreenshot) driver).getScreenshotAs(OutputType.FILE);
     FileUtils.copyFile(scrFile, new File("./target/screenshot.png"));
-
### Switching among windows
- id:: 63639930-f311-4975-a9f6-428c4b7d40eb
   How to change to #flashcard 
    driver.switchTo().window(firstWindow);
-
### Switching between frames
- id:: 63639930-88fb-408e-8d36-3e2bf3986ec5
  
  // First Frame
     driver.switchTo().frame(0); #flashcard  #code
-
- id:: 63639930-e908-4b9b-8b01-e692a8227227
  
  driver.switchTo().defaultContent(); #flashcard
-
### Waiting for WebElements to load
- id:: 63639930-4ae1-460e-8c7f-b499b16966d1
  
  There are two ways by which you can make the WebDriver wait for WebElement. They are Implicit Wait Time and Explicit Wait Time. Implicit timeouts are common to all the WebElements and have a global timeout period associated with them, but the explicit timeouts can be configured to individual WebElements. Let's discuss each of them here. #flashcard
-
### Implicit wait time
- id:: 63639930-a581-4d0c-85da-76283b621452
  
  driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS); #flashcard
-
### Explicit wait time
- id:: 63639930-6749-49a4-9ce0-ecb20400d257
  
  WebElement searchBox = (new WebDriverWait(driver, 20))
     .until((ExpectedCondition<WebElement>) d -> d.findElement(By.name("q"))); #flashcard
-
### Using cloud-based grids for cross-browser testing
- id:: 63639930-4508-4233-afe8-eca0a7445353
   To use it in cloud #flashcard 
    Let's set up and run a test with Sauce Labs. You need a free Sauce Labs account, to begin with. Register for a free account on Sauce Labs at https://saucelabs.com/
-
### Using the @FindBy annotation
- id:: 63639930-611a-495d-bfe6-383d661630ec
  
  @FindBy(id="user_login")
     WebElement userId; #flashcard
-
### Understanding PageFactory
### Always look for implied services
- id:: 63639930-5693-42bc-9af1-830f52f76cad
  
  Some of a page's services can be identified very clearly on it. And there are some services that are not visible on the page but that are implied. For example, in the All Posts page, we have identified five services just by looking at the page. But let's say your test case wants to know the count of existing posts #flashcard
-
### The AllPostsPage PageObject
- id:: 63639930-2210-4982-b473-84e82939a57f
  
  Now, as you can see in the AllPostsPage PageObject, we have instantiated the AddNewPage PageObject in the createNewPost() method. Thus, we are using one PageObject with another and keeping the behavior as close as possible to the target application. #flashcard
-
### Understanding loadable components
- id:: 63639930-dae3-4b6b-83a1-20e5e345b952
  
  @Override
     protected void load() {
     driver.get("http://demo-blog.seleniumacademy.com/wp/wp-admin");
     }
     @Override
     protected void isLoaded() throws Error {
     Assert.assertTrue(driver.getCurrentUrl().contains("wp-admin"));
     } #flashcard
-
- id:: 63639930-850d-4bd7-bd7e-95b69b7b1109
   Get() of loadable page #flashcard 
    AdminLoginPageUsingLoadableComponent loginPage = new AdminLoginPageUsingLoadableComponent(driver).get();
     The get() method from the LoadableComponent class will make sure the component is loaded by invoking the isLoaded() method
-
### Automating iOS Application tests
- id:: 63639930-3a6a-4fca-94e7-db802511af29
  
  After the command is executed against your app on the simulator or device, the target app sends the response to XCTest or UI Automation Instrument, which is transferred to Appium in the JavaScript response format. Appium translates the responses into Selenium WebDriver JSON wire protocol responses and sends them back to your test script. #flashcard
-