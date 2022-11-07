title:: IBM Professional Certificate of DevOps and Software Engineering/Python for Data Science, AI & Development/Week 4
tags:: Coursera, DevOps, Python
deck:: [[IBM-DevOps::Python for Data Science]]

-
- #tags #Coursera #DevOps #python
-
- ## Reading & Writing Files with Open
	- ### Reading Files with Open #flashcard
	  id:: 634545b3-f9bf-46ec-a377-41a578b68767
		- ![image.png](../assets/image_1665321413818_0.png)
		- #### Modes of opening a file in Python
			- **r** --> for reading
			- **w** --> for writing
			- **a** --> appending
		-
		- But is recommended to use `with open() as var:`
			- ![image.png](../assets/image_1665321709102_0.png)
		- Also, you can use `myfile.readlines()`
		-
		- ![image.png](../assets/image_1665321819028_0.png)
	-
	- ---
	-
	- ### Writing Files with Open #flashcard
	  id:: 634545b3-4abc-4b18-8c48-ee02f3ccb5b5
		- We can use the `.write()` method to write to a file
		- The option **w** will overwrite the file if it already exists
		- The option **a** will append our contents
		- The option **r+** is for reading and writing.
		- The option **w+** is also for reading and writing. Truncates the pre-existing file content.
		- The option **a+** is for appending and reading. Creates a new file if not exists.
		-
		- To work with a file on existing data, use **r+** and **a+**.
			- If using **r+** (read and write), it's a good idea to call the `.truncate()` method to not use more space than needed.
			- This will reduce the file to your data and delete everything that follows (if not using `.truncate()` after a `.write()` followed by `.read()`).
		- It's important to use `file.truncate()` when dealing with files in Python in read and write `r+`
-
- ## Pandas
	- ### Loading Data with Pandas
		- We use it with `import pandas (as pd)`
		- `pd.read_csv(csv_path)`
	- ### Pandas: Working with and Saving Data #flashcard
	  id:: 634545b3-0cc2-4713-99e1-93633b54cad1
		- **Pandas** is a popular library for data analysis built on top of the Python programming language. Pandas generally provide two data structures for manipulating data, They are:
			- DataFrame
				- A **DataFrame** is a two-dimensional data structure, i.e., data is aligned in a tabular fashion in rows and columns.
				- A Pandas DataFrame will be created by loading the datasets from existing storage.
				- Storage can be SQL Database, CSV file, an Excel file, etc.
				- It can also be created from the lists, dictionary, and from a list of dictionaries.
			- Series
				- **Series** represents a one-dimensional array of indexed data.
				  It has two main components :
				- An array of actual data.
				- An associated array of indexes or data labels.
		- We create a DataFrame by:
			- `dataframe = pandas.DataFrame(<source>)`
	- When you pass the dataFrame an array, you are passing it just the array of headers of the column that you want to retrieve. #flashcard #dev-notes
	  id:: 634545b3-dea6-475b-a720-ff6261fd7b0a
		- **NOTE:** If you want DataFrame, use double brackets.
			- If you want a Series, use single brackets. For example:
		- `print(dataFrame [['ID']] )`
		- `print(dataFrame [['ID', 'Name', 'Surname']] )`
		- `print(dataFrame ['Name'])`
		-
	- ### loc[,] and iloc[,] functions #flashcard
	  id:: 634545b3-8a85-4602-b267-c4c449d7b934
		- `loc[,]` is a label-based data selecting method that recieves the name of the row or column.
		- `iloc[,]` is an indexed-based selecting method that receives the integer index of a specific row or column.
		- **Both deal with data, not with headers.**
		- You can label-index a column by calling `df.set_index('column')`
		- You must use the label-index as excluded to count indexes
		- The bounds of slicing with loc[] are inclusive, as dealing with labels, not indexes.
	-
	-
- ## Numpy in Python
	- ### One Dimensional Numpy
		- In Numpy, all the elements of a list are of the same type
		- `a = numpy.array([0, 1, 2, 3, 4])`
		- To sum or substract arrays, just use `+` or `-`.
		- To multiply use `*` for scalars and between arrays also.
		- For the dot product, do `result = numpy.dot(u,v)`
		- For adding a constant, `z = u + 1`
		-
	- ### Two Dimensional Numpy
		-
		-
		-
-
	-
- ## Flaschards
	- ¿Cómo puedes crear un DataFrame en Pandas que contenga solo los datos de 'Nombre' y 'Apellidos'?, ¿y un Series de Pandas? #flashcard
	  id:: 634545b3-30a4-403d-8e9e-337ec9b6f3c3
		- Con: `df = pandas.dataFrame(<source>)`
		- `answer = df[['Nombre', 'Apellidos']]`
		- Con un Series: `answer = df['Nombre', 'Apellidos']`
	- ¿Cómo puedes mostrar solo las dos primeras líneas y las columnas desde la 2 hasta la 5 de un dataFrame (ya inicializado)? #flashcard
	  id:: 634545b3-821d-4509-a0ac-db0a71258e3e
		- Con iloc(), `df.iloc[0:2, 1:5] # Interval opened on the right`
		- Con loc(), `df.loc['label1': 'label2', 'col_2': 'col_5']`
	- ¿Con qué función puedes obtener valores a través de índices y labels de un dataFrame de Pandas? #flashcard
	  id:: 634545b3-0693-4dfc-8276-35e61dd3d801
		- Con `df.loc[ , ]` y `df.iloc[ , ]`
	-
		-