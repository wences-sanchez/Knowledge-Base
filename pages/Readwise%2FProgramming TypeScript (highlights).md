title:: Readwise/Programming TypeScript (highlights)
deck:: [[O'Reilly-Learning::Programming TypeScript]]
author:: [[Boris Cherny]]
full-title:: "Programming TypeScript"
category:: #books

tags:: cloud O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Friday, 03-02-2023]]
	- -
		- Supplemental material (code examples, exercises, etc.) is available for download at [*https://github.com/bcherny/programming-typescript-answers*](https://github.com/bcherny/programming-typescript-answers). #flashcard
		  id:: 2f32753a-9581-4a72-bdbc-0af2ed2ed7cb
		- ([View Highlight](https://read.readwise.io/read/01gr8sg2dt0vb40tjwmd9sfp3p))
	- -
	- Chapter 1. Introduction
		- Chapter 2. TypeScript: A 10_000 Foot View
			- -
				- How does TypeScript compile the code? #flashcard
				  id:: a7de04ea-6046-4023-8a64-3a84968ea080
					- Let’s start broad: programs are files that contain a bunch of text written by you, the programmer. That text is parsed by a special program called a *compiler*, which transforms it into an *abstract syntax tree (AST)*, a data structure that ignores things like whitespace, comments, and where you stand on the tabs versus spaces debate. The compiler then converts that AST to a lower-level representation called *bytecode*. You can feed that bytecode into another program called a *runtime* to evaluate it and get a result. So when you run a program, what you’re really doing is telling the runtime to evaluate the bytecode generated by the compiler from the AST parsed from your source code. The details vary, but for most languages this is an accurate high-level view.
					  
					  Once again, the steps are:
					  
					  1.  Program is parsed into an AST.
					    
					  2.  AST is compiled to bytecode.
					    
					  3.  Bytecode is evaluated by the runtime.
					    
					  
					  Where TypeScript is special is that instead of compiling straight to bytecode, TypeScript compiles to… JavaScript code! You then run that JavaScript code like you normally would—in your browser, or with NodeJS, or by hand with a paper and pen (for anyone reading this after the machine uprising has begun).
					  
					  At this point you may be thinking: “Wait! In the last chapter you said TypeScript makes my code safer! When does that happen?”
					  
					  Great question. I actually skipped over a crucial step: after the TypeScript Compiler generates an AST for your program—but before it emits code—it *typechecks* your code.
				- ([View Highlight](https://read.readwise.io/read/01gr8t2ytgrg14dwqm9pq08n18))
			- -
			- -
				- ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/31439948/img-idm46320597968936-prts_0201.png)Figure 2-1. Compiling and running TypeScript
				  id:: 8d5baa35-4026-4ce5-9045-5c858746e662
				  
				  Steps 1–3 are done by TSC, and steps 4–6 are done by the JavaScript runtime that lives in your browser, NodeJS, or whatever JavaScript engine you’re using. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr8t6dr2vvsmd396ry7qwgf5))
			- -
			- -
				- In this process, steps 1–2 use your program’s types; step 3 does not. That’s worth reiterating: *when TSC compiles your code from TypeScript to JavaScript, it won’t look at your types*. That means your program’s types will never affect your program’s generated output, and are only used for typechecking. This feature makes it foolproof to play around with, update, and improve your program’s types, without risking breaking your application. #flashcard
				  id:: 6cb532ca-405e-4939-9595-41aae010fda9
				- ([View Highlight](https://read.readwise.io/read/01gr8t9ae4q9vn4gy8gr4fszzj))
			- -
			- -
				- About types in TypeScript #flashcard
				  id:: 115cfd1f-cead-4941-9d17-42b6dcdd3ab2
					- To explicitly signal to TypeScript what your types are, use annotations. Annotations take the form *value: type* and tell the typechecker, “Hey! You see this *value* here? Its type is *type*.” Let’s look at a few examples (the comments following each line are the actual types inferred by TypeScript):
					  
					    let
					  
					  And if you want TypeScript to infer your types for you, just leave them off and let TypeScript get to work:
					  
					    let
					  
					  Right away, you’ll notice how good TypeScript is at inferring types for you. If you leave off the annotations, the types are the same! Throughout this book, we will use annotations only when necessary, and let TypeScript work its inference magic for us whenever possible.
				- ([View Highlight](https://read.readwise.io/read/01gr8v282971k5cmbmb41v2eeb))
			- -
			- -
				- Table 2-1. Comparing JavaScript’s and TypeScript’s type systems
				  id:: 07aec987-097c-4319-b153-923b40d751c3
				  
				  Type system feature
				  
				  JavaScript
				  
				  TypeScript
				  
				  **How are types bound?**
				  
				  Dynamically
				  
				  Statically
				  
				  **Are types automatically converted?**
				  
				  Yes
				  
				  No (mostly)
				  
				  **When are types checked?**
				  
				  At runtime
				  
				  At compile time
				  
				  **When are errors surfaced?**
				  
				  At runtime (mostly)
				  
				  At compile time (mostly) #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr8v6h6257sch1bbx0ygj3sr))
			- -
			- -
				- Dynamic type binding means that JavaScript needs to actually run your program to know the types of things in it. JavaScript doesn’t know your types before running your program.
				  id:: fa4c91bb-4aac-41a0-bc24-39604d760417
				  
				  TypeScript is a *gradually typed* language. That means that TypeScript works best when it knows the types of everything in your program at compile time, but it doesn’t have to know every type in order to compile your program. Even in an untyped program TypeScript can infer some types for you and catch some mistakes, but without knowing the types for everything, it will let a lot of mistakes slip through to your users.
				  
				  This gradual typing is really useful for migrating legacy codebases from untyped JavaScript to typed TypeScript (more on that in [“Gradually Migrating from JavaScript to TypeScript”](#migrating-to-typescript)), but unless you’re in the middle of migrating your codebase, you should aim for 100% type coverage. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr8vac0j5t4184vds49egtee))
			- -
		- Chapter 3. All About Types
			- -
				- What is a type literal in TypeScript? #flashcard
				  id:: 70425ede-1ec0-4499-8ccb-f841e9f7350e
					- Type literal
					  
					  A type that represents a single value and nothing else.
				- ([View Highlight](https://read.readwise.io/read/01gr8ybpaypkavad4rq25sk4j6))
			- -
			- -
				- bigint
				  id:: 981fee15-084e-4719-8375-04b08a8970b1
				  
				  `bigint` is a newcomer to JavaScript and TypeScript: it lets you work with large integers without running into rounding errors. While the `number` type can only represent whole numbers up to 253, `bigint` can represent integers bigger than that too. The `bigint` type is the set of all BigInts, and supports things like addition (`+`), subtraction (`-`), multiplication (*), division (`/`), and comparison (`<`). Use it like this:
				  
				    let
				  
				  Like with `boolean` and `number`, there are four ways to declare bigints. Try to let TypeScript infer your bigint’s type when you can.
				  
				  Warning
				  
				  At the time of writing, `bigint` is not yet natively supported by every JavaScript engine. If your application relies on `bigint`, be careful to check whether or not it’s supported by your target platform. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr8ym0hm2nnkk62wepg2vwc2))
			- -
			- -
				- How exactly do we specify in TypeScript the type of a variable?
				  id:: 2e60187f-7613-402f-b859-c5f73b8c3341
				  With `var: type`. #flashcard
					- `let` `a` `=` `'hello'` `// string` `var` `b` `=` `'billy'` `// string` `const` `c` `=` `'!'` `// '!'` `let` `d` `=` `a` `+` `' '` `+` `b` `+` `c` `// string` `let` `e`: `string` `=` `'zoom'` `// string` `let` `f``:` `'john'` `=` `'john'` `// 'john'` `let` `g``:` `'john'` `=` `'zoe'` `// Error TS2322: Type "zoe" is not assignable` `// to type "john".`
				- tags:: [[testing]]
				- ([View Highlight](https://read.readwise.io/read/01gr8yqggd5w9cmtds83xre69n))
			- -
			- -
				- symbol
				  id:: c167015c-ddcb-4481-9c33-2d1f3a3e0683
				  
				  `symbol` is a relatively new language feature that arrived with one of the latest major JavaScript revisions (ES2015). Symbols don’t come up often in practice; they are used as an alternative to string keys in objects and maps, in places where you want to be extra sure that people are using the right well-known key and didn’t accidentally set the key—think setting a default iterator for your object (`Symbol.iterator`), or overriding at runtime whether or not your object is an instance of something (`Symbol.hasInstance`). Symbols have the type `symbol`, and there isn’t all that much you can do with them:
				  
				    let #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr8zg1zr2y3f8ecqhbtejpa0))
			- -
			- -
				- About duck typing #flashcard
				  id:: 5ae02c69-db7f-443a-9401-b9b2f495b1ea
					- JavaScript is generally *structurally typed*, so TypeScript favors that style of programming over a *nominally typed* style.
					  
					  Structural typing
					  
					  A style of programming where you just care that an object has certain properties, and not what its name is (nominal typing). Also called *duck typing* in some languages (or, not judging a book by its cover).
				- ([View Highlight](https://read.readwise.io/read/01gr8zsjyr57cvtt28b1j57na9))
			- -
			- -
				- Example of a class in Typescript #flashcard
				  id:: 78046a66-21d4-43f4-8d9e-70f1a050070e
					- let
					  
					  `{firstName: string, lastName: string}` describes the *shape* of an object, and both the object literal and the class instance from the last example satisfy that shape, so TypeScript lets us assign a `Person` to `c`.
				- tags:: [[code]]
				- ([View Highlight](https://read.readwise.io/read/01gr9019sdpd3qqhqtk6ppbyda))
			- -
			- -
				- What `[key: T] : U` means in TypeScript? #flashcard
				  id:: c69662b4-4c72-4e54-8fe1-6c0e182b1621
					- Index Signatures
					  
					  The `[key: T]: U` syntax is called an *index signature*, and this is the way you tell TypeScript that the given object might contain more keys. The way to read it is, “For this object, all keys of type `T` must have values of type `U`.” Index signatures let you safely add more keys to an object, in addition to any keys that you explicitly declared.
					  
					  There is one rule to keep in mind for index signatures: the index signature key’s type (`T`) must be assignable to either `number` or `string`
				- ([View Highlight](https://read.readwise.io/read/01gr90ebmvsx5aapbgn52x21xq))
			- -
			- -
				- How do you declare objects in TypeScript? #flashcard
				  id:: 92114ae7-bcd7-43c7-a767-bd690d263367
					- To summarize, there are four ways to declare objects in TypeScript:
					  
					  1.  Object literal notation (like `{a: string}`), also called a *shape*. Use this when you know which fields your object could have, or when all of your object’s values will have the same type.
					    
					  2.  Empty object literal notation (`{}`). Try to avoid this.
					    
					  3.  The `object` type. Use this when you just want an object, and don’t care about which fields it has.
					    
					  4.  The `Object` type. Try to avoid this.
					    
					  
					  In your TypeScript programs, you should almost always stick to the first way and the third way. Be careful to avoid the second and fourth ways—use a linter to warn about them, complain about them in code reviews, print posters—use your team’s preferred tool to keep them far away from your codebase.
				- ([View Highlight](https://read.readwise.io/read/01gr90xgqhhb159p1kpm915tym))
			- -
			- -
				- Explain the type aliases in Typescript #flashcard
				  id:: 360847f1-eef2-4e33-b48c-15fac40e6f8a
					- Type aliases
					  
					  Just like you can use variable declarations (`let`, `const`, and `var`) to declare a variable that aliases a value, you can declare a type alias that points to a type. It looks like this:
					  
					    type
					  
					  `Age` is but a `number`. It can also help make the definition of the `Person` shape easier to understand.
				- ([View Highlight](https://read.readwise.io/read/01gr914znh94xtsbjpb4e0zrdp))
			- -
			- -
				- ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/31439948/img-idm46320586999832-prts_0302.png)Figure 3-2. Union (|) and intersection (& #flashcard
				  id:: 6d8cf1b0-9297-487c-b0d8-54d9433870ab
				- ([View Highlight](https://read.readwise.io/read/01gr91cvgs5tgmpftb41qkryyw))
			- -
			- -
				- About tuples in Typescript #flashcard
				  id:: 13d5eb15-54fd-43b3-b919-1e08fc0cc047
					- Tuples
					  
					  Tuples are subtypes of `array`. They’re a special way to type arrays that have fixed lengths, where the values at each index have specific, known types. Unlike most other types, tuples have to be explicitly typed when you declare them. That’s because the JavaScript syntax is the same for tuples and arrays (both use square brackets), and TypeScript already has rules for inferring array types from square brackets:
					  
					    let
				- ([View Highlight](https://read.readwise.io/read/01gr923r9p346hdpc2ef83mj0m))
			- -
			- -
				- About indefinitely arguments in Typescript #flashcard
				  id:: a78bc560-cb49-4b7a-a54e-6083611d0505
					- Tuples also support rest elements, which you can use to type tuples with minimum lengths:
					  
					    // A list of strings with at least 1 element
				- ([View Highlight](https://read.readwise.io/read/01gr92c4rc7snxye7knj5tfj38))
			- -
- New highlights added [[Friday, 03-02-2023]] at 11:00 AM
	- -
		- TypeScript comes with a `readonly` array type out of the box, which you can use to create immutable arrays. Read-only arrays are just like regular arrays, but you can’t update them in place. To create a read-only array, use an explicit type annotation; to update a read-only array, use nonmutating methods like `.concat` and `.slice` instead of mutating ones like `.push` and `.splice`:
		  id:: 63de231a-a54f-46a6-a865-e29ad8cf3066
		  
		    let #flashcard
		- ([View Highlight](https://read.readwise.io/read/01grb8b0hejnvhfkwaw10kahy8))
	- -
	- -
		- Enums
		  id:: 63de231a-7057-4fad-b425-1fcc2f069e8f
		  
		  Enums are a way to *enumerate* the possible values for a type. They are unordered data structures that map keys to values. Think of them like objects where the keys are fixed at compile time, so TypeScript can check that the given key actually exists when you access it.
		  
		  There are two kinds of enums: enums that map from strings to strings, and enums that map from strings to numbers. They look like this:
		  
		    enum
		  
		  Note
		  
		  By convention, enum names are uppercase and singular. Their keys are also uppercase.
		  
		  TypeScript will automatically infer a number as the value for each member of your enum, but you can also set values explicitly. Let’s make explicit what TypeScript inferred in the previous example:
		  
		    enum
		  
		  To retrieve a value from an enum, you access it with either dot or bracket notation—just like you would to get a value from a regular object:
		  
		    let #flashcard
		- ([View Highlight](https://read.readwise.io/read/01grb8psgav0j0vmwdhmqs31r2))
	- -
	- Chapter 4. Functions
		- -
			- Example of a function in TypeScript #flashcard
			  id:: 63de231a-22e7-44c3-8ab3-607e91f20b94
				- `function` `add``(``a`: `number``,` `b`: `number``)``:` `number` `{` `return` `a` `+` `b` `}`
			- ([View Highlight](https://read.readwise.io/read/01grb9pgaf4sk84gg9h6tz688y))
		- -
		- -
			- More examples of functions in TypeScript #flashcard
			  id:: 63de231a-1f14-41e2-b7d6-ddda1c67aebe
				- `// Named function` `function` `greet``(``name`: `string``)` `{` `return` `'hello '` `+` `name` `}` `// Function expression` `let` `greet2` `=` `function``(``name`: `string``)` `{` `return` `'hello '` `+` `name` `}` `// Arrow function expression` `let` `greet3` `=` `(``name`: `string``)` `=>` `{` `return` `'hello '` `+` `name` `}` `// Shorthand arrow function expression` `let` `greet4` `=` `(``name`: `string``)` `=>` `'hello '` `+` `name` `// Function constructor` `let` `greet5` `=` `new` `Function``(``'name'``,` `'return "hello " + name'``)`
			- ([View Highlight](https://read.readwise.io/read/01grb9wygzyjvs3nda54rw6pjz))
		- -
		- -
			- Like in object and tuple types, you can use `?` to mark parameters as optional. When declaring your function’s parameters, required parameters have to come first, followed by optional parameters:
			  id:: 63de231a-1c44-4b77-9384-66ca8706f6ec
			  
			    function #flashcard
			- ([View Highlight](https://read.readwise.io/read/01grba34s0cj1qn16ejcvn54b0))
		- -
		- -
			- Like in JavaScript, you can provide default values for optional parameters. Semantically it’s similar to making a parameter optional, in that callers no longer have to pass it in (a difference is that default parameters don’t have to be at the end of your list of parameters, while optional parameters do).
			  id:: 63de231a-c29e-4fc6-a809-3a1d8d95be64
			  
			  For example, we can rewrite `log` as:
			  
			    function #flashcard
			- ([View Highlight](https://read.readwise.io/read/01grba3sprqwaak6mj0r76jr1e))
		- -
		- -
			- How can you pass an undefined number of parameters to a function in TypeScript #flashcard
			  id:: 63de231a-f1d3-4aa9-9d97-31a8cc661b6a
				- we can instead use rest parameters to safely make our `sum` function accept any number of arguments:
				  
				    function
			- ([View Highlight](https://read.readwise.io/read/01grbad7vte39scbc2sg4sy03m))
		- -
- New highlights added [[Friday, 03-02-2023]] at 3:29 PM
	- -
		- The function type syntax we used in the last section—`type Fn = (...) => ...`—is a *shorthand call signature*. We can instead write it out more explicitly. Again taking the example of `Log`:
		  id:: 63de231a-2b6c-4765-9ee0-663ba34a0bb4
		  
		    // Shorthand call signature
		  
		  The two are completely equivalent in every way, and differ only in syntax. #flashcard
		- ([View Highlight](https://read.readwise.io/read/01grbp8ja7v85w3fygnh607zav))
	- -