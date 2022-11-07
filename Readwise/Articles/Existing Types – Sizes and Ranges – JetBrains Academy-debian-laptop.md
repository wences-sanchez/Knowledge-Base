# Existing Types – Sizes and Ranges – JetBrains Academy

deck:: [[Across-the-Net]]\
author:: [[hyperskill.org]]\
full-title:: "Existing Types – Sizes and Ranges – JetBrains Academy"\
category:: #articles\
url:: https://hyperskill.org/learn/step/3510\

![](https://readwise-assets.s3.amazonaws.com/static/images/article1.be68295a7e40.png)
## Highlights
- id:: 63639906-42cf-47c5-b70d-c4c2d0033700
   About implicit type casting precision .java #flashcard 
    In some cases, implicit type casting may be a bit lossy. When we convert an int to float, or a long to float or to double, we may lose some less significant bits of the value, which will result in the loss of precision. However, the result of this conversion will be a correctly rounded version of the integer value, which will be in the overall range of the target type. To understand that, check out the example:
     long bigLong =  1_200_000_002L;float bigFloat = bigLong; // 1.2E9 (= 1_200_000_000)
-
- id:: 63639906-ad87-4772-b131-51530f12ab4b
  
  As you remember, in Java long is a 64-bit number, while int is 32-bit. When converting long to int the program just takes the last 32 bits to represent the new number. If the long contains a number less than or equal to Integer.MAX_VALUE you can convert it by casting without losing information. Otherwise, the result will be quite meaningless, although determined. That is why you shouldn't perform casting from a larger type to a smaller type unless you are absolutely sure that it is necessary, and that truncation will not interfere with your program. #flashcard
-
- id:: 63639906-296c-4071-bc46-320538e41363
  
  If you want to cast a narrower type to a wider type, you do not need to write anything, the Java compiler will do it automatically for you. But if you want the opposite, specify the required type in parentheses following the assignment operator. Keep in mind, the boolean type cannot be cast to another type and vice versa. #flashcard
-