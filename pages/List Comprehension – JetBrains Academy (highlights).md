title:: List Comprehension – JetBrains Academy (highlights)
author:: [[hyperskill.org]]
full-title:: "List Comprehension – JetBrains Academy"
category:: #articles
url:: https://hyperskill.org/learn/step/6315

- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- How to use if else in list comprehension .python #car
		- Finally, we can introduce the else statement in list comprehension. The syntax here differs a bit: [x if condition else y for x in some_iterable]. Using this, we can, for example, get 0 in a new list for each negative number in the old list:
		  
		  `old_list = [8, 13, -7, 4, -9, 2, 10]new_list = [num if num >= 0 else 0 for num in old_list]print(new_list)  # [ 8, 13, 0, 4, 0, 2, 10]`
		-
	- -