title:: Learn Selenium (highlights)
author:: [[]]
full-title:: "Learn Selenium"
category:: #books

tags:: #[[O'Reilly-Learning]]

- #tags #[[O'Reilly-Learning]]
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- Selenium Server
		- -
		- What is Selenium Server? #car
		  id:: 63401528-20c2-4303-91e1-36cd47df0d76
			- Selenium Server allows us to run tests on browser instances running on remote machines and in parallel, thus spreading a load of testing across several machines.
		- -
	- Selenium IDE
		- -
		- What is Selenium IDE? #car
		  id:: 63401528-cc9c-4dd4-8b62-c00c28b14c1a
			- Selenium IDE is a Firefox add-on that allows users to record, edit, debug, and play back tests captured in the Selenese format, which was introduced in the Selenium Core version.
		- -
	- Testing Mobile Apps with Appium
		- -
		- What is Appium? #car
			- The mobile-testing features that were part of Selenium 2 are now moved into a separate project named Appium. 
			  Appium is an open source mobile-automation framework for testing native, hybrid, and web mobile apps on iOS and Android platforms using the JSON-Wire protocol with Selenium WebDriver. Appium replaces the iPhoneDriver and AndroidDriver APIs in Selenium 2 that were used to test mobile web applications.
		- -
	- Using the By locating mechanism
		- -
		- Say a little about Maven #car
			- Along with Eclipse, Apache Maven provides support for managing the life cycle of a test project. Maven is used to define the project structure, dependencies, build, and test-management.
		- -
	- The findElement method
	- The By.tagName() method
		- -
		- Specify the function to locate WebElements #car
			- WebElement findElement(By by)
		- -
	- The By.linkText() method
	- The getText() method
		- -
		- Handling a link as WebElement #car
		  id:: 63401528-d11a-4472-8969-57314bfa8778
			- the By.linkText locating mechanism can only be used to identify the HTML links
		- -
	- The By.partialLinkText() method
	- Questions
		- -
		- When the link is not complete or sure. #car
			- The By.partialLinkText locating mechanism is an extension of the By.linkText locator. If you are not sure of the entire link text or want to use only part of the link text, you can use this locator
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
		  To identify specific elements, we use attribute values of those elements, such as //*/div/a[@id='attrValue'], which will return the anchor element. This element is at the third level from the root within a div element and has an id value of attrValue. #ñspace
		- -
		- -
		- Disadvantages of XPath #car
			- One disadvantage of using XPath is that it is costly in terms of time. For every element to be identified, WebDriver actually scans through the entire page, which is very time consuming, and too much usage of XPath in your test script will actually make it too slow to execute.
		- -
	- The sendKeys() method
	- Stream.filter()
		- -
		- Which is the function to enter text in a web element? #car
		  id:: 63401528-ea14-4101-a299-39826904ca4e
			- ThesendKeys  action is applicable for textbox or textarea HTML elements. This is used to type text into the textbox. This will simulate the user keyboard and types text into WebElements exactly as a user would.
		- -
	- Filtering and counting WebElements&#xA0;
	- Stream.sort()
		- -
		- Example of lambda applied to Selenium #car
		  id:: 63401528-b958-4b25-abbf-10752c6ab76f
			- long count = links.stream().filter(item -> item.isDisplayed()).count();
		- -
	- Using the Map function to get the text value from elements
	- Stream.map()
		- -
		- List<String> expectedProductNames =            Arrays.asList("MADISON EARBUDS",                    "MADISON OVEREAR HEADPHONES",                    "MP3 PLAYER WITH AUDIO");    List<String> productNames = searchItems.stream()            .map(WebElement::getText)            .collect(Collectors.toList());    assertThat(productNames).            isEqualTo(expectedProductNames); #ñspace
		- -
	- Selenium WebDriver&#xA0;
		- -
		- How does Selenium work? #car
		  id:: 63401528-8bd2-4777-9aca-af800f45f819
			- It works with the following sequence:
			  
			  The driver listens to the commands from Selenium 
			  It converts these commands into the browser's native API
			  The driver takes the result of native commands and sends the result back to Selenium
		- -
		- -
		- What is Selenium WebDriver? #car
		  id:: 63401528-628a-40ea-8cdf-fc7a5b66ff5d
			- Selenium WebDriver is the successor of Selenium RC (Remote Control), which has been officially deprecated. Selenium WebDriver accepts commands using the JSON-Wire protocol (also called Client API) and sends them to a browser launched by the specific driver class (such as ChromeDriver, FirefoxDriver, or IEDriver)
		- -
	- Setting up a project in Eclipse with Maven and TestNG using Java
		- -
		- What is (most basically) Selenium WebDriver? #car
		  id:: 63401528-c328-4fba-b24b-429110a3bdad
			- Selenium WebDriver is a library that helps you automate browsers. However, much more is needed when using it for testing and building a test framework
		- -
		- -
		- Name the best benefit of Maven. #car
			- Another important benefit of using Maven is that we can get all the Selenium library files and their dependencies by configuring the pom.xml file. Maven automatically downloads the necessary files from the repository while building the project.
		- -
		- -
		- Mention the different eight ways of locating WebElements using By. #car
		  id:: 63401528-a140-43f8-86e0-85d274ac2405
			- They are located by ID, Name, ClassName, TagName, LinkText, PartialLinkText, XPath, and CSS Selector.
		- -
		- -
		- What's related to a tag? #car
			- Locating an element by tag name is slightly different from the locating mechanisms we saw earlier. For example, on a  Homepage, if you search for an element with the button tag name, it will result in multiple WebElements because there are nine buttons present on the Homepage.
		- -
		- -
		- Explain what the getText() method does. #car
			- The getText method can be called from all the WebElements. It will return visible text if the element contains any text on it, otherwise it will return nothing.  The API syntax for the getText() method is as follows:
			  java.lang.String getText()
		- -
		- -
		- Questions of chapter 1: #car
			- True or false: Selenium is a browser automation library.
			  What are the different types of locator mechanisms provided by Selenium?
			  True or false: With the getAttribute() method, we can read CSS attributes as well?
			  What actions can be performed on a WebElement?
			  How can we determine whether the checkbox is checked or unchecked?
		- -
		- -
		- How can we get a stream in Java? #car
		  id:: 63401528-d7c1-4c05-bf16-063137df9654
			- We can obtain a Stream from a collection using the .stream() method
		- -
		- -
		- Convert the following code by using streams:
		  ```
		  for(String language : languages) {
		    System.out.println(language);
		  }
		  ``` #card
			- languages.stream().forEach(System.out::println);
		- -
		- -
		- Let's filter the stream obtained from the languages list to filter items starting with E #car
		  id:: 63401528-834c-49f5-bf94-bbdf2e9771e3
			- stream.filter( item -> item.startsWith("E") );
		- -
		- -
		- How can you order a stream? #car
			- languages.stream().sorted();
		- -
		- -
		- Let's take and convert the elements of languages list to uppercase (using streams) #car
			- languages.stream().map(item -> item.toUpperCase());
		- -
	- Stream.collect()
		- -
		- How can you retrieve the output of a stream operation? #car
		  id:: 63401528-5be3-4e54-bda9-98e38218cfe3
			- List<String> upperCaseLanguages = languages.stream()        .map(item -> item.toUpperCase())        .collect(Collectors.toList());System.out.println(upperCaseLanguages);
		- -
	- Stream.min() and Stream.max()
		- -
		- Calculate those names with the minimum price between a stream of objects which have ~.getPrice() #car
		  id:: 63401528-c337-4e4b-a4da-bc7efe57b044
			- Product product = searchResult.stream()        .min(Comparator.comparing(item -> item.getPrice()))        .get();System.out.println("The product with lowest price is " + product.getName());
		- -
	- Stream.count()
		- -
		- Count the number of objects which start with "MADISON" on a stream. #car
			- long count = searchResult.stream()        .filter(item -> item.getName().startsWith("MADISON"))        .count();System.out.println("The number of products from MADISON are: " + count);
		- -
	- Filtering element attributes
		- -
		- How could you get the images which have an empty alt attribute and store it in a list? #car
			- List<WebElement> imagesWithOutAlt = images.stream()            .filter(item -> item.getAttribute("alt") == "")            .collect(Collectors.toList());
		- -
	- Filtering and performing actions on WebElements
		- -
		- A way of retrieving the first WebElement using streams #car
			- WebElement product = searchItems.stream().filter(
			  item -> item.getText()
			  .equalsIgnoreCase("MADISON_EARBUDS")
			  ).findFirst().get();
		- -
		- -
		- A way of retrieving the first WebElement using streams #car
		  id:: 63401528-c346-4eaf-8437-10ce05eea562
			- WebElement product = searchItems.stream().filter(
			  item -> item.getText()
			  .equalsIgnoreCase("MADISON_EARBUDS")
			  ).findFirst().get();
		- -
		- -
		- Questions of Chapter 2: #car
			- Which version of Java Streams API is introduced?
			  Explain the filter function of Streams API.
			  Which method of Streams API will return the number of matching elements from the filter() function?
			  We can use the map() function to filter a list of WebElements by attribute values: True or false?
		- -
	- Taking screenshots
		- -
		- How many different formats has getScreenshotAs() #car
			- We can ask WebDriver to output the screenshot in three different formats : BASE64, BYTES (raw data), and FILE. If you choose the FILE format, it writes the data into a .png file, which will be deleted once the JVM is killed.
		- -
	- Explicit wait time
		- -
		- Explicitly wait for one WebElement conditionally #car
		  id:: 63401528-d6de-4cae-94f8-117de4617d73
			- WebElement searchBox = (new WebDriverWait(driver, 20))        .until((ExpectedCondition<WebElement>) d -> d.findElement(By.name("q")));
		- -
	- Implicit wait time
		- -
		- Implicit wait for the whole flow for remote executions #car
			- driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
		- -
		- -
		- Questions of Chapter 3. #car
		  id:: 63401528-b56d-460c-8577-586318e5c69b
			- Which are the different formats we can use to output a screenshot?
			  How can we switch to another browser tab with Selenium?
			  True or false: The defaultContent() method will switch to the previously selected frame.
			  What navigation methods are available with Selenium?
			  How can we add a cookie using Selenium?
			  Explain the difference between an implicit wait and an explicit wait.
		- -