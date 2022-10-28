# Programming - Evernote

deck:: [[Across-the-Net]]\
author:: [[evernote.com]]\
full-title:: "Programming - Evernote"\
category:: #articles\
url:: https://www.evernote.com/client/web?login=true#?b=7de30b4e-ef62-4acc-a94a-48268d048e10&n=d85c1257-c05b-4e88-93a3-b6d4912d094c&\

![](https://readwise-assets.s3.amazonaws.com/static/images/article0.00998d930354.png)

## Highlights
- 

How to send ENTER to a text field in Selenium? You can use either of Keys.ENTER or Keys.RETURN. Here are some details: Usage: Java: Using Keys.ENTER: import org.openqa.selenium.Keys; driver.findElement(By.id("element_id")).sendKeys(Keys.ENTER); Using Keys.RETURN import org.openqa.selenium.Keys; driver.findElement(By.id("element_id")).sendKeys(Keys.RETURN); Python: Using Keys.ENTER: from selenium.webdriver.common.keys import Keys driver.find_element_by_id("element_id").send_keys(Keys.ENTER) Using Keys.RETURN from selenium.webdriver.common.keys import Keys driver.find_element_by_id("element_id").send_keys(Keys.RETURN) Keys.ENTER and Keys.RETURN both are from org.openqa.selenium.Keys, which extends java.lang.Enum<Keys> and implements java.lang.CharSequence Enum Keys Enum Keys is the representations of pressable keys that aren't text. These are stored in the Unicode PUA (Private Use Area) code points, 0xE000-0xF8FF. Key Codes: The special keys codes for them are as follows: RETURN = u'\ue006' ENTER = u'\ue007' The implementation of all the Enum Keys are handled the same way. Hence these is No Functional or Operational difference while working with either sendKeys(Keys.ENTER); or WebElement.sendKeys(Keys.RETURN); through Selenium. Enter Key and Return Key On computer keyboards, the Enter (or the Return on Mac OS X) in most cases causes a command line, window form, or dialog box to operate its default function. This is typically to finish an "entry" and begin the desired process and is usually an alternative to pressing an OK button. The Return is often also referred as the Enter and they usually perform identical functions; however in some particular applications (mainly page layout) Return operates specifically like the Carriage Return key from which it originates. In contrast, the Enter is commonly labelled with its name in plain text on generic PC keyboards. #flashcard 


    
-
