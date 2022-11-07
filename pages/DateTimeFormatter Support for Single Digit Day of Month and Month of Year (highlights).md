title:: DateTimeFormatter Support for Single Digit Day of Month and Month of Year (highlights)
deck:: [[Across-the-Net]]
author:: [[stackoverflow.com]]
full-title:: "DateTimeFormatter Support for Single Digit Day of Month and Month of Year"
category:: #articles
url:: https://stackoverflow.com/questions/27571377/datetimeformatter-support-for-single-digit-day-of-month-and-month-of-year

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- . #flashcard
		  id:: 592744b4-014a-4bec-b0df-59b303f01379
			- DateTimeFormatter formatter = new DateTimeFormatterBuilder()
			            .appendOptional(DateTimeFormatter.ofPattern("M/dd/yyyy"))
			            .toFormatter();
			  
			  System.out.println(LocalDate.parse("10/22/2020", formatter));
			  System.out.println(LocalDate.parse("2/21/2020", formatter));
	- -