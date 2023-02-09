title:: How Can I Match "Anything Up Until This Sequence of Characters" in a Regular Expression? (highlights)
author:: [[stackoverflow.com]]
full-title:: "How Can I Match "Anything Up Until This Sequence of Characters" in a Regular Expression?"
category:: #articles
url:: https://stackoverflow.com/questions/7124778/how-can-i-match-anything-up-until-this-sequence-of-characters-in-a-regular-exp

- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- How do you build a regex that eat everything until one character? #card
		- You didn't  specify which flavor  of regex  you're using, but  this will
		  work in any of the most popular ones that can be considered "complete".
		  
		  /.+?(?=abc)/
		  
		  
		  How it works
		  
		  The  .+?  part is  the  un-greedy  version of  .+  (one  or more  of
		  anything). When we use .+, the engine will basically match everything.
		  Then, if there is  something else in the regex it will  go back in steps
		  trying to  match the  following part. This  is the  greedy behavior,
		  meaning as much as possible to satisfy.
		  
		  When using  .+?, instead of  matching all at  once and going  back for
		  other conditions (if any), the engine  will match the next characters by
		  step until the  subsequent part of the regex is  matched (again if any).
		  This  is  the un-greedy,  meaning  match  the fewest  possible  to
		  satisfy.
		  
		  /.+X/  ~ "abcXabcXabcX"        /.+/  ~ "abcXabcXabcX"
		          ^^^^^^^^^^^^                  ^^^^^^^^^^^^
		  
		  /.+?X/ ~ "abcXabcXabcX"        /.+?/ ~ "abcXabcXabcX"
		          ^^^^                          ^
		  
		  
		  Following  that   we  have   (?={contents}),  a   zero  width
		  assertion,  a  look around.  This  grouped  construction matches  its
		  contents, but does not count  as characters matched (zero width). It
		  only returns if it is a match or not (assertion).
		  
		  Thus, in other terms the regex /.+?(?=abc)/ means:
		  
		  
		  Match any  characters as  few  as possible  until a  "abc" is  found,
		  without counting the "abc".
	- -