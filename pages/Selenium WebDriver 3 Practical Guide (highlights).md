title:: Selenium WebDriver 3 Practical Guide (highlights)
author:: [[Unmesh Gundecha, Satya Avasarala]]
full-title:: "Selenium WebDriver 3 Practical Guide"
category:: #books

- ![](https://images-na.ssl-images-amazon.com/images/I/51nYrf6CcmL._SL200_.jpg)
- Highlights first synced by [[Readwise]] [[Friday, 28-10-2022]]
	- Selenium is a set of tools for automating browsers. ([Location 316](https://readwise.io/to_kindle?action=open&asin=B07BJKWB1J&location=316))
		- **Tags**: #[[pink]] #[[rosa]]
	- Selenium 3.0 offers three important tools, Selenium WebDriver, Selenium Server, and Selenium IDE. Each of these tools provides features to create, debug, and run tests on supported browsers ([Location 429](https://readwise.io/to_kindle?action=open&asin=B07BJKWB1J&location=429))
		- **Tags**: #[[blue]] #[[azul]]
	- Selenium WebDriver accepts commands using the JSON-Wire protocol (also called Client API) and sends them to a browser launched by the specific driver class (such as ChromeDriver, FirefoxDriver, or IEDriver). This is implemented through a browser-specific browser driver. ([Location 432](https://readwise.io/to_kindle?action=open&asin=B07BJKWB1J&location=432))
		- **Tags**: #[[blue]] #[[azul]]
	- Selenium Server allows us to run tests on browser instances running on remote machines and in parallel, ([Location 445](https://readwise.io/to_kindle?action=open&asin=B07BJKWB1J&location=445))
		- **Tags**: #[[blue]] #[[azul]]
	- Selenium IDE is a Firefox add-on that allows users to record, edit, debug, and play back tests captured in the Selenese format, ([Location 451](https://readwise.io/to_kindle?action=open&asin=B07BJKWB1J&location=451))
		- **Tags**: #[[blue]] #[[azul]]
	- The Selenium IDE for Firefox stopped working after the Firefox 55 moved to the WebExtension format from XPI format and it is currently no longer maintained. ([Location 455](https://readwise.io/to_kindle?action=open&asin=B07BJKWB1J&location=455))
	- Apache Maven provides support for managing the life cycle of a test project. Maven is used to define the project structure, dependencies, build, and test-management. ([Location 481](https://readwise.io/to_kindle?action=open&asin=B07BJKWB1J&location=481))
		- **Tags**: #[[blue]] #[[azul]]
	- TestNG ([Location 490](https://readwise.io/to_kindle?action=open&asin=B07BJKWB1J&location=490))
		- **Tags**: #[[pink]] #[[rosa]]
		- **Note**: Buscar y comparar con junit
	- A web page is composed of many different types of HTML elements, such as links, textboxes, dropdown buttons, a body, labels, and forms. These are called WebElements in the context of WebDriver. ([Location 574](https://readwise.io/to_kindle?action=open&asin=B07BJKWB1J&location=574))
		- **Tags**: #[[pink]] #[[rosa]]
	- UI-automation using Selenium is mostly about locating these WebElements on a web page and executing user actions on them. ([Location 601](https://readwise.io/to_kindle?action=open&asin=B07BJKWB1J&location=601))
		- **Tags**: #[[pink]] #[[rosa]]
	- According to WebDriver's Javadoc (http://selenium.googlecode.com/git/docs/api/java/index.html), the method declaration is as follows: WebElement findElement(By by) ([Location 639](https://readwise.io/to_kindle?action=open&asin=B07BJKWB1J&location=639))
		- **Tags**: #[[pink]] #[[rosa]]
	- There are eight different ways to locate a WebElement on a web page. ([Location 644](https://readwise.io/to_kindle?action=open&asin=B07BJKWB1J&location=644))
		- **Tags**: #[[blue]] #[[azul]]
	- The method declaration of the findElements() method is as follows: java.util.List findElements(By by) ([Location 652](https://readwise.io/to_kindle?action=open&asin=B07BJKWB1J&location=652))
		- **Tags**: #[[pink]] #[[rosa]]
	- There are eight different locating mechanisms; that is, eight different ways to identify an HTML element on a web page. They are located by ID, Name, ClassName, TagName, LinkText, PartialLinkText, XPath, and CSS Selector. ([Location 695](https://readwise.io/to_kindle?action=open&asin=B07BJKWB1J&location=695))
		- **Tags**: #[[blue]] #[[azul]]
	- driver.findElement(By.id("search")); ([Location 707](https://readwise.io/to_kindle?action=open&asin=B07BJKWB1J&location=707))
		- **Tags**: #[[orange]] #[[naranja]]
	- driver.findElement(By.name("q")); ([Location 731](https://readwise.io/to_kindle?action=open&asin=B07BJKWB1J&location=731))
		- **Tags**: #[[orange]] #[[naranja]]
	- driver.findElement(By.className("search-button")); ([Location 756](https://readwise.io/to_kindle?action=open&asin=B07BJKWB1J&location=756))
		- **Tags**: #[[orange]] #[[naranja]]
		- **Note**: La clase es la del CSS! Ya sea especificada en el .css o en el .html
	- As the name suggests, the By.linkText locating mechanism can only be used to identify the HTML links. ([Location 768](https://readwise.io/to_kindle?action=open&asin=B07BJKWB1J&location=768))
		- **Tags**: #[[pink]] #[[rosa]]