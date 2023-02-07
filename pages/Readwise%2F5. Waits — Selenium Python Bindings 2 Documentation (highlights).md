title:: Readwise/5. Waits — Selenium Python Bindings 2 Documentation (highlights)
deck:: [[Across-the-Net]]
author:: [[selenium-python.readthedocs.io]]
full-title:: "5. Waits — Selenium Python Bindings 2 Documentation"
category:: #articles
url:: https://selenium-python.readthedocs.io/waits.html

- Highlights first synced by [[Readwise]] [[Tuesday, 07-02-2023]]
	- -
		- About explicit and implicit waits in Selenium (with Python example) .info #flashcard
			- These days, most of the web apps are using AJAX techniques.  When a page is
			  loaded by the browser, the elements within that page may load at different time
			  intervals.  This makes locating elements difficult: if an element is not yet
			  present in the DOM, a locate function will raise an ElementNotVisibleException
			  exception.  Using waits, we can solve this issue.  Waiting provides some slack
			  between actions performed - mostly locating an element or any other operation
			  with the element.
			  Selenium Webdriver provides two types of waits - implicit & explicit.  An
			  explicit wait makes WebDriver wait for a certain condition to occur before
			  proceeding further with execution.  An implicit wait makes WebDriver poll the
			  DOM for a certain amount of time when trying to locate an element.
			  
			  5.1. Explicit Waits¶
			  An explicit wait is a code you define to wait for a certain condition to occur
			  before proceeding further in the code.  The extreme case of this is
			  time.sleep(), which sets the condition to an exact time period to wait.  There
			  are some convenience methods provided that help you write code that will wait
			  only as long as required.  WebDriverWait in combination with ExpectedCondition
			  is one way this can be accomplished.
			  from selenium import webdriver
			  from selenium.webdriver.common.by import By
			  from selenium.webdriver.support.ui import WebDriverWait
			  from selenium.webdriver.support import expected_conditions as EC
			  
			  driver = webdriver.Firefox()
			  driver.get("http://somedomain/url_that_delays_loading")
			  try:
			    element = WebDriverWait(driver, 10).until(
			        EC.presence_of_element_located((By.ID, "myDynamicElement"))
			    )
			  finally:
			    driver.quit()
	- -