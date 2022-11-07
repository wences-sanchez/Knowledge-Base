- ## Cosas que he aprendido hoy
- Para convertir una cadena de texto a un array, podemos usar: #flashcard #Bash #dev-notes
  id:: 63454580-bfc6-4e5e-811b-f9fde6dd263b
	- `$ echo $myArray | grep -o .`
	- > grep --help
	  > -o, --only-matching       show only nonempty parts of lines that match
- Para saber la longitud de un array en Bash, hacemos: #flashcard #Bash #dev-notes
  id:: 63454580-238d-4841-b215-05b717c80df5
	- `${#my_array[@]}`
- Para iterar en un bucle con los índices de un array, usar: #flashcard #Bash #dev-notes
  id:: 63454580-39b6-43ba-824b-631abfceed08
	- `for i in "${!my_array[@]}"; do ...`
	      `echo "The index is $i and the element is ${my_array[$i]}"`
	  `done`
- Para comparar strings en Bash hay que usar: #flashcard #Bash #dev-notes
  id:: 63454580-9eac-4536-b37f-bc79702acf6b
	- $string1 **==** $string2 # or $string1 **!=** $string2
- ¿Cómo harías para obtener la longitud de un string en Bash? #flashcard #Bash #dev-notes
  id:: 63454580-7c23-44e6-9827-2bb9826c5927
	- Usando: `${#my_var}`