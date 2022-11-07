# Learning PHP 7

deck:: [[Other-Books::Learning PHP 7]]\
author:: [[Antonio Lopez]]\
full-title:: "Learning PHP 7"\
category:: #books\
\

![](https://images-na.ssl-images-amazon.com/images/I/514I--nQyqL._SL200_.jpg)

## Highlights
- 

The idea is simple: a configuration file specifies which base virtual machine we need to use from a set of available ones online and how you would like to customize it—that is, which commands you will want to run the first time you start the machine—this is called "provisioning". #flashcard 


    ([Location 385](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=385))
-
- 

You will probably get the Vagrant configuration from a public repository, and if this configuration ever changes, you can get the changes and reprovision your machine. It's easy, right? #flashcard 


    ([Location 387](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=387))
-
- 

$ vagrant up The first time you execute it, it will take some time as it will have to download the image from the repository, and then it will execute the provisioner.sh file. #flashcard 


    ([Location 420](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=420))
-
- 

HTTP stands for HyperText Transfer Protocol. As any other protocol, the goal is to allow two entities or nodes to communicate with each other. #flashcard  #pink #rosa 


    ([Location 578](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=578))
-
- 

HTTP is stateless; that is, it treats each request independently, unrelated to any previous one. This means that with this request and response sequence, the communication is finished. Any new requests will not be aware of this specific interchange of messages. #flashcard  #blue #azul 


    ([Location 588](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=588))
-
- 

The URL of the message is the destination of the message. The request will contain the receiver's URL, and the response will contain the sender's. #flashcard  #pink #rosa 


    ([Location 592](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=592))
-
- 

http://myserver.com/greeting?name=Alex. #flashcard  #orange #naranja 


    ([Location 595](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=595))
-
- 

The HTTP method is the verb of the message. #flashcard  #pink #rosa 


    ([Location 599](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=599))
-
- 

GET: This asks the receiver about something, and the receiver usually sends this information back. The most common example is asking for a web page, where the receiver will respond with the HTML code of the requested page. #flashcard  #blue #azul 


    ([Location 600](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=600))
-
- 

POST: This means that the sender wants to perform an action that will update the data that the receiver is holding. For example, the sender can ask the receiver to update his profile name. #flashcard  #blue #azul 


    ([Location 602](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=602))
-
- 

The body part is usually present in response messages even though a request message can contain it too. #flashcard  #blue #azul 


    ([Location 607](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=607))
-
- 

The headers on an HTTP message are the metadata that the receiver needs in order to understand the content of the message. #flashcard  #blue #azul 


    ([Location 613](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=613))
-
- 

The status code is present in responses. #flashcard  #blue #azul 


    ([Location 619](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=619))
-
- 

Common status codes are: #flashcard 


    ([Location 622](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=622))
-
- 

Representing the parameters as part of the body is a common way to send information when submitting a form, but not the only one. You can add a query string to the URL, add JSON to the body of the message, and so on. #flashcard 


    ([Location 633](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=633))
-
- 

rather all of them in a generic way. The main reason for this choice of terminology is to try to separate HTTP from web applications. You will see at the end of the book that HTTP is used for more than just websites. #flashcard 


    ([Location 639](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=639))
-
- 

A web page is a single document with content. It contains links that open other web pages with different content. #flashcard  #blue #azul 


    ([Location 642](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=642))
-
- 

A website is the set of web pages that usually live in the same server and are related to each other. #flashcard  #blue #azul 


    ([Location 644](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=644))
-
- 

A web application is just a piece of software that runs on a client, which is usually a browser, and communicates with a server. #flashcard  #pink #rosa 


    ([Location 645](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=645))
-
- 

A server is a remote machine that receives requests from a client, processes them, and generates a response. This response will go back to the client, generally rendered by the browser in order to display it to the user. #flashcard  #pink #rosa 


    ([Location 646](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=646))
-
- 

So, what is the difference between a website and a web application? Well, the web application can be a small part of a bigger website with a specific functionality. #flashcard  #blue #azul 


    ([Location 650](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=650))
-
- 

Also, not all websites are web applications as a web application always does something but a website can just display information. #flashcard  #blue #azul 


    ([Location 651](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=651))
-
- 

Different ways of including JS You might notice that we included the CSS file reference at the end of the <head> section and JS at the end of <body>. You can actually include JS in both the <head> and the <body>; just bear in mind that the script will be executed as soon as it is included. If your script references fields that are not yet defined or other JS files that will be included later, JS will fail. #flashcard 


    ([Location 684](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=684))
-
- 
 Recibiendo solicitudes por el protocolo HTTP #flashcard  #pink #rosa 
    A web server is no more than a piece of software running on a machine and listening to requests from a specific port.

    ([Location 692](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=692))
-
- 

The web server decides which web application—usually a file in the filesystem—needs to process the request. In order to decide, the web server usually considers the path of the URL; #flashcard 


    ([Location 702](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=702))
-
- 

There are powerful web servers that support high loads of traffic, such as Apache or Nginx, #flashcard  #pink #rosa 


    ([Location 709](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=709))
-
- 
 El servidor web (en este caso el embebido) busca el fichero index.php primero #flashcard  #orange #naranja 
    $ php -S localhost:8000

    ([Location 723](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=723))
-
- 

If you do not change the default options, PHP will always try to find an index.php file in the directory in which you started the web server. If this is not found, PHP will try to find an index.html file. #flashcard 


    ([Location 738](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=738))
-
- 

you have to start the file with <?php. There are other options, and you can also finish the file with ?>, #flashcard  #pink #rosa 


    ([Location 768](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=768))
-
- 

<?php   echo 'hello world'; ?> bye world #flashcard  #orange #naranja 


    ([Location 771](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=771))
-
- 

you will see that it prints both messages, hello world and bye world. The reason why this happens is simple: you already know that the PHP code there prints the hello world message. What happens next is that anything outside the PHP tags will be interpreted as is. If there is an HTML code for instance, it would not be printed as is, but will be interpreted by the browser. #flashcard 


    ([Location 772](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=772))
-
- 

include: This will try to find and include the specified file each time it is invoked. If the file is not found, PHP will throw a warning, but will continue with the execution. #flashcard  #blue #azul 


    ([Location 778](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=778))
-
- 

require: This will do the same as include, but PHP will throw an error instead of a warning if the file is not found. #flashcard  #blue #azul 


    ([Location 780](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=780))
-
- 

include_once: This function will do what include does, but it will include the file only the first time that it is invoked. Subsequent calls will be ignored. #flashcard  #blue #azul 


    ([Location 781](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=781))
-
- 

require_once: This works the same as require, but it will include the file only the first time that it is invoked. Subsequent calls will be ignored. #flashcard  #blue #azul 


    ([Location 782](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=782))
-
- 

Each function has its own usage, so it is not right to say that one is better than the other. #flashcard 


    ([Location 784](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=784))
-
- 

Moreover, as it is some HTML code, we might want to include it multiple times, so we did not choose the require_once option. #flashcard 


    ([Location 789](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=789))
-
- 

$a = 1; #flashcard  #orange #naranja 


    ([Location 802](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=802))
-
- 

PHP variables start with the $ sign followed by the variable name. A valid variable name starts with a letter or an underscore followed by any combination of letters, numbers, and/or underscores. It is case sensitive. #flashcard 


    ([Location 809](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=809))
-
- 

$1number = 12.3; // not valid! #flashcard  #orange #naranja 


    ([Location 811](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=811))
-
- 

PHP has eight primitive types, but for now, we will focus on its four scalar types: #flashcard 


    ([Location 818](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=818))
-
- 

Exponentiation (**) raises the first operand to the power of the second. #flashcard 


    ([Location 853](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=853))
-
- 

var_dump(1 <=> 2); // int less than 0 var_dump(1 <=> 1); // 0 var_dump(3 <=> 2); // int greater than 0 #flashcard  #orange #naranja 


    ([Location 877](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=877))
-
- 

The == (equals) operator evaluates two expressions after type juggling, that is, it will try to transform both expressions to the same type, and then compare them. Instead, the === (identical) operator evaluates two expressions without type juggling, so even if they look the same, if they are not of the same type, the comparison will return false. The same applies to != or <> (not equal to) and !== (not identical): #flashcard  #blue #azul 


    ([Location 879](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=879))
-
- 

You can find the entire list of functions at http://php.net/manual/en/ref.strings.php, #flashcard 


    ([Location 953](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=953))
-
- 

strlen: This function returns the number of characters that the string contains. #flashcard  #blue #azul 


    ([Location 960](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=960))
-
- 

trim: This function returns the string, removing all the blank spaces to the left and to the right. #flashcard  #blue #azul 


    ([Location 961](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=961))
-
- 

strtoupper and strtolower: These functions return the string with all the characters in upper or lower case respectively. #flashcard  #blue #azul 


    ([Location 962](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=962))
-
- 

str_replace: This function replaces all occurrences of a given string by the replacement string. #flashcard  #blue #azul 


    ([Location 963](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=963))
-
- 

substr: This function extracts the string contained between the positions specified by parameters, with the first character being at position 0. #flashcard  #blue #azul 


    ([Location 964](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=964))
-
- 

strpos: This function shows the position of the first occurrence of the given string. It returns false if the string cannot be found. #flashcard  #blue #azul 


    ([Location 966](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=966))
-
- 

there is an operator for strings (.) which concatenates two strings #flashcard  #blue #azul 


    ([Location 967](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=967))
-
- 

$empty1 = []; $empty2 = array(); $names1 = ['Harry', 'Ron', 'Hermione']; $names2 = array('Harry', 'Ron', 'Hermione'); #flashcard  #orange #naranja 


    ([Location 998](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=998))
-
- 

$status1 = [     'name' => 'James Potter',     'status' => 'dead' ]; $status2 = array(     'name' => 'James Potter',     'status' => 'dead' ); #flashcard  #orange #naranja 


    ([Location 999](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=999))
-
- 
 Para hacer append del array #flashcard  #orange #naranja 
    $names[] = 'Neville';

    ([Location 1018](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1018))
-
- 
 Para eliminar un elemento. 'status' es la clave a eliminar #flashcard  #orange #naranja 
    unset($status['status']);

    ([Location 1029](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1029))
-
- 

the empty function. That function actually works with strings too, an empty string being a string with no characters (' '). #flashcard 


    ([Location 1050](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1050))
-
- 

The isset function takes an array position, and returns true or false depending on whether that position exists or not: #flashcard  #blue #azul 


    ([Location 1051](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1051))
-
- 

empty($string)); #flashcard  #orange #naranja 


    ([Location 1053](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1053))
-
- 

isset($names[3])); #flashcard  #orange #naranja 


    ([Location 1054](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1054))
-
- 

in_array. This function takes two values, the value that you want to search for and the array. The function returns true if the value is in the array and false otherwise. #flashcard  #blue #azul 


    ([Location 1060](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1060))
-
- 

array_search. This function works in the same way except that instead of returning a Boolean, it returns the key where the value is found, or false otherwise. #flashcard  #blue #azul 


    ([Location 1063](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1063))
-
- 
 e #flashcard  #orange #naranja 
    $containsHermione = in_array('Hermione', $names);

    ([Location 1065](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1065))
-
- 

$wheresVoldemort = array_search('Voldemort', $names); #flashcard  #orange #naranja 


    ([Location 1068](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1068))
-
- 

sort, orders the values alphabetically. #flashcard  #blue #azul 


    ([Location 1111](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1111))
-
- 

asort orders the values in the same way, but keeps the association of key-values. #flashcard  #blue #azul 


    ([Location 1112](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1112))
-
- 

ksort orders the elements by their keys, alphabetically. #flashcard  #blue #azul 


    ([Location 1113](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1113))
-
- 

An a in the name means associative, and thus, will preserve the key-value association. An r in the name means reverse, so the order will be from high to low. A k means key, so the sorting will be based on the keys instead of the values. #flashcard 


    ([Location 1118](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1118))
-
- 

We can get a list of the keys of the array with array_keys, and a list of its values with array_values: #flashcard  #blue #azul 


    ([Location 1124](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1124))
-
- 

We can get the number of elements in an array with the count function: #flashcard  #blue #azul 


    ([Location 1128](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1128))
-
- 

we can merge two or more arrays into one with array_merge: #flashcard  #blue #azul 


    ([Location 1131](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1131))
-
- 

PHP stores all the parameters that come from the query string in an array called $_GET. #flashcard  #blue #azul 


    ([Location 1157](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1157))
-
- 

When printing something with echo, PHP tries to transform everything it gets into strings. Since the string version of the Boolean false is an empty string, that would not be useful for our application. Casting the Boolean to an integer first assures that we will see a value, even if it is just a 0. #flashcard 


    ([Location 1172](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1172))
-
- 

with great power comes great responsibility, #flashcard 


    ([Location 1235](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1235))
-
- 

<?php if ($submitted): ?> #flashcard  #orange #naranja 


    ([Location 1293](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1293))
-
- 

<?php else: ?> #flashcard  #orange #naranja 


    ([Location 1296](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1296))
-
- 

<?php endif; ?> #flashcard  #orange #naranja 


    ([Location 1297](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1297))
-
- 

foreach ($names as $name) {     echo $name . " "; } #flashcard  #orange #naranja 


    ([Location 1373](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1373))
-
- 

foreach ($names as $key => $name) {     echo $key . " -> " . $name . " "; } #flashcard  #orange #naranja 


    ([Location 1374](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1374))
-
- 

<?php if (!$book['available']): ?>           <b>Not available</b> <?php endif; ?>         </li> <?php endforeach; ?> #flashcard  #orange #naranja 


    ([Location 1395](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1395))
-
- 

PHP does not support overloaded functions. #flashcard  #pink #rosa 


    ([Location 1416](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1416))
-
- 

As you can see, you can declare the arguments without knowing what their types are, so PHP would not be able to decide which function to use. #flashcard 


    ([Location 1417](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1417))
-
- 

pass the argument by reference. To do that, you add an ampersand (&) before the argument when declaring the function: #flashcard  #blue #azul 


    ([Location 1442](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1442))
-
- 

function modify(&$a) {     $a = 3; } #flashcard  #orange #naranja 


    ([Location 1444](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1444))
-
- 

Usually, when someone uses a function, they expect a result, and they do not want the arguments provided by them to be modified. So try to avoid it; people will be grateful! #flashcard 


    ([Location 1449](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1449))
-
- 

declare(strict_types=1); #flashcard  #orange #naranja 


    ([Location 1467](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1467))
-
- 

function addNumbers(int $a, int $b, bool $printSum): int { #flashcard  #orange #naranja 


    ([Location 1467](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1467))
-
- 

file_put_contents(__DIR__ . '/books.json', $booksJson); #flashcard  #orange #naranja 


    ([Location 1569](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1569))
-
- 

$booksJson = json_encode($books); #flashcard  #orange #naranja 


    ([Location 1569](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1569))
-
- 

public function __construct(int $isbn, string $title, string $author, int $available) { #flashcard  #orange #naranja 


    ([Location 1665](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1665))
-
- 

__toString: This method is invoked when we try to cast an object to a string. #flashcard  #blue #azul 


    ([Location 1687](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1687))
-
- 

rules. Each time you reference a class that PHP does not know about, it will ask the autoloader. If the autoloader can figure out which file that class is in, it will load it, and the execution of the program will continue as normal. If it does not, PHP will stop the execution. #flashcard  #pink #rosa 


    ([Location 1868](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1868))
-
- 

So, what is the autoloader? It is no more than a PHP function that gets a class name as a parameter, and it is expected to load a file. #flashcard  #blue #azul 


    ([Location 1871](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1871))
-
- 

class Customer extends Person { #flashcard  #orange #naranja 


    ([Location 1932](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1932))
-
- 

parent::__construct($firstname, $surname); #flashcard  #orange #naranja 


    ([Location 1954](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1954))
-
- 

interface Customer { #flashcard  #orange #naranja 


    ([Location 2073](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=2073))
-
- 

class Basic implements Customer { #flashcard  #orange #naranja 


    ([Location 2083](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=2083))
-
