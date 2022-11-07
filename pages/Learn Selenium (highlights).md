title:: Learn Selenium (highlights)
deck:: [[O'Reilly-Learning::Learn Selenium]]
author:: [[]]
full-title:: "Learn Selenium"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- Selenium Server
		- -
			- What is Selenium Server? #flashcard
			  id:: b49cae3b-8bdf-412d-bf9c-a0ef05d3c5f5
				- Selenium Server allows us to run tests on browser instances running on remote machines and in parallel, thus spreading a load of testing across several machines.
		- -
	- Selenium IDE
		- -
			- What is Selenium IDE? #flashcard
			  id:: 9568ec51-0597-48e5-8dcd-68fa9dadb82a
				- Selenium IDE is a Firefox add-on that allows users to record, edit, debug, and play back tests captured in the Selenese format, which was introduced in the Selenium Core version.
		- -
	- Testing Mobile Apps with Appium
		- -
			- What is Appium? #flashcard
			  id:: 3379e6f3-ad06-4185-81c0-afd6420c849a
				- The mobile-testing features that were part of Selenium 2 are now moved into a separate project named Appium. 
				  Appium is an open source mobile-automation framework for testing native, hybrid, and web mobile apps on iOS and Android platforms using the JSON-Wire protocol with Selenium WebDriver. Appium replaces the iPhoneDriver and AndroidDriver APIs in Selenium 2 that were used to test mobile web applications.
		- -
	- Using the By locating mechanism
		- -
			- Say a little about Maven #flashcard
			  id:: cd535fc5-0102-4996-a747-a73f00f3d649
				- Along with Eclipse, Apache Maven provides support for managing the life cycle of a test project. Maven is used to define the project structure, dependencies, build, and test-management.
		- -
	- The findElement method
	- The By.tagName() method
		- -
			- Specify the function to locate WebElements #flashcard
			  id:: 04bd989c-6db0-4d81-9ad3-dc2f6728af28
				- WebElement findElement(By by)
		- -
	- The By.linkText() method
	- The getText() method
		- -
			- Handling a link as WebElement #flashcard
			  id:: a7e8d8d1-4864-4e25-8241-5df001681466
				- the By.linkText locating mechanism can only be used to identify the HTML links
		- -
	- The By.partialLinkText() method
	- Questions
		- -
			- When the link is not complete or sure. #flashcard
			  id:: 26c7a9bd-e6c6-4a18-a165-62bbc5cacc1f
				- The By.partialLinkText locating mechanism is an extension of the By.linkText locator. If you are not sure of the entire link text or want to use only part of the link text, you can use this locator
		- -
	- The By.xpath() method
	- Introducing Java 8 Stream API
		- -
			- to use a specific XPath syntax:
			  id:: 1a859b40-b3db-42a5-b0b5-bba414cd5ea4
			  
			  The root element is identified as //.
			  To identify all the div elements, the syntax will be //div.
			  To identify the link tags that are within the div element, the syntax will be //div/a.
			  To identify all the elements with a tag, we use *. The syntax will be //div/*.
			  To identify all the div elements that are at three levels down from the root, we can use //*/*/div.
			  To identify specific elements, we use attribute values of those elements, such as //*/div/a[@id='attrValue'], which will return the anchor element. This element is at the third level from the root within a div element and has an id value of attrValue. #flashcard
		- -
		- -
			- Disadvantages of XPath #flashcard
			  id:: 7c5b77b8-f64a-4fbb-bb1d-7150c1ca7df5
				- One disadvantage of using XPath is that it is costly in terms of time. For every element to be identified, WebDriver actually scans through the entire page, which is very time consuming, and too much usage of XPath in your test script will actually make it too slow to execute.
		- -
	- The sendKeys() method
	- Stream.filter()
		- -
			- Which is the function to enter text in a web element? #flashcard
			  id:: 6c6e9cda-7203-4f95-8b48-c8ca2e658545
				- ThesendKeys  action is applicable for textbox or textarea HTML elements. This is used to type text into the textbox. This will simulate the user keyboard and types text into WebElements exactly as a user would.
		- -
	- Filtering and counting WebElements&#xA0;
	- Stream.sort()
		- -
			- Example of lambda applied to Selenium #flashcard
			  id:: 9163db78-c61c-4e4a-bc9f-4fba41581c56
				- long count = links.stream().filter(item -> item.isDisplayed()).count();
		- -
	- Using the Map function to get the text value from elements
	- Stream.map()
		- -
			- List<String> expectedProductNames =            Arrays.asList("MADISON EARBUDS",                    "MADISON OVEREAR HEADPHONES",                    "MP3 PLAYER WITH AUDIO");    List<String> productNames = searchItems.stream()            .map(WebElement::getText)            .collect(Collectors.toList());    assertThat(productNames).            isEqualTo(expectedProductNames); #flashcard
			  id:: 3260d9ee-d001-4639-a891-c4f29f73671c
		- -
	- Selenium WebDriver&#xA0;
		- -
			- How does Selenium work? #flashcard
			  id:: 386b33d5-d561-44f7-95f4-5ebcd06e0edf
				- It works with the following sequence:
				  
				  The driver listens to the commands from Selenium 
				  It converts these commands into the browser's native API
				  The driver takes the result of native commands and sends the result back to Selenium
		- -
		- -
			- What is Selenium WebDriver? #flashcard
			  id:: a193802a-63b4-435f-afb7-b5c80f85bf6e
				- Selenium WebDriver is the successor of Selenium RC (Remote Control), which has been officially deprecated. Selenium WebDriver accepts commands using the JSON-Wire protocol (also called Client API) and sends them to a browser launched by the specific driver class (such as ChromeDriver, FirefoxDriver, or IEDriver)
		- -
	- Setting up a project in Eclipse with Maven and TestNG using Java
		- -
			- What is (most basically) Selenium WebDriver? #flashcard
			  id:: 51e35be9-c058-4e64-9641-6914dacfee29
				- Selenium WebDriver is a library that helps you automate browsers. However, much more is needed when using it for testing and building a test framework
		- -
		- -
			- Name the best benefit of Maven. #flashcard
			  id:: 0dad724b-aa8e-47d7-86f1-edc41e79e290
				- Another important benefit of using Maven is that we can get all the Selenium library files and their dependencies by configuring the pom.xml file. Maven automatically downloads the necessary files from the repository while building the project.
		- -
		- -
			- Mention the different eight ways of locating WebElements using By. #flashcard
			  id:: 71942e06-3d0e-4c32-a269-e818cfbea7b1
				- They are located by ID, Name, ClassName, TagName, LinkText, PartialLinkText, XPath, and CSS Selector.
		- -
		- -
			- What's related to a tag? #flashcard
			  id:: 4cbd73db-059d-415c-81f4-4834d3836ac1
				- Locating an element by tag name is slightly different from the locating mechanisms we saw earlier. For example, on a  Homepage, if you search for an element with the button tag name, it will result in multiple WebElements because there are nine buttons present on the Homepage.
		- -
		- -
			- Explain what the getText() method does. #flashcard
			  id:: 553fef92-3798-4fdc-9eeb-7c0961584631
				- The getText method can be called from all the WebElements. It will return visible text if the element contains any text on it, otherwise it will return nothing.  The API syntax for the getText() method is as follows:
				  java.lang.String getText()
		- -
		- -
			- Questions of chapter 1: #flashcard
			  id:: ee59c414-5dfb-4ab6-8db0-33e53c95de5d
				- True or false: Selenium is a browser automation library.
				  What are the different types of locator mechanisms provided by Selenium?
				  True or false: With the getAttribute() method, we can read CSS attributes as well?
				  What actions can be performed on a WebElement?
				  How can we determine whether the checkbox is checked or unchecked?
		- -
		- -
			- How can we get a stream in Java? #flashcard
			  id:: 2d919aa6-c9ac-464c-9248-0a51f67d979c
				- We can obtain a Stream from a collection using the .stream() method
		- -
		- -
			- Convert the following code by using streams:
			  ```
			  for(String language : languages) {
			    System.out.println(language);
			  }
			  ``` #flashcard
				- languages.stream().forEach(System.out::println);
		- -
		- -
			- Let's filter the stream obtained from the languages list to filter items starting with E #flashcard
			  id:: 663bb8e2-cfe1-4911-9fbc-fae25c3f72b9
				- stream.filter( item -> item.startsWith("E") );
		- -
		- -
			- How can you order a stream? #flashcard
			  id:: bcb1dc4c-8b26-4a55-ab4e-e5dbc54aa3cf
				- languages.stream().sorted();
		- -
		- -
			- Let's take and convert the elements of languages list to uppercase (using streams) #flashcard
			  id:: 69b6affb-35ae-4043-a5e2-c22249b3ad9c
				- languages.stream().map(item -> item.toUpperCase());
		- -
	- Stream.collect()
		- -
			- How can you retrieve the output of a stream operation? #flashcard
			  id:: ac494a13-8ab8-4a23-bfc2-221cf4bec9e2
				- List<String> upperCaseLanguages = languages.stream()        .map(item -> item.toUpperCase())        .collect(Collectors.toList());System.out.println(upperCaseLanguages);
		- -
	- Stream.min() and Stream.max()
		- -
			- Calculate those names with the minimum price between a stream of objects which have ~.getPrice() #flashcard
			  id:: cef4b406-7ac6-4613-a025-041b0be57b14
				- Product product = searchResult.stream()        .min(Comparator.comparing(item -> item.getPrice()))        .get();System.out.println("The product with lowest price is " + product.getName());
		- -
	- Stream.count()
		- -
			- Count the number of objects which start with "MADISON" on a stream. #flashcard
			  id:: 10936104-e6ee-4c6a-a6b3-7ae2efe6759c
				- long count = searchResult.stream()        .filter(item -> item.getName().startsWith("MADISON"))        .count();System.out.println("The number of products from MADISON are: " + count);
		- -
	- Filtering element attributes
		- -
			- How could you get the images which have an empty alt attribute and store it in a list? #flashcard
			  id:: b81f28db-caf1-4466-91e3-f2b931e9d4bd
				- List<WebElement> imagesWithOutAlt = images.stream()            .filter(item -> item.getAttribute("alt") == "")            .collect(Collectors.toList());
		- -
	- Filtering and performing actions on WebElements
		- -
			- A way of retrieving the first WebElement using streams #flashcard
			  id:: 84605ed6-d813-40e1-8e04-ac6dc1bc09ff
				- WebElement product = searchItems.stream().filter(
				  item -> item.getText()
				  .equalsIgnoreCase("MADISON_EARBUDS")
				  ).findFirst().get();
		- -
		- -
			- A way of retrieving the first WebElement using streams #flashcard
			  id:: 8e90d306-cec4-452c-ae09-c72fff552d0c
				- WebElement product = searchItems.stream().filter(
				  item -> item.getText()
				  .equalsIgnoreCase("MADISON_EARBUDS")
				  ).findFirst().get();
		- -
		- -
			- Questions of Chapter 2: #flashcard
			  id:: 215c0faf-3d27-4a32-987e-b5506b73163c
				- Which version of Java Streams API is introduced?
				  Explain the filter function of Streams API.
				  Which method of Streams API will return the number of matching elements from the filter() function?
				  We can use the map() function to filter a list of WebElements by attribute values: True or false?
		- -
	- Taking screenshots
		- -
			- How many different formats has getScreenshotAs() #flashcard
			  id:: 75caf961-ce50-4544-80f4-c8f482c2ae15
				- We can ask WebDriver to output the screenshot in three different formats : BASE64, BYTES (raw data), and FILE. If you choose the FILE format, it writes the data into a .png file, which will be deleted once the JVM is killed.
		- -
	- Explicit wait time
		- -
			- Explicitly wait for one WebElement conditionally #flashcard
			  id:: 00e5bada-ba95-4c3e-b215-5eabce90c9c3
				- WebElement searchBox = (new WebDriverWait(driver, 20))        .until((ExpectedCondition<WebElement>) d -> d.findElement(By.name("q")));
		- -
	- Implicit wait time
		- -
			- Implicit wait for the whole flow for remote executions #flashcard
			  id:: 2c0956af-3aa4-40b0-93c6-33d0977cb2e9
				- driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
		- -
		- -
			- Questions of Chapter 3. #flashcard
			  id:: a57a3e46-7f23-4f0d-824c-14941d5fe6e8
				- Which are the different formats we can use to output a screenshot?
				  How can we switch to another browser tab with Selenium?
				  True or false: The defaultContent() method will switch to the previously selected frame.
				  What navigation methods are available with Selenium?
				  How can we add a cookie using Selenium?
				  Explain the difference between an implicit wait and an explicit wait.
		- -