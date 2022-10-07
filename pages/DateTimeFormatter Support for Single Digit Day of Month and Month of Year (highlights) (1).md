title:: DateTimeFormatter Support for Single Digit Day of Month and Month of Year (highlights) (1)
author:: [[stackoverflow.com]]
full-title:: "DateTimeFormatter Support for Single Digit Day of Month and Month of Year"
category:: #articles
url:: https://stackoverflow.com/questions/27571377/datetimeformatter-support-for-single-digit-day-of-month-and-month-of-year

- Highlights first synced by [[Readwise]] [[Friday, 07-10-2022]]
	- -
	- . #flashcard
		- DateTimeFormatter formatter = new DateTimeFormatterBuilder()
		            .appendOptional(DateTimeFormatter.ofPattern("M/dd/yyyy"))
		            .toFormatter();
		  
		  System.out.println(LocalDate.parse("10/22/2020", formatter));
		  System.out.println(LocalDate.parse("2/21/2020", formatter));
	- -