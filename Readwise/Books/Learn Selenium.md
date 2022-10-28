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
- 
 What is Selenium Server? #flashcard 
    Selenium Server allows us to run tests on browser instances running on remote machines and in parallel, thus spreading a load of testing across several machines.

    
-
### Selenium IDE
- 
 What is Selenium IDE? #flashcard 
    Selenium IDE is a Firefox add-on that allows users to record, edit, debug, and play back tests captured in the Selenese format, which was introduced in the Selenium Core version.

    
-
### Testing Mobile Apps with Appium
- 
 What is Appium? #flashcard 
    The mobile-testing features that were part of Selenium 2 are now moved into a separate project named Appium. 
     Appium is an open source mobile-automation framework for testing native, hybrid, and web mobile apps on iOS and Android platforms using the JSON-Wire protocol with Selenium WebDriver. Appium replaces the iPhoneDriver and AndroidDriver APIs in Selenium 2 that were used to test mobile web applications.

    
-
### Using the By locating mechanism
- 
 Say a little about Maven #flashcard 
    Along with Eclipse, Apache Maven provides support for managing the life cycle of a test project. Maven is used to define the project structure, dependencies, build, and test-management.

    
-
### The findElement method
### The By.tagName() method
- 
 Specify the function to locate WebElements #flashcard 
    WebElement findElement(By by)

    
-
### The By.linkText() method
### The getText() method
- 
 Handling a link as WebElement #flashcard 
    the By.linkText locating mechanism can only be used to identify the HTML links

    
-
### The By.partialLinkText() method
### Questions
- 
 When the link is not complete or sure. #flashcard 
    The By.partialLinkText locating mechanism is an extension of the By.linkText locator. If you are not sure of the entire link text or want to use only part of the link text, you can use this locator

    
-
### The By.xpath() method
### Introducing Java 8 Stream API
- 

to use a specific XPath syntax:
     The root element is identified as //.
     To identify all the div elements, the syntax will be //div.
     To identify the link tags that are within the div element, the syntax will be //div/a.
     To identify all the elements with a tag, we use *. The syntax will be //div/*.
     To identify all the div elements that are at three levels down from the root, we can use //*/*/div.
     To identify specific elements, we use attribute values of those elements, such as //*/div/a[@id='attrValue'], which will return the anchor element. This element is at the third level from the root within a div element and has an id value of attrValue. #flashcard 


    
-
- 
 Disadvantages of XPath #flashcard 
    One disadvantage of using XPath is that it is costly in terms of time. For every element to be identified, WebDriver actually scans through the entire page, which is very time consuming, and too much usage of XPath in your test script will actually make it too slow to execute.

    
-
### The sendKeys() method
### Stream.filter()
- 
 Which is the function to enter text in a web element? #flashcard 
    ThesendKeys  action is applicable for textbox or textarea HTML elements. This is used to type text into the textbox. This will simulate the user keyboard and types text into WebElements exactly as a user would.

    
-
### Filtering and counting WebElements&#xA0;
### Stream.sort()
- 
 Example of lambda applied to Selenium #flashcard 
    long count = links.stream().filter(item -> item.isDisplayed()).count();

    
-
### Using the Map function to get the text value from elements
### Stream.map()
- 

List<String> expectedProductNames = Arrays.asList("MADISON EARBUDS", "MADISON OVEREAR HEADPHONES", "MP3 PLAYER WITH AUDIO"); List<String> productNames = searchItems.stream() .map(WebElement::getText) .collect(Collectors.toList()); assertThat(productNames). isEqualTo(expectedProductNames); #flashcard 


    
-
### Selenium WebDriver&#xA0;
- 
 How does Selenium work? #flashcard 
    It works with the following sequence:
     The driver listens to the commands from Selenium 
     It converts these commands into the browser's native API
     The driver takes the result of native commands and sends the result back to Selenium

    
-
- 
 What is Selenium WebDriver? #flashcard 
    Selenium WebDriver is the successor of Selenium RC (Remote Control), which has been officially deprecated. Selenium WebDriver accepts commands using the JSON-Wire protocol (also called Client API) and sends them to a browser launched by the specific driver class (such as ChromeDriver, FirefoxDriver, or IEDriver)

    
-
### Setting up a project in Eclipse with Maven and TestNG using Java
- 
 What is (most basically) Selenium WebDriver? #flashcard 
    Selenium WebDriver is a library that helps you automate browsers. However, much more is needed when using it for testing and building a test framework

    
-
- 
 Name the best benefit of Maven. #flashcard 
    Another important benefit of using Maven is that we can get all the Selenium library files and their dependencies by configuring the pom.xml file. Maven automatically downloads the necessary files from the repository while building the project.

    
-
- 
 Mention the different eight ways of locating WebElements using By. #flashcard 
    They are located by ID, Name, ClassName, TagName, LinkText, PartialLinkText, XPath, and CSS Selector.

    
-
- 
 What's related to a tag? #flashcard 
    Locating an element by tag name is slightly different from the locating mechanisms we saw earlier. For example, on a  Homepage, if you search for an element with the button tag name, it will result in multiple WebElements because there are nine buttons present on the Homepage.

    
-
- 
 Explain what the getText() method does. #flashcard 
    The getText method can be called from all the WebElements. It will return visible text if the element contains any text on it, otherwise it will return nothing.  The API syntax for the getText() method is as follows:
     java.lang.String getText()

    
-
- 
 Questions of chapter 1: #flashcard 
    True or false: Selenium is a browser automation library.
     What are the different types of locator mechanisms provided by Selenium?
     True or false: With the getAttribute() method, we can read CSS attributes as well?
     What actions can be performed on a WebElement?
     How can we determine whether the checkbox is checked or unchecked?

    
-
- 
 How can we get a stream in Java? #flashcard 
    We can obtain a Stream from a collection using the .stream() method

    
-
- 
 Convert the following code by using streams:
   ```
   for(String language : languages) {
   System.out.println(language);
   }
   ``` #flashcard 
    languages.stream().forEach(System.out::println);

    
-
- 
 Let's filter the stream obtained from the languages list to filter items starting with E #flashcard 
    stream.filter( item -> item.startsWith("E") );

    
-
- 
 How can you order a stream? #flashcard 
    languages.stream().sorted();

    
-
- 
 Let's take and convert the elements of languages list to uppercase (using streams) #flashcard 
    languages.stream().map(item -> item.toUpperCase());

    
-
### Stream.collect()
- 
 How can you retrieve the output of a stream operation? #flashcard 
    List<String> upperCaseLanguages = languages.stream() .map(item -> item.toUpperCase()) .collect(Collectors.toList());System.out.println(upperCaseLanguages);

    
-
### Stream.min() and Stream.max()
- 
 Calculate those names with the minimum price between a stream of objects which have ~.getPrice() #flashcard 
    Product product = searchResult.stream() .min(Comparator.comparing(item -> item.getPrice())) .get();System.out.println("The product with lowest price is " + product.getName());

    
-
### Stream.count()
- 
 Count the number of objects which start with "MADISON" on a stream. #flashcard 
    long count = searchResult.stream() .filter(item -> item.getName().startsWith("MADISON")) .count();System.out.println("The number of products from MADISON are: " + count);

    
-
### Filtering element attributes
- 
 How could you get the images which have an empty alt attribute and store it in a list? #flashcard 
    List<WebElement> imagesWithOutAlt = images.stream() .filter(item -> item.getAttribute("alt") == "") .collect(Collectors.toList());

    
-
### Filtering and performing actions on WebElements
- 
 A way of retrieving the first WebElement using streams #flashcard 
    WebElement product = searchItems.stream().filter(
     item -> item.getText()
     .equalsIgnoreCase("MADISON_EARBUDS")
     ).findFirst().get();

    
-
- 
 A way of retrieving the first WebElement using streams #flashcard 
    WebElement product = searchItems.stream().filter(
     item -> item.getText()
     .equalsIgnoreCase("MADISON_EARBUDS")
     ).findFirst().get();

    
-
- 
 Questions of Chapter 2: #flashcard 
    Which version of Java Streams API is introduced?
     Explain the filter function of Streams API.
     Which method of Streams API will return the number of matching elements from the filter() function?
     We can use the map() function to filter a list of WebElements by attribute values: True or false?

    
-
### Taking screenshots
- 
 How many different formats has getScreenshotAs() #flashcard 
    We can ask WebDriver to output the screenshot in three different formats : BASE64, BYTES (raw data), and FILE. If you choose the FILE format, it writes the data into a .png file, which will be deleted once the JVM is killed.

    
-
### Explicit wait time
- 
 Explicitly wait for one WebElement conditionally #flashcard 
    WebElement searchBox = (new WebDriverWait(driver, 20)) .until((ExpectedCondition<WebElement>) d -> d.findElement(By.name("q")));

    
-
### Implicit wait time
- 
 Implicit wait for the whole flow for remote executions #flashcard 
    driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);

    
-
- 
 Questions of Chapter 3. #flashcard 
    Which are the different formats we can use to output a screenshot?
     How can we switch to another browser tab with Selenium?
     True or false: The defaultContent() method will switch to the previously selected frame.
     What navigation methods are available with Selenium?
     How can we add a cookie using Selenium?
     Explain the difference between an implicit wait and an explicit wait.

    
-
