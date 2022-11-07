# Learn Selenium

deck:: [[O'Reilly-Learning::Learn Selenium]]\
author:: [[None]]\
full-title:: "Learn Selenium"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/library/view/learn-selenium/9781838983048/ibis_generated_cover_thumbnail.jpg)
## Highlights
### Selenium Server
- id:: 63639920-7316-458c-95b4-83ac66561502
   What is Selenium Server? #flashcard 
    Selenium Server allows us to run tests on browser instances running on remote machines and in parallel, thus spreading a load of testing across several machines.
-
### Selenium IDE
- id:: 63639920-8999-4e18-bd2d-23df8dcac3d6
   What is Selenium IDE? #flashcard 
    Selenium IDE is a Firefox add-on that allows users to record, edit, debug, and play back tests captured in the Selenese format, which was introduced in the Selenium Core version.
-
### Testing Mobile Apps with Appium
- id:: 63639920-dfdb-413f-9b96-eb6bb930d8d4
   What is Appium? #flashcard 
    The mobile-testing features that were part of Selenium 2 are now moved into a separate project named Appium. 
     Appium is an open source mobile-automation framework for testing native, hybrid, and web mobile apps on iOS and Android platforms using the JSON-Wire protocol with Selenium WebDriver. Appium replaces the iPhoneDriver and AndroidDriver APIs in Selenium 2 that were used to test mobile web applications.
-
### Using the By locating mechanism
- id:: 63639920-944e-42df-b04b-85e86931529a
   Say a little about Maven #flashcard 
    Along with Eclipse, Apache Maven provides support for managing the life cycle of a test project. Maven is used to define the project structure, dependencies, build, and test-management.
-
### The findElement method
### The By.tagName() method
- id:: 63639920-48bd-4893-b6a4-253f386403c7
   Specify the function to locate WebElements #flashcard 
    WebElement findElement(By by)
-
### The By.linkText() method
### The getText() method
- id:: 63639920-8146-42a2-bd87-0d2d0bde7639
   Handling a link as WebElement #flashcard 
    the By.linkText locating mechanism can only be used to identify the HTML links
-
### The By.partialLinkText() method
### Questions
- id:: 63639920-ee84-427e-b5bd-c0180823da9c
   When the link is not complete or sure. #flashcard 
    The By.partialLinkText locating mechanism is an extension of the By.linkText locator. If you are not sure of the entire link text or want to use only part of the link text, you can use this locator
-
### The By.xpath() method
### Introducing Java 8 Stream API
- id:: 63639920-41f6-4345-9beb-81966a5407e2
  
  to use a specific XPath syntax:
     The root element is identified as //.
     To identify all the div elements, the syntax will be //div.
     To identify the link tags that are within the div element, the syntax will be //div/a.
     To identify all the elements with a tag, we use *. The syntax will be //div/*.
     To identify all the div elements that are at three levels down from the root, we can use //*/*/div.
     To identify specific elements, we use attribute values of those elements, such as //*/div/a[@id='attrValue'], which will return the anchor element. This element is at the third level from the root within a div element and has an id value of attrValue. #flashcard
-
- id:: 63639920-9090-4c93-8d05-f7da6fc29655
   Disadvantages of XPath #flashcard 
    One disadvantage of using XPath is that it is costly in terms of time. For every element to be identified, WebDriver actually scans through the entire page, which is very time consuming, and too much usage of XPath in your test script will actually make it too slow to execute.
-
### The sendKeys() method
### Stream.filter()
- id:: 63639920-626b-43f9-bc49-b37feebca6db
   Which is the function to enter text in a web element? #flashcard 
    ThesendKeys  action is applicable for textbox or textarea HTML elements. This is used to type text into the textbox. This will simulate the user keyboard and types text into WebElements exactly as a user would.
-
### Filtering and counting WebElements&#xA0;
### Stream.sort()
- id:: 63639920-ff65-4dda-9c67-d29bc3642741
   Example of lambda applied to Selenium #flashcard 
    long count = links.stream().filter(item -> item.isDisplayed()).count();
-
### Using the Map function to get the text value from elements
### Stream.map()
- id:: 63639920-8df0-46b6-b390-0f0bec21937d
  
  List<String> expectedProductNames = Arrays.asList("MADISON EARBUDS", "MADISON OVEREAR HEADPHONES", "MP3 PLAYER WITH AUDIO"); List<String> productNames = searchItems.stream() .map(WebElement::getText) .collect(Collectors.toList()); assertThat(productNames). isEqualTo(expectedProductNames); #flashcard
-
### Selenium WebDriver&#xA0;
- id:: 63639920-c3c5-4535-813f-81438f44ff69
   How does Selenium work? #flashcard 
    It works with the following sequence:
     The driver listens to the commands from Selenium 
     It converts these commands into the browser's native API
     The driver takes the result of native commands and sends the result back to Selenium
-
- id:: 63639920-1df5-4785-b5cb-a37590876a80
   What is Selenium WebDriver? #flashcard 
    Selenium WebDriver is the successor of Selenium RC (Remote Control), which has been officially deprecated. Selenium WebDriver accepts commands using the JSON-Wire protocol (also called Client API) and sends them to a browser launched by the specific driver class (such as ChromeDriver, FirefoxDriver, or IEDriver)
-
### Setting up a project in Eclipse with Maven and TestNG using Java
- id:: 63639920-137b-408f-8cc7-63176c28b1b1
   What is (most basically) Selenium WebDriver? #flashcard 
    Selenium WebDriver is a library that helps you automate browsers. However, much more is needed when using it for testing and building a test framework
-
- id:: 63639920-01fe-4850-8415-74ffce91cca3
   Name the best benefit of Maven. #flashcard 
    Another important benefit of using Maven is that we can get all the Selenium library files and their dependencies by configuring the pom.xml file. Maven automatically downloads the necessary files from the repository while building the project.
-
- id:: 63639920-ce44-4b14-93f1-c70151b13634
   Mention the different eight ways of locating WebElements using By. #flashcard 
    They are located by ID, Name, ClassName, TagName, LinkText, PartialLinkText, XPath, and CSS Selector.
-
- id:: 63639920-a07e-4a67-821c-c43520b1a14f
   What's related to a tag? #flashcard 
    Locating an element by tag name is slightly different from the locating mechanisms we saw earlier. For example, on a  Homepage, if you search for an element with the button tag name, it will result in multiple WebElements because there are nine buttons present on the Homepage.
-
- id:: 63639920-1ace-446b-9dca-f44e802162e4
   Explain what the getText() method does. #flashcard 
    The getText method can be called from all the WebElements. It will return visible text if the element contains any text on it, otherwise it will return nothing.  The API syntax for the getText() method is as follows:
     java.lang.String getText()
-
- id:: 63639920-cb46-468d-ae99-fa71669ebd60
   Questions of chapter 1: #flashcard 
    True or false: Selenium is a browser automation library.
     What are the different types of locator mechanisms provided by Selenium?
     True or false: With the getAttribute() method, we can read CSS attributes as well?
     What actions can be performed on a WebElement?
     How can we determine whether the checkbox is checked or unchecked?
-
- id:: 63639920-6381-431d-8e16-74947c1fc730
   How can we get a stream in Java? #flashcard 
    We can obtain a Stream from a collection using the .stream() method
-
- Convert the following code by using streams:
   ```
   for(String language : languages) {
   System.out.println(language);
   }
   ``` #flashcard 
    languages.stream().forEach(System.out::println);
-
- id:: 63639920-c1e4-4571-898c-45066b2a2452
   Let's filter the stream obtained from the languages list to filter items starting with E #flashcard 
    stream.filter( item -> item.startsWith("E") );
-
- id:: 63639920-2648-46c7-84f7-93598cdaa699
   How can you order a stream? #flashcard 
    languages.stream().sorted();
-
- id:: 63639920-c7c2-4176-8470-060ddc8884dc
   Let's take and convert the elements of languages list to uppercase (using streams) #flashcard 
    languages.stream().map(item -> item.toUpperCase());
-
### Stream.collect()
- id:: 63639920-a327-4518-a641-1e602cf5085e
   How can you retrieve the output of a stream operation? #flashcard 
    List<String> upperCaseLanguages = languages.stream() .map(item -> item.toUpperCase()) .collect(Collectors.toList());System.out.println(upperCaseLanguages);
-
### Stream.min() and Stream.max()
- id:: 63639920-2a25-4bb4-aa9a-38161d98c454
   Calculate those names with the minimum price between a stream of objects which have ~.getPrice() #flashcard 
    Product product = searchResult.stream() .min(Comparator.comparing(item -> item.getPrice())) .get();System.out.println("The product with lowest price is " + product.getName());
-
### Stream.count()
- id:: 63639920-74ba-4cdb-86f1-7989f2ae6c5b
   Count the number of objects which start with "MADISON" on a stream. #flashcard 
    long count = searchResult.stream() .filter(item -> item.getName().startsWith("MADISON")) .count();System.out.println("The number of products from MADISON are: " + count);
-
### Filtering element attributes
- id:: 63639920-301b-40a6-86f9-19288c3587ac
   How could you get the images which have an empty alt attribute and store it in a list? #flashcard 
    List<WebElement> imagesWithOutAlt = images.stream() .filter(item -> item.getAttribute("alt") == "") .collect(Collectors.toList());
-
### Filtering and performing actions on WebElements
- id:: 63639920-e04f-4313-b7a2-7704d0eacd87
   A way of retrieving the first WebElement using streams #flashcard 
    WebElement product = searchItems.stream().filter(
     item -> item.getText()
     .equalsIgnoreCase("MADISON_EARBUDS")
     ).findFirst().get();
-
- id:: 63639920-b34d-4dc1-b01d-9bcf226c5368
   A way of retrieving the first WebElement using streams #flashcard 
    WebElement product = searchItems.stream().filter(
     item -> item.getText()
     .equalsIgnoreCase("MADISON_EARBUDS")
     ).findFirst().get();
-
- id:: 63639920-5c6f-4951-96ad-b38afa4c3e2a
   Questions of Chapter 2: #flashcard 
    Which version of Java Streams API is introduced?
     Explain the filter function of Streams API.
     Which method of Streams API will return the number of matching elements from the filter() function?
     We can use the map() function to filter a list of WebElements by attribute values: True or false?
-
### Taking screenshots
- id:: 63639920-76e4-4293-b5db-46b73a8e7b46
   How many different formats has getScreenshotAs() #flashcard 
    We can ask WebDriver to output the screenshot in three different formats : BASE64, BYTES (raw data), and FILE. If you choose the FILE format, it writes the data into a .png file, which will be deleted once the JVM is killed.
-
### Explicit wait time
- id:: 63639920-2052-40a4-9be2-ec0bf10b20fa
   Explicitly wait for one WebElement conditionally #flashcard 
    WebElement searchBox = (new WebDriverWait(driver, 20)) .until((ExpectedCondition<WebElement>) d -> d.findElement(By.name("q")));
-
### Implicit wait time
- id:: 63639920-9b4f-48f9-b141-938041323ff5
   Implicit wait for the whole flow for remote executions #flashcard 
    driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
-
- id:: 63639920-def4-4cbc-9fae-37b4228a48d8
   Questions of Chapter 3. #flashcard 
    Which are the different formats we can use to output a screenshot?
     How can we switch to another browser tab with Selenium?
     True or false: The defaultContent() method will switch to the previously selected frame.
     What navigation methods are available with Selenium?
     How can we add a cookie using Selenium?
     Explain the difference between an implicit wait and an explicit wait.
-