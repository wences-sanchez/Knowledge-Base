title:: Learning PHP 7 (highlights)
deck:: [[Other-Books::Learning PHP 7]]
author:: [[Antonio Lopez]]
full-title:: "Learning PHP 7"
category:: #books

- ![](https://images-na.ssl-images-amazon.com/images/I/514I--nQyqL._SL200_.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- The idea is simple: a configuration file specifies which base virtual machine we need to use from a set of available ones online and how you would like to customize it—that is, which commands you will want to run the first time you start the machine—this is called "provisioning". #flashcard
		  id:: 59241016-0ae0-4ec0-9b58-00f6900f4dcb
		- ([Location 385](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=385))
	- -
	- -
		- You will probably get the Vagrant configuration from a public repository, and if this configuration ever changes, you can get the changes and reprovision your machine. It's easy, right? #flashcard
		  id:: 273cf50d-5a62-41d6-94f7-8240750504d7
		- ([Location 387](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=387))
	- -
	- -
		- $ vagrant up The first time you execute it, it will take some time as it will have to download the image from the repository, and then it will execute the provisioner.sh file. #flashcard
		  id:: 3dea4431-bee7-4641-8f82-638d5f656a8a
		- ([Location 420](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=420))
	- -
	- -
		- HTTP stands for HyperText Transfer Protocol. As any other protocol, the goal is to allow two entities or nodes to communicate with each other. #flashcard
		  id:: af04959e-5d5f-44fd-bde4-96187d9a2824
		- tags:: [[pink]] [[rosa]]
		- ([Location 578](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=578))
	- -
	- -
		- HTTP is stateless; that is, it treats each request independently, unrelated to any previous one. This means that with this request and response sequence, the communication is finished. Any new requests will not be aware of this specific interchange of messages. #flashcard
		  id:: 9f08f28c-d821-48d1-b381-c96fd34fcf75
		- tags:: [[blue]] [[azul]]
		- ([Location 588](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=588))
	- -
	- -
		- The URL of the message is the destination of the message. The request will contain the receiver's URL, and the response will contain the sender's. #flashcard
		  id:: 45e8fb63-1e54-41b1-a475-f3aaf1b8cb7d
		- tags:: [[pink]] [[rosa]]
		- ([Location 592](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=592))
	- -
	- -
		- http://myserver.com/greeting?name=Alex. #flashcard
		  id:: 7b01b2ff-b4e1-419d-9301-b48d97f9527f
		- tags:: [[orange]] [[naranja]]
		- ([Location 595](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=595))
	- -
	- -
		- The HTTP method is the verb of the message. #flashcard
		  id:: bca4a194-06e7-43bb-903b-3ec4998d8fa6
		- tags:: [[pink]] [[rosa]]
		- ([Location 599](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=599))
	- -
	- -
		- GET: This asks the receiver about something, and the receiver usually sends this information back. The most common example is asking for a web page, where the receiver will respond with the HTML code of the requested page. #flashcard
		  id:: 476a5d4b-f0f9-44bf-ba18-51a0b0ad99f8
		- tags:: [[blue]] [[azul]]
		- ([Location 600](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=600))
	- -
	- -
		- POST: This means that the sender wants to perform an action that will update the data that the receiver is holding. For example, the sender can ask the receiver to update his profile name. #flashcard
		  id:: 0e314903-ac60-4ea5-99f1-b30dfd1bbd3e
		- tags:: [[blue]] [[azul]]
		- ([Location 602](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=602))
	- -
	- -
		- The body part is usually present in response messages even though a request message can contain it too. #flashcard
		  id:: 0651461c-ccb3-41dd-a596-f679248948ce
		- tags:: [[blue]] [[azul]]
		- ([Location 607](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=607))
	- -
	- -
		- The headers on an HTTP message are the metadata that the receiver needs in order to understand the content of the message. #flashcard
		  id:: fc7fd5ea-7040-41c5-bdb9-a9471c169c17
		- tags:: [[blue]] [[azul]]
		- ([Location 613](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=613))
	- -
	- -
		- The status code is present in responses. #flashcard
		  id:: 5949adcd-887e-44a1-b73d-0eacc08cbb4d
		- tags:: [[blue]] [[azul]]
		- ([Location 619](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=619))
	- -
	- -
		- Common status codes are: #flashcard
		  id:: 86fc1e0d-9d9c-47ce-ba2f-5368fc0cc20a
		- ([Location 622](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=622))
	- -
	- -
		- Representing the parameters as part of the body is a common way to send information when submitting a form, but not the only one. You can add a query string to the URL, add JSON to the body of the message, and so on. #flashcard
		  id:: 957c84b5-1c78-4347-bfb6-20465a783ebf
		- ([Location 633](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=633))
	- -
	- -
		- rather all of them in a generic way. The main reason for this choice of terminology is to try to separate HTTP from web applications. You will see at the end of the book that HTTP is used for more than just websites. #flashcard
		  id:: ad9ed1eb-2da0-4562-a15c-075a86f06638
		- ([Location 639](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=639))
	- -
	- -
		- A web page is a single document with content. It contains links that open other web pages with different content. #flashcard
		  id:: a4e87622-9d22-4da8-bd20-59caf1833a0f
		- tags:: [[blue]] [[azul]]
		- ([Location 642](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=642))
	- -
	- -
		- A website is the set of web pages that usually live in the same server and are related to each other. #flashcard
		- tags:: [[blue]] [[azul]]
		- ([Location 644](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=644))
	- -
	- -
		- A web application is just a piece of software that runs on a client, which is usually a browser, and communicates with a server. #flashcard
		  id:: 33c32379-9c04-4904-9873-30c6b751e4fd
		- tags:: [[pink]] [[rosa]]
		- ([Location 645](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=645))
	- -
	- -
		- A server is a remote machine that receives requests from a client, processes them, and generates a response. This response will go back to the client, generally rendered by the browser in order to display it to the user. #flashcard
		- tags:: [[pink]] [[rosa]]
		- ([Location 646](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=646))
	- -
	- -
		- So, what is the difference between a website and a web application? Well, the web application can be a small part of a bigger website with a specific functionality. #flashcard
		  id:: c6f260cd-b24f-441a-84dc-ed7f6ac8b787
		- tags:: [[blue]] [[azul]]
		- ([Location 650](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=650))
	- -
	- -
		- Also, not all websites are web applications as a web application always does something but a website can just display information. #flashcard
		  id:: af38c5a3-e37c-45a9-8170-a9698ba82da1
		- tags:: [[blue]] [[azul]]
		- ([Location 651](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=651))
	- -
	- -
		- Different ways of including JS You might notice that we included the CSS file reference at the end of the <head> section and JS at the end of <body>. You can actually include JS in both the <head> and the <body>; just bear in mind that the script will be executed as soon as it is included. If your script references fields that are not yet defined or other JS files that will be included later, JS will fail. #flashcard
		- ([Location 684](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=684))
	- -
	- -
		- Recibiendo solicitudes por el protocolo HTTP #flashcard
		  id:: 8675fc8c-9d4d-428b-b952-13f3a0d75c6c
			- A web server is no more than a piece of software running on a machine and listening to requests from a specific port.
		- tags:: [[pink]] [[rosa]]
		- ([Location 692](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=692))
	- -
	- -
		- The web server decides which web application—usually a file in the filesystem—needs to process the request. In order to decide, the web server usually considers the path of the URL; #flashcard
		  id:: 5f14f63c-6d1f-4e49-9c66-1370dc4cf45c
		- ([Location 702](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=702))
	- -
	- -
		- There are powerful web servers that support high loads of traffic, such as Apache or Nginx, #flashcard
		  id:: 90efd906-1e84-4864-8537-a38a80f1f477
		- tags:: [[pink]] [[rosa]]
		- ([Location 709](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=709))
	- -
	- -
		- El servidor web (en este caso el embebido) busca el fichero index.php primero #flashcard
		  id:: e15c8a03-6ac6-4dad-83a9-9710f8678f6a
			- $ php -S localhost:8000
		- tags:: [[orange]] [[naranja]]
		- ([Location 723](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=723))
	- -
	- -
		- If you do not change the default options, PHP will always try to find an index.php file in the directory in which you started the web server. If this is not found, PHP will try to find an index.html file. #flashcard
		  id:: 60b4a83f-c176-46a9-b230-a2caa89e87a4
		- ([Location 738](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=738))
	- -
	- -
		- you have to start the file with <?php. There are other options, and you can also finish the file with ?>, #flashcard
		  id:: 23efee9b-6f77-4853-a202-ddbdbb49278c
		- tags:: [[pink]] [[rosa]]
		- ([Location 768](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=768))
	- -
	- -
		- <?php   echo 'hello world'; ?> bye world #flashcard
		  id:: 74e16ae0-c2b7-4eea-9be3-496b07c1ebc1
		- tags:: [[orange]] [[naranja]]
		- ([Location 771](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=771))
	- -
	- -
		- you will see that it prints both messages, hello world and bye world. The reason why this happens is simple: you already know that the PHP code there prints the hello world message. What happens next is that anything outside the PHP tags will be interpreted as is. If there is an HTML code for instance, it would not be printed as is, but will be interpreted by the browser. #flashcard
		  id:: d2d22695-5dda-4b53-9f5f-1ed73fa92274
		- ([Location 772](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=772))
	- -
	- -
		- include: This will try to find and include the specified file each time it is invoked. If the file is not found, PHP will throw a warning, but will continue with the execution. #flashcard
		  id:: 3959c54a-d04f-4d58-8a10-23820c68032b
		- tags:: [[blue]] [[azul]]
		- ([Location 778](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=778))
	- -
	- -
		- require: This will do the same as include, but PHP will throw an error instead of a warning if the file is not found. #flashcard
		  id:: 0b25d837-aa4f-4669-aafc-221cc88062e6
		- tags:: [[blue]] [[azul]]
		- ([Location 780](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=780))
	- -
	- -
		- include_once: This function will do what include does, but it will include the file only the first time that it is invoked. Subsequent calls will be ignored. #flashcard
		  id:: 09a9d05f-dc31-4b41-b3e5-90ae73bdc309
		- tags:: [[blue]] [[azul]]
		- ([Location 781](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=781))
	- -
	- -
		- require_once: This works the same as require, but it will include the file only the first time that it is invoked. Subsequent calls will be ignored. #flashcard
		  id:: 5baf0b68-7923-4d2f-a186-33876589f525
		- tags:: [[blue]] [[azul]]
		- ([Location 782](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=782))
	- -
	- -
		- Each function has its own usage, so it is not right to say that one is better than the other. #flashcard
		  id:: ab7d8413-00e6-44a7-a02e-301bc8447f04
		- ([Location 784](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=784))
	- -
	- -
		- Moreover, as it is some HTML code, we might want to include it multiple times, so we did not choose the require_once option. #flashcard
		  id:: 2f04e282-4589-480c-a561-92e1e9e31382
		- ([Location 789](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=789))
	- -
	- -
		- $a = 1; #flashcard
		  id:: c717e89f-b3bb-43fa-9bdc-aa4c73de665d
		- tags:: [[orange]] [[naranja]]
		- ([Location 802](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=802))
	- -
	- -
		- PHP variables start with the $ sign followed by the variable name. A valid variable name starts with a letter or an underscore followed by any combination of letters, numbers, and/or underscores. It is case sensitive. #flashcard
		  id:: d9f7a2ea-aa38-430e-99ab-237e23515bb5
		- ([Location 809](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=809))
	- -
	- -
		- $1number = 12.3; // not valid! #flashcard
		  id:: 64f2a5f1-2bdb-4c18-a747-ba7fa62d1435
		- tags:: [[orange]] [[naranja]]
		- ([Location 811](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=811))
	- -
	- -
		- PHP has eight primitive types, but for now, we will focus on its four scalar types: #flashcard
		  id:: c699d93b-dd00-4259-9e1e-e5ad9202f138
		- ([Location 818](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=818))
	- -
	- -
		- Exponentiation (**) raises the first operand to the power of the second. #flashcard
		  id:: 05bf3971-160a-414e-8c22-313aecf4895a
		- ([Location 853](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=853))
	- -
	- -
		- var_dump(1 <=> 2); // int less than 0 var_dump(1 <=> 1); // 0 var_dump(3 <=> 2); // int greater than 0 #flashcard
		  id:: 3948bade-6044-45f3-bebd-e9b21cdc7180
		- tags:: [[orange]] [[naranja]]
		- ([Location 877](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=877))
	- -
	- -
		- The == (equals) operator evaluates two expressions after type juggling, that is, it will try to transform both expressions to the same type, and then compare them. Instead, the === (identical) operator evaluates two expressions without type juggling, so even if they look the same, if they are not of the same type, the comparison will return false. The same applies to != or <> (not equal to) and !== (not identical): #flashcard
		  id:: c64eee72-ce6e-4a31-8ab9-b69e1a4deeb2
		- tags:: [[blue]] [[azul]]
		- ([Location 879](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=879))
	- -
	- -
		- You can find the entire list of functions at http://php.net/manual/en/ref.strings.php, #flashcard
		  id:: 2b5f96e5-db1e-469e-ae72-52a14b461c3d
		- ([Location 953](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=953))
	- -
	- -
		- strlen: This function returns the number of characters that the string contains. #flashcard
		  id:: 97d9277e-1a02-4426-abc6-9715ef6646ea
		- tags:: [[blue]] [[azul]]
		- ([Location 960](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=960))
	- -
	- -
		- trim: This function returns the string, removing all the blank spaces to the left and to the right. #flashcard
		  id:: 94d7a113-0bf7-4bf3-96cc-57937c8fe734
		- tags:: [[blue]] [[azul]]
		- ([Location 961](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=961))
	- -
	- -
		- strtoupper and strtolower: These functions return the string with all the characters in upper or lower case respectively. #flashcard
		  id:: c10091c9-5a9e-4001-8dbd-a7dc25522d24
		- tags:: [[blue]] [[azul]]
		- ([Location 962](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=962))
	- -
	- -
		- str_replace: This function replaces all occurrences of a given string by the replacement string. #flashcard
		  id:: 2654eaea-bddf-4e0a-b64f-189c9777c340
		- tags:: [[blue]] [[azul]]
		- ([Location 963](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=963))
	- -
	- -
		- substr: This function extracts the string contained between the positions specified by parameters, with the first character being at position 0. #flashcard
		- tags:: [[blue]] [[azul]]
		- ([Location 964](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=964))
	- -
	- -
		- strpos: This function shows the position of the first occurrence of the given string. It returns false if the string cannot be found. #flashcard
		  id:: 2b6d06ba-e7ad-4011-95bc-e04afc3c6b13
		- tags:: [[blue]] [[azul]]
		- ([Location 966](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=966))
	- -
	- -
		- there is an operator for strings (.) which concatenates two strings #flashcard
		  id:: 68636a4a-f205-4914-9fb4-ff08ed4e1216
		- tags:: [[blue]] [[azul]]
		- ([Location 967](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=967))
	- -
	- -
		- $empty1 = []; $empty2 = array(); $names1 = ['Harry', 'Ron', 'Hermione']; $names2 = array('Harry', 'Ron', 'Hermione'); #flashcard
		  id:: e643eb0a-ee43-49a6-9c9c-eeee608d2872
		- tags:: [[orange]] [[naranja]]
		- ([Location 998](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=998))
	- -
	- -
		- $status1 = [     'name' => 'James Potter',     'status' => 'dead' ]; $status2 = array(     'name' => 'James Potter',     'status' => 'dead' ); #flashcard
		  id:: 84cdacac-4d63-4a82-b007-b244d62511fa
		- tags:: [[orange]] [[naranja]]
		- ([Location 999](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=999))
	- -
	- -
		- Para hacer append del array #flashcard
		  id:: 22c41b4c-76b8-434d-9742-f11c83300a04
			- $names[] = 'Neville';
		- tags:: [[orange]] [[naranja]]
		- ([Location 1018](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1018))
	- -
	- -
		- Para eliminar un elemento. 'status' es la clave a eliminar #flashcard
		  id:: 573a3638-9cb6-42cb-a5ba-e8bd4b9afbac
			- unset($status['status']);
		- tags:: [[orange]] [[naranja]]
		- ([Location 1029](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1029))
	- -
	- -
		- the empty function. That function actually works with strings too, an empty string being a string with no characters (' '). #flashcard
		  id:: 4d9ed434-175d-4420-9819-268526b221af
		- ([Location 1050](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1050))
	- -
	- -
		- The isset function takes an array position, and returns true or false depending on whether that position exists or not: #flashcard
		  id:: d5aedf4e-bc76-4e44-a480-e5bb4c193b47
		- tags:: [[blue]] [[azul]]
		- ([Location 1051](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1051))
	- -
	- -
		- empty($string)); #flashcard
		  id:: 7996d2d4-1c2e-426b-890e-a635f238afe2
		- tags:: [[orange]] [[naranja]]
		- ([Location 1053](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1053))
	- -
	- -
		- isset($names[3])); #flashcard
		  id:: cbbb0a99-d7a3-48d4-a955-31efd2cb1799
		- tags:: [[orange]] [[naranja]]
		- ([Location 1054](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1054))
	- -
	- -
		- in_array. This function takes two values, the value that you want to search for and the array. The function returns true if the value is in the array and false otherwise. #flashcard
		  id:: 1a12e8c4-c79c-4e3f-a6dc-43db2c7aea4c
		- tags:: [[blue]] [[azul]]
		- ([Location 1060](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1060))
	- -
	- -
		- array_search. This function works in the same way except that instead of returning a Boolean, it returns the key where the value is found, or false otherwise. #flashcard
		  id:: fc132a9e-aa14-4130-be93-628bd85ffea1
		- tags:: [[blue]] [[azul]]
		- ([Location 1063](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1063))
	- -
	- -
		- e #flashcard
		  id:: cd04b6f6-5e98-49cc-82b8-0953dc4f6159
			- $containsHermione = in_array('Hermione', $names);
		- tags:: [[orange]] [[naranja]]
		- ([Location 1065](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1065))
	- -
	- -
		- $wheresVoldemort = array_search('Voldemort', $names); #flashcard
		  id:: 4c05bc5e-c29c-4340-a26a-0ec1eb222959
		- tags:: [[orange]] [[naranja]]
		- ([Location 1068](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1068))
	- -
	- -
		- sort, orders the values alphabetically. #flashcard
		  id:: 7562bd7f-0502-4db7-a165-f84cff113330
		- tags:: [[blue]] [[azul]]
		- ([Location 1111](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1111))
	- -
	- -
		- asort orders the values in the same way, but keeps the association of key-values. #flashcard
		  id:: 2d6aa8a2-1dd0-43e4-b037-a22d46ba2e3b
		- tags:: [[blue]] [[azul]]
		- ([Location 1112](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1112))
	- -
	- -
		- ksort orders the elements by their keys, alphabetically. #flashcard
		  id:: bd275d0e-5faa-4f3b-8ac1-25feef8501d2
		- tags:: [[blue]] [[azul]]
		- ([Location 1113](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1113))
	- -
	- -
		- An a in the name means associative, and thus, will preserve the key-value association. An r in the name means reverse, so the order will be from high to low. A k means key, so the sorting will be based on the keys instead of the values. #flashcard
		  id:: 171114a3-cd9b-4123-80b8-641eeddbae9d
		- ([Location 1118](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1118))
	- -
	- -
		- We can get a list of the keys of the array with array_keys, and a list of its values with array_values: #flashcard
		  id:: f288d00b-7b24-4991-9b26-55fbf419d219
		- tags:: [[blue]] [[azul]]
		- ([Location 1124](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1124))
	- -
	- -
		- We can get the number of elements in an array with the count function: #flashcard
		  id:: 9a1a3b7f-f7df-4e5e-a26a-769c800da2a5
		- tags:: [[blue]] [[azul]]
		- ([Location 1128](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1128))
	- -
	- -
		- we can merge two or more arrays into one with array_merge: #flashcard
		- tags:: [[blue]] [[azul]]
		- ([Location 1131](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1131))
	- -
	- -
		- PHP stores all the parameters that come from the query string in an array called $_GET. #flashcard
		  id:: 5d819481-0510-4734-bcb0-578b035312cf
		- tags:: [[blue]] [[azul]]
		- ([Location 1157](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1157))
	- -
	- -
		- When printing something with echo, PHP tries to transform everything it gets into strings. Since the string version of the Boolean false is an empty string, that would not be useful for our application. Casting the Boolean to an integer first assures that we will see a value, even if it is just a 0. #flashcard
		  id:: a08fe2b1-daf2-4167-ae1a-30c662e823e7
		- ([Location 1172](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1172))
	- -
	- -
		- with great power comes great responsibility, #flashcard
		  id:: 8b881f64-db4a-42d3-9c56-c496fd14114d
		- ([Location 1235](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1235))
	- -
	- -
		- <?php if ($submitted): ?> #flashcard
		- tags:: [[orange]] [[naranja]]
		- ([Location 1293](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1293))
	- -
	- -
		- <?php else: ?> #flashcard
		  id:: ef6a49e9-f5f0-4d0e-9245-a4c11e32c3ee
		- tags:: [[orange]] [[naranja]]
		- ([Location 1296](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1296))
	- -
	- -
		- <?php endif; ?> #flashcard
		  id:: 959dce77-8551-4778-94ed-656831dd1548
		- tags:: [[orange]] [[naranja]]
		- ([Location 1297](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1297))
	- -
	- -
		- foreach ($names as $name) {     echo $name . " "; } #flashcard
		  id:: 539d7eb5-609c-423f-bb44-9bc66fdd594d
		- tags:: [[orange]] [[naranja]]
		- ([Location 1373](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1373))
	- -
	- -
		- foreach ($names as $key => $name) {     echo $key . " -> " . $name . " "; } #flashcard
		  id:: 713a616f-8a49-445d-ac00-0727de48964e
		- tags:: [[orange]] [[naranja]]
		- ([Location 1374](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1374))
	- -
	- -
		- <?php if (!$book['available']): ?>           <b>Not available</b> <?php endif; ?>         </li> <?php endforeach; ?> #flashcard
		  id:: 63fe2b7f-afd4-47b3-bff1-9fbc781d540a
		- tags:: [[orange]] [[naranja]]
		- ([Location 1395](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1395))
	- -
	- -
		- PHP does not support overloaded functions. #flashcard
		- tags:: [[pink]] [[rosa]]
		- ([Location 1416](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1416))
	- -
	- -
		- As you can see, you can declare the arguments without knowing what their types are, so PHP would not be able to decide which function to use. #flashcard
		  id:: 7a8871c9-5343-4a69-9784-8cbfeb67d006
		- ([Location 1417](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1417))
	- -
	- -
		- pass the argument by reference. To do that, you add an ampersand (&) before the argument when declaring the function: #flashcard
		  id:: b208f4ac-1ea0-4457-b8da-383c80522189
		- tags:: [[blue]] [[azul]]
		- ([Location 1442](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1442))
	- -
	- -
		- function modify(&$a) {     $a = 3; } #flashcard
		  id:: ce3a400d-e33f-4719-959b-08743d1549bb
		- tags:: [[orange]] [[naranja]]
		- ([Location 1444](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1444))
	- -
	- -
		- Usually, when someone uses a function, they expect a result, and they do not want the arguments provided by them to be modified. So try to avoid it; people will be grateful! #flashcard
		- ([Location 1449](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1449))
	- -
	- -
		- declare(strict_types=1); #flashcard
		  id:: a3d005ae-b885-4d93-baed-91bcf459b7c1
		- tags:: [[orange]] [[naranja]]
		- ([Location 1467](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1467))
	- -
	- -
		- function addNumbers(int $a, int $b, bool $printSum): int { #flashcard
		  id:: bcc3a7b9-d377-4215-9baf-e06f58fbc32e
		- tags:: [[orange]] [[naranja]]
		- ([Location 1467](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1467))
	- -
	- -
		- file_put_contents(__DIR__ . '/books.json', $booksJson); #flashcard
		  id:: 8c89ee34-3f33-4fcf-9fd5-1b524f178dde
		- tags:: [[orange]] [[naranja]]
		- ([Location 1569](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1569))
	- -
	- -
		- $booksJson = json_encode($books); #flashcard
		  id:: e7ba948c-283f-4f10-ae38-18b967f20f72
		- tags:: [[orange]] [[naranja]]
		- ([Location 1569](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1569))
	- -
	- -
		- public function __construct(int $isbn, string $title, string $author, int $available) { #flashcard
		- tags:: [[orange]] [[naranja]]
		- ([Location 1665](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1665))
	- -
	- -
		- __toString: This method is invoked when we try to cast an object to a string. #flashcard
		- tags:: [[blue]] [[azul]]
		- ([Location 1687](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1687))
	- -
	- -
		- rules. Each time you reference a class that PHP does not know about, it will ask the autoloader. If the autoloader can figure out which file that class is in, it will load it, and the execution of the program will continue as normal. If it does not, PHP will stop the execution. #flashcard
		  id:: 7aecf990-2c3a-4fb8-aeec-4e0724282b07
		- tags:: [[pink]] [[rosa]]
		- ([Location 1868](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1868))
	- -
	- -
		- So, what is the autoloader? It is no more than a PHP function that gets a class name as a parameter, and it is expected to load a file. #flashcard
		  id:: 1b7da377-cf5b-42a5-a914-223a810ae3ed
		- tags:: [[blue]] [[azul]]
		- ([Location 1871](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1871))
	- -
	- -
		- class Customer extends Person { #flashcard
		  id:: ebc480d3-8123-4f89-bd40-480282e57c2e
		- tags:: [[orange]] [[naranja]]
		- ([Location 1932](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1932))
	- -
	- -
		- parent::__construct($firstname, $surname); #flashcard
		  id:: 928561fc-08db-4212-8d84-1a52c601a747
		- tags:: [[orange]] [[naranja]]
		- ([Location 1954](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=1954))
	- -
	- -
		- interface Customer { #flashcard
		  id:: 100b8cba-3e9f-4507-8ded-0897b1b2c186
		- tags:: [[orange]] [[naranja]]
		- ([Location 2073](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=2073))
	- -
	- -
		- class Basic implements Customer { #flashcard
		  id:: 42de2e0d-3692-4dfc-a6a0-c7ca79e5efbd
		- tags:: [[orange]] [[naranja]]
		- ([Location 2083](https://readwise.io/to_kindle?action=open&asin=B01ALMQ550&location=2083))
	- -