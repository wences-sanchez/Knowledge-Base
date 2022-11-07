- ## Cosas que he aprendido hoy
- Para convertir una cadena de texto a un array, podemos usar: #flashcard #Bash #dev-notes
  id:: 6368c415-6e36-4df4-af1a-17312a9110ce
	- `$ echo $myArray | grep -o .`
	- > grep --help
	  > -o, --only-matching       show only nonempty parts of lines that match
- Para saber la longitud de un array en Bash, hacemos: #flashcard #Bash #dev-notes
  id:: 6368c415-c703-40f9-ac60-725989321806
	- `${#my_array[@]}`
- Para iterar en un bucle con los índices de un array, usar: #flashcard #Bash #dev-notes
  id:: 6368c415-1063-48f9-9fa0-d5a45526c32e
	- `for i in "${!my_array[@]}"; do ...`
	      `echo "The index is $i and the element is ${my_array[$i]}"`
	  `done`
- Para comparar strings en Bash hay que usar: #flashcard #Bash #dev-notes
  id:: 6368c415-af4a-40cf-bf78-d71290ddbae3
	- $string1 **==** $string2 # or $string1 **!=** $string2
- ¿Cómo harías para obtener la longitud de un string en Bash? #flashcard #Bash #dev-notes
  id:: 6368c415-59d9-4f3b-9ae8-1f6a28b306d3
	- Usando: `${#my_var}`