# <p align="center"><strong>🧩 ***Unidad 3*** 🧩</strong></p>


##    <p align="center"><strong>***Temas Vistos en la Unidad 3***</strong></p>

---

##    <p align="center"><strong>🔀 ***Modularidad:***</strong></p>
###   🟢 1. Pase de Parametros por Valor:
💡 Descripción: Cuando se pasa un parámetro por valor, lo que se envía a la función es una copia del dato original, esto significa que cualquier cambio que se haga dentro de la función no afecta al valor de la variable en el programa principal.

####   🔹 Ejemplo:
- ⚡ Se envían los valores de "a" y "b" a la función. Dentro de la función, "x" recibe una copia de "a", y "y" recibe una copia de "b".
- ⚡ Se necesita un auxiliar.

####   💻 Código en C:
<img width="1117" height="865" alt="image" src="https://github.com/user-attachments/assets/ab9a0954-64f0-48fc-b44e-67934fa74f77" />



---


###   🔵 2. Pase de Parametro por Referencia:
💡 Descripción: Cuando se pasa un parámetro por referencia, lo que se envía a la función es la dirección de memoria de la variable original, esto significa que la función trabaja directamente sobre la variable del programa principal, no sobre una copia, entonces si se hace un cambio dentro de la funcion si afecta a la varibale original.

####   🔹Ejemplo:
- ⚡ Los valores de "a = 3" y "b = 5" cambuian en la funcion. Cuando se imprimen en el Main se intercambian los valores.
- ⚡ Se usan operadores & "para enviar direcciones" y * "para acceder y modificar valores".

####   💻 Código en C: 
<img width="1117" height="863" alt="image" src="https://github.com/user-attachments/assets/b4f6c0ac-b801-4d6c-92b3-74cf3577e986" />



---
---


##    <p align="center"><strong>🗂️ ***Arreglos:***</strong></p>

###   🟢 1. Listas Unidimensionales "Vector":
💡 Descripción: Es una estructura de datos que permite almacenar varios elementos del mismo tipo en una sola variable. Los datos se organizan de forma lineal. Normalmente comienza la lista desde 0 hasta n datos

####  📋 Su estructura se ve asi:
<img width="440" height="109" alt="image" src="https://github.com/user-attachments/assets/e1cf3816-d581-44ec-9a49-5a7569523058" />

####   🔹Ejemplo:
- ⚡ La variable del vector se llama lista y tiene un tamaño de [5].
- ⚡ Se usa un For para optimizar la imprisión los datos del vector sin tener excesos de printf.
  
####   💻 Código en C:
<img width="1382" height="862" alt="image" src="https://github.com/user-attachments/assets/d6bd44c6-3f52-4305-913e-4ffc57245dc5" />



---


###   🔵 2. listas Bidimensionales "Matriz":
💡 Descripción: Es una estructura de datos que permite almacenar datos en dos dimensiones del mismo tipo en una sola variable, en filas y en columnas. El primer numero de la matriz representa las filas y el segundo las columnas m[i][j].

####  🔢 Su estructura se ve asi:
<img width="391" height="197" alt="image" src="https://github.com/user-attachments/assets/aea3295a-d5a6-4922-b5a3-a783f454dc23" />



####   🔹Ejemplo:
- ⚡ La variable del vector se llama matriz y tiene un tamaño de [3] [4].
- ⚡ Se usa un For para optimizar la imprisión los datos del vector sin tener excesos de printf.
  
####   💻 Código en C: 
<img width="1393" height="1275" alt="image" src="https://github.com/user-attachments/assets/de51695e-25db-42ed-bee3-9256003c9c2f" />



---


###   🟡 3. listas Tridimensionales "Matriz Tridimensional":
💡 Descripción: En lugar de organizar los datos en filas y columnas "2D", se organizan los datos en filas, columnas y profundidad "3D" del mismo tipo en una sola variable. El primer numero de la matriz representa la profundidad, el segundo las filas y el tercero las conlumnas, m[i][j][k].

####  🗂️ Su estructura se ve asi:
<img width="222" height="157" alt="image" src="https://github.com/user-attachments/assets/54cc0639-b30f-4e7a-9e4d-0cd657cc13b7" />

####   🔹Ejemplo:
- ⚡ La variable del vector se llama matriz y tiene un tamaño de [2] [3] [2].
- ⚡ Se usa un For para optimizar la imprisión los datos del vector sin tener excesos de printf.
  
####   💻 Código en C: 
<img width="1256" height="1778" alt="image" src="https://github.com/user-attachments/assets/42b7faeb-8b7d-4550-acd6-71bef3664cd7" />



---
---



##    <p align="center"><strong>📝 ***Actividades Realizadas en Toda la Unidad:*** </strong></p>

##    💻 ***APE - Aprendizaje Práctico Experimental***

###    1. Construcción de funciones y procedimientos en un lenguaje de programación: 
####  🔗 [Actividad APE 1](https://drive.google.com/file/d/1Yi1KxWn2n5VvgddqLNo1KZIsk0ur9fOz/view?usp=sharing)



###    2. Implementación de funciones utilizando el paso de parámetros por valor y por referencia: 
####  🔗 [Actividad APE 2](https://drive.google.com/file/d/1QQKu5XuYdsayHUz01Ds_1xJnhIuH7Mt9/view?usp=sharing)




---

##    💡***AA - Aprendizaje Autónomo***

###    1. Curso Fundamentos de Python 1. Computación UNL:
####  🔗 [Actividad AA 1](https://drive.google.com/file/d/1tmwndZAheQlX66LAPfo1f4CimQHROrT-/view?usp=sharing)



---
---

##   📌 ***Principales dificultades en la aplicación de los contenidos***
- ⚡ Dificultad en diferenciar los pases de parametro por `valor` y `referencia.`
- ⚡ Manejo de matrices tridimensionales.

---
---

##   📝 ***Reflexiones y Conclusiones***
###   📌 Conclusiones:
🔹 El paso de parametros por valor trabaja con copias, lo que protege las variables originales e impide que la función las modifique y el paso por referencia usa direcciones de memoria, permitiendo que la función altere directamente los valores originales. Entender esta diferencia es clave para controlar cómo se transmiten y manipulan datos en un programa.

🔹 Gracias a las matrices de 1 dimension, 2 dimesiones y 3 dimensiones se puede organizar información de manera ordenada y eficiente usando una sola variable.

🔹 Saber cuándo usar pase de parametros por valor o referencia, y cómo estructurar datos en listas o matrices, es esencial para realizar programas claros, eficientes.



###   💡 Reflexión crítica:

🔹 Usar paso de parametros por valor o por referencia cambia mucho el resultado obtenido, hay que saber cual necesitamos y tener cuidado al usarlo.

🔹 No siempre se debe usar matrices tridimensionales, a veces un vector simple es suficiente para usar estructuras complejas para realizar nuestro trabajo.

🔹 Las listas y matrices ayudan a organizar los datos de mejor manera, son formas prácticas de ordenar la información para resolver problemas, hay que tener en cuenta lo que vas a realizar en nustro programa para elegir las diferentes tipos de listas para hacer nuestro trabajo de manera adecuada y eficiente. 


---

###    <p align="center"><strong>[***Volver atrás***](Portafolio.md)</strong></p>




