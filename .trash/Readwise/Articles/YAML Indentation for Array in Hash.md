# YAML Indentation for Array in Hash

deck:: [[Across-the-Net]]\
author:: [[stackoverflow.com]]\
full-title:: "YAML Indentation for Array in Hash"\
category:: #articles\
url:: https://stackoverflow.com/questions/17014460/yaml-indentation-for-array-in-hash\

![](https://readwise-assets.s3.amazonaws.com/static/images/article2.74d541386bbf.png)

## Highlights
- 
 Which is the preferred way of indentation of dashes in YAML? .code #flashcard 
    Both ways are valid, as far as I can tell:
     require 'yaml'
     YAML.load(%q{--- 
     1:
     - 1
     - 2
     - 3
     })
     # => {1=>[1, 2, 3]}
     YAML.load(%q{--- 
     1:
     - 1
     - 2
     - 3
     })
     # => {1=>[1, 2, 3]}
     It's not clear why you think there should be spaces before the hyphens. If you think this is a violation of the spec, please explain how.
     Why isn't there indentation for the array?
     There's no need for indentation before the hyphens, and it's simpler not to add any.

    
-
