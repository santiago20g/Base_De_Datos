# <p align="center"><strong>🧩 ***Unidad 2*** 🧩</strong></p>


##    <p align="center"><strong>🔀 ***Aprendizaje autónomo:***</strong></p>
###   🟢 Ejemplo 1: Sistema de Biblioteca:
💡 Descripción: 

Una biblioteca registra libros y autores. Un libro puede tener varios autores y un autor varios libros. Los socios toman libros prestados; de cada préstamo interesan la fecha de retiro y la de devolución.

####   🖥️ Diagrama:
<img width="865" height="630" alt="image" src="https://github.com/user-attachments/assets/a21380ef-0c6b-47b0-971c-69a1869eb7dd" />




---
###   🔵 Ejemplo 2: Pedidos de Restaurante:
💡 Descripción: 

Los clientes realizan pedidos que contienen varios platos con distinta cantidad. Los platos se agrupan en categorías. Cada pedido lo atiende un único mesero. El precio del plato debe registrarse tal como estaba al momento del pedido, aunque luego cambie.

####   🖥️ Diagrama:
<img width="721" height="397" alt="image" src="https://github.com/user-attachments/assets/e842b2c3-772f-4bb2-afd0-d45e80167a00" />



---
###   🟡 Ejemplo 3: Clínica Médica:
💡 Descripción: 

Los pacientes solicitan citas; cada cita la atiende un médico a un paciente en fecha, hora y consultorio. De algunas citas se genera una receta que incluye medicamentos con dosis y duración. Cada médico pertenece a una especialidad.

####   🖥️ Diagrama:



---
###   🟢 Ejemplo 4: Sistema de Aerolínea:
💡 Descripción: 

Una aerolínea opera vuelos (cada uno con número, fecha, origen y destino), cada vuelo lo realiza un avión. Los pasajeros realizan reservas para un vuelo específico, indicando asiento y tarifa pagada en el momento de la reserva.

####   🖥️ Diagrama:



---
###   🔵 Ejercicio 5: Empresa Discográfica:
💡 Descripción: 

Una empresa discográfica necesita modelar los datos sobre sus diferentes recursos según las siguientes características:

🔹 Manager: de cada mánager se almacena un identificador de manager y su nombre. Un manager representa a una serie de artistas.

🔹 Artista: un artista es representado por un manager. De los artistas se almacena su nombre completo (usando un único atributo) y su NIF.

🔹 Evento de promoción: los artistas participan en eventos de promoción para dar a conocer sus trabajos. En un evento de promoción pueden participar varios artistas. De un evento se almacena un identificador único, la fecha de celebración y el número de asistentes.


####   🖥️ Diagrama:



---
###   🟡 Ejercicio 6: Tienda Informática:
💡 Descripción: 

Se desea crear una aplicación para la gestión de una tienda informática. La tienda dispone de una serie de productos que se venden a los clientes. De cada producto informático se desea guardar el código, descripción, precio y número de existencias. De cada cliente se desea guardar el código, nombre, apellidos, dirección y número telefónico. Un cliente puede comprar varios productos en la tienda y un mismo producto puede ser comprado por varios clientes. Cada vez que se compre un artículo quedará registrada la compra en la base de datos junto con la fecha en la que se compró el artículo. La tienda tiene contactos con varios proveedores que son los que suministran los productos. Un mismo producto puede ser suministrado por varios proveedores. De cada proveedor se desea guardar el código, nombres, apellidos, dirección, provincia y número de teléfono.

####   🖥️ Diagrama:



---
###   🟢 Ejercicio 7: Discos Musicales:
💡 Descripción:

🔹 La tienda vende discos de diferentes géneros musicales y cantantes

🔹 Cada género musical tiene un identificador

🔹 Cada disco tiene título, género musical, precio y cantante

🔹 De un cantante se registra el nombre y su país, Todo disco pertenece a un cantante y un cantante puede tener muchos discos. Además, un disco tiene un conjunto de canciones (identificador y título)

🔹 Un disco tiene muchas canciones y una canción puede estar en varios discos. Interesa conocer la posición de una canción en un determinado disco


####   🖥️ Diagrama:



---
###   🔵 Ejercicio 8: Camiones:
💡 Descripción: 

Se desea informatizar la gestión de una empresa de transporte que reparte paquetes por toda España. Los encargados de llevar los paquetes son los camioneros, de los que se quiere guardar la cédula, nombre, teléfono, dirección, salario y población en que vive. De los paquetes transportados interesa conocer el código del paquete, descripción, destinatario y dirección del destinatario.

Un camionero distribuye muchos paquetes, y un paquete sólo puede ser distribuido por un camionero. De las provincias a las que llegan los paquetes interesa guardar el código de provincia y el nombre. Un paquete sólo puede llegar a una provincia. Sin embargo, a una provincia pueden llegar varios paquetes.

De los camiones que llevan los camioneros, interesa conocer la matrícula, modelo, tipo y potencia. Un camionero puede conducir diferentes camiones en fechas diferentes, y un camión puede ser conducido por varios camioneros.


####   🖥️ Diagrama:



---
###   🟡 Ejercicio 9: Veterinaria:
💡 Descripción: 

🔹 Del propietario interesa: cédula, apellidos, nombres, dirección, teléfonos

🔹 De la mascota interesa: identificador, nombre, fecha de nacimiento, tipo

🔹 Un propietario puede llevar una o varias mascotas

🔹 Una mascota la lleva uno y solo un propietario

🔹 Del personal de la clínica veterinaria interesa un código, la cédula, nombre

🔹 Entre el personal de la clínica se distingue a los veterinarios y los auxiliares, pudiendo haber otros tipos
   - Del veterinario se guarda además su fecha_alta y especialidad
   - De los auxiliares interesa su base de cotización

🔹Las mascotas pasan consulta con los veterinarios. De manera que:
   - Un veterinario puede pasar consulta a ninguna o a varias mascotas, y una misma mascota de la clínica ha pasado consulta una o más veces en fechas diferentes con varios veterinarios.
   - AL pasar consulta se realiza un diagnóstico.

🔹 Cada propietario tiene un familiar de contacto para casos de emergencia.
   - De este familiar interesa la cédula, nombre y teléfono.
   - Si el propietario se da de alta en la clínica veterinaria, el familiar ya no interesa.
   - El familiar es contacto de un solo propietario


####   🖥️ Diagrama:



---
###   🟢 Ejercicio 10: Empresa:
💡 Descripción: 

La empresa necesita administrar sus departamentos, empleados, proyectos y el historial de salarios.

Cada empleado pertenece a un departamento y puede trabajar en varios proyectos. También existen empleados que supervisan a otros empleados. Se necesita registrar el historial salarial de cada empleado.

####   🖥️ Diagrama:



---
###   🔵 Ejercicio 11: Universidad :
💡 Descripción: 

Los alumnos se inscriben en cursos obteniendo una calificación por ciclo. Algunos cursos exigen haber aprobado otros cursos antes, e incluso exigen una nota mínima como prerrequisito.

####   🖥️ Diagrama:



---
###   🟡 12. :
💡 Descripción: 

####   🖥️ Diagrama:



---

##   📝 ***Reflexiones y Conclusiones***
###   📌 Conclusiones:
🔹 

🔹 

🔹 



###   💡 Reflexión crítica:

🔹 

🔹 

🔹 


---

###    <p align="center"><strong>[***Volver atrás***](Portafolio.md)</strong></p>




