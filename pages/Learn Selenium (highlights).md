title:: Learn Selenium (highlights)
deck:: [[O'Reilly-Learning::Learn Selenium]]
author:: [[]]
full-title:: "Learn Selenium"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- Selenium Server
		- -
		- Selenium Server allows us to run tests on browser instances running on remote machines and in parallel, thus spreading a load of testing across several machines. #flashcard
			- What is Selenium Server?
		- -
	- Selenium IDE
		- -
		- Selenium IDE is a Firefox add-on that allows users to record, edit, debug, and play back tests captured in the Selenese format, which was introduced in the Selenium Core version. #flashcard
			- What is Selenium IDE?
		- -
	- Testing Mobile Apps with Appium
		- -
		- The mobile-testing features that were part of Selenium 2 are now moved into a separate project named Appium. 
		  Appium is an open source mobile-automation framework for testing native, hybrid, and web mobile apps on iOS and Android platforms using the JSON-Wire protocol with Selenium WebDriver. Appium replaces the iPhoneDriver and AndroidDriver APIs in Selenium 2 that were used to test mobile web applications. #flashcard
			- What is Appium?
		- -
	- Using the By locating mechanism
		- -
		- Along with Eclipse, Apache Maven provides support for managing the life cycle of a test project. Maven is used to define the project structure, dependencies, build, and test-management. #flashcard
			- Say a little about Maven
		- -
	- The findElement method
	- The By.tagName() method
		- -
		- WebElement findElement(By by) #flashcard
			- Specify the function to locate WebElements
		- -
	- The By.linkText() method
	- The getText() method
		- -
		- the By.linkText locating mechanism can only be used to identify the HTML links #flashcard
			- Handling a link as WebElement
		- -
	- The By.partialLinkText() method
	- Questions
		- -
		- The By.partialLinkText locating mechanism is an extension of the By.linkText locator. If you are not sure of the entire link text or want to use only part of the link text, you can use this locator #flashcard
			- When the link is not complete or sure.
		- -
	- The By.xpath() method
	- Introducing Java 8 Stream API
		- -
		- to use a specific XPath syntax:
		  
		  The root element is identified as //.
		  To identify all the div elements, the syntax will be //div.
		  To identify the link tags that are within the div element, the syntax will be //div/a.
		  To identify all the elements with a tag, we use *. The syntax will be //div/*.
		  To identify all the div elements that are at three levels down from the root, we can use //*/*/div.
		  To identify specific elements, we use attribute values of those elements, such as //*/div/a[@id='attrValue'], which will return the anchor element. This element is at the third level from the root within a div element and has an id value of attrValue. #flashcard
		- -
		- -
		- One disadvantage of using XPath is that it is costly in terms of time. For every element to be identified, WebDriver actually scans through the entire page, which is very time consuming, and too much usage of XPath in your test script will actually make it too slow to execute. #flashcard
			- Disadvantages of XPath
		- -
	- The sendKeys() method
	- Stream.filter()
		- -
		- ThesendKeys  action is applicable for textbox or textarea HTML elements. This is used to type text into the textbox. This will simulate the user keyboard and types text into WebElements exactly as a user would. #flashcard
			- Which is the function to enter text in a web element?
		- -
	- Filtering and counting WebElements&#xA0;
	- Stream.sort()
		- -
		- long count = links.stream().filter(item -> item.isDisplayed()).count(); #flashcard
			- Example of lambda applied to Selenium
		- -
	- Using the Map function to get the text value from elements
	- Stream.map()
		- -
		- List<String> expectedProductNames =            Arrays.asList("MADISON EARBUDS",                    "MADISON OVEREAR HEADPHONES",                    "MP3 PLAYER WITH AUDIO");    List<String> productNames = searchItems.stream()            .map(WebElement::getText)            .collect(Collectors.toList());    assertThat(productNames).            isEqualTo(expectedProductNames); #flashcard
		- -
	- Selenium WebDriver&#xA0;
		- -
		- It works with the following sequence:
		  
		  The driver listens to the commands from Selenium 
		  It converts these commands into the browser's native API
		  The driver takes the result of native commands and sends the result back to Selenium #flashcard
			- How does Selenium work?
		- -
		- -
		- Selenium WebDriver is the successor of Selenium RC (Remote Control), which has been officially deprecated. Selenium WebDriver accepts commands using the JSON-Wire protocol (also called Client API) and sends them to a browser launched by the specific driver class (such as ChromeDriver, FirefoxDriver, or IEDriver) #flashcard
			- What is Selenium WebDriver?
		- -
	- Setting up a project in Eclipse with Maven and TestNG using Java
		- -
		- Selenium WebDriver is a library that helps you automate browsers. However, much more is needed when using it for testing and building a test framework #flashcard
			- What is (most basically) Selenium WebDriver?
		- -
		- -
		- Another important benefit of using Maven is that we can get all the Selenium library files and their dependencies by configuring the pom.xml file. Maven automatically downloads the necessary files from the repository while building the project. #flashcard
			- Name the best benefit of Maven.
		- -
		- -
		- They are located by ID, Name, ClassName, TagName, LinkText, PartialLinkText, XPath, and CSS Selector. #flashcard
			- Mention the different eight ways of locating WebElements using By.
		- -
		- -
		- Locating an element by tag name is slightly different from the locating mechanisms we saw earlier. For example, on a  Homepage, if you search for an element with the button tag name, it will result in multiple WebElements because there are nine buttons present on the Homepage. #flashcard
			- What's related to a tag?
		- -
		- -
		- The getText method can be called from all the WebElements. It will return visible text if the element contains any text on it, otherwise it will return nothing.  The API syntax for the getText() method is as follows:
		  java.lang.String getText() #flashcard
			- Explain what the getText() method does.
		- -
		- -
		- True or false: Selenium is a browser automation library.
		  What are the different types of locator mechanisms provided by Selenium?
		  True or false: With the getAttribute() method, we can read CSS attributes as well?
		  What actions can be performed on a WebElement?
		  How can we determine whether the checkbox is checked or unchecked? #flashcard
			- Questions of chapter 1:
		- -
		- -
		- We can obtain a Stream from a collection using the .stream() method #flashcard
			- How can we get a stream in Java?
		- -
		- -
		- languages.stream().forEach(System.out::println); #flashcard
			- Convert the following code by using streams:
			  ```
			  for(String language : languages) {
			    System.out.println(language);
			  }
			  ```
		- -
		- -
		- stream.filter( item -> item.startsWith("E") ); #flashcard
			- Let's filter the stream obtained from the languages list to filter items starting with E
		- -
		- -
		- languages.stream().sorted(); #flashcard
			- How can you order a stream?
		- -
		- -
		- languages.stream().map(item -> item.toUpperCase()); #flashcard
			- Let's take and convert the elements of languages list to uppercase (using streams)
		- -
	- Stream.collect()
		- -
		- List<String> upperCaseLanguages = languages.stream()        .map(item -> item.toUpperCase())        .collect(Collectors.toList());System.out.println(upperCaseLanguages); #flashcard
			- How can you retrieve the output of a stream operation?
		- -
	- Stream.min() and Stream.max()
		- -
		- Product product = searchResult.stream()        .min(Comparator.comparing(item -> item.getPrice()))        .get();System.out.println("The product with lowest price is " + product.getName()); #flashcard
			- Calculate those names with the minimum price between a stream of objects which have ~.getPrice()
		- -
	- Stream.count()
		- -
		- long count = searchResult.stream()        .filter(item -> item.getName().startsWith("MADISON"))        .count();System.out.println("The number of products from MADISON are: " + count); #flashcard
			- Count the number of objects which start with "MADISON" on a stream.
		- -
	- Filtering element attributes
		- -
		- List<WebElement> imagesWithOutAlt = images.stream()            .filter(item -> item.getAttribute("alt") == "")            .collect(Collectors.toList()); #flashcard
			- How could you get the images which have an empty alt attribute and store it in a list?
		- -
	- Filtering and performing actions on WebElements
		- -
		- WebElement product = searchItems.stream().filter(
		  item -> item.getText()
		  .equalsIgnoreCase("MADISON_EARBUDS")
		  ).findFirst().get(); #flashcard
			- A way of retrieving the first WebElement using streams
		- -
		- -
		- WebElement product = searchItems.stream().filter(
		  item -> item.getText()
		  .equalsIgnoreCase("MADISON_EARBUDS")
		  ).findFirst().get(); #flashcard
			- A way of retrieving the first WebElement using streams
		- -
		- -
		- Which version of Java Streams API is introduced?
		  Explain the filter function of Streams API.
		  Which method of Streams API will return the number of matching elements from the filter() function?
		  We can use the map() function to filter a list of WebElements by attribute values: True or false? #flashcard
			- Questions of Chapter 2:
		- -
	- Taking screenshots
		- -
		- We can ask WebDriver to output the screenshot in three different formats : BASE64, BYTES (raw data), and FILE. If you choose the FILE format, it writes the data into a .png file, which will be deleted once the JVM is killed. #flashcard
			- How many different formats has getScreenshotAs()
		- -
	- Explicit wait time
		- -
		- WebElement searchBox = (new WebDriverWait(driver, 20))        .until((ExpectedCondition<WebElement>) d -> d.findElement(By.name("q"))); #flashcard
			- Explicitly wait for one WebElement conditionally
		- -
	- Implicit wait time
		- -
		- driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS); #flashcard
			- Implicit wait for the whole flow for remote executions
		- -
		- -
		- Which are the different formats we can use to output a screenshot?
		  How can we switch to another browser tab with Selenium?
		  True or false: The defaultContent() method will switch to the previously selected frame.
		  What navigation methods are available with Selenium?
		  How can we add a cookie using Selenium?
		  Explain the difference between an implicit wait and an explicit wait. #flashcard
			- Questions of Chapter 3.
		- -