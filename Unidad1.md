# <p align="center"><strong>🧩 ***Unidad 1*** 🧩</strong></p>


##    <p align="center"><strong>🔀 ***Aprendizaje autónomo:***</strong></p>
###   🟢 Ejemplo 1: Sistema de Biblioteca:
💡 Descripción: 

Una biblioteca registra libros y autores. Un libro puede tener varios autores y un autor varios libros. Los socios toman libros prestados; de cada préstamo interesan la fecha de retiro y la de devolución.

####   🖥️ Diagrama Entidad-Relación:
<img width="865" height="630" alt="image" src="https://github.com/user-attachments/assets/a21380ef-0c6b-47b0-971c-69a1869eb7dd" />

####   🗺️ Modelo Relacional:
<img width="693" height="903" alt="image" src="https://github.com/user-attachments/assets/47e46617-6be2-4da9-8ef1-a4ecf6f29cc1" />

####   📋 Codigo SQL:
```SQL
CREATE DATABASE ejercicio01_biblioteca;
USE ej1_biblioteca;

CREATE TABLE Autor (
    id_autor INT PRIMARY KEY,
    nombre   VARCHAR(50) NOT NULL
);

CREATE TABLE Libro (
    id_libro INT PRIMARY KEY,
    titulo   VARCHAR(100) NOT NULL
);

CREATE TABLE Escrito (
    id_libro INT NOT NULL,
    id_autor INT NOT NULL,
    PRIMARY KEY (id_libro, id_autor),
    FOREIGN KEY (id_libro) REFERENCES Libro (id_libro),
    FOREIGN KEY (id_autor) REFERENCES Autor (id_autor)
);

CREATE TABLE Socio (
    id_socio INT PRIMARY KEY,
    nombre   VARCHAR(50) NOT NULL
);

CREATE TABLE Prestamo (
    id_libro         INT  NOT NULL,
    id_socio         INT  NOT NULL,
    fecha_retiro     DATE NOT NULL,
    fecha_devolucion DATE,
    PRIMARY KEY (id_libro, id_socio),
    FOREIGN KEY (id_libro) REFERENCES Libro (id_libro),
    FOREIGN KEY (id_socio) REFERENCES Socio (id_socio)
);
```


---
###   🔵 Ejemplo 2: Pedidos de Restaurante:
💡 Descripción: 

Los clientes realizan pedidos que contienen varios platos con distinta cantidad. Los platos se agrupan en categorías. Cada pedido lo atiende un único mesero. El precio del plato debe registrarse tal como estaba al momento del pedido, aunque luego cambie.

####   🖥️ Diagrama Entidad-Relación:
<img width="1208" height="644" alt="image" src="https://github.com/user-attachments/assets/cb724d02-852d-4495-ae12-c5b48c23e88b" />

####   🗺️ Modelo Relacional:
<img width="692" height="923" alt="image" src="https://github.com/user-attachments/assets/bf0898f5-ee0b-41bd-ad54-67ed7009aada" />

####   📋 Codigo SQL:
```SQL
CREATE DATABASE ejercicio02_restaurante;
USE ej2_restaurante;

CREATE TABLE Cliente (
    id_cliente INT PRIMARY KEY,
    nombre     VARCHAR(50) NOT NULL
);

CREATE TABLE Mesero (
    id_mesero INT PRIMARY KEY,
    nombre    VARCHAR(50) NOT NULL
);

CREATE TABLE Pedido (
    id_pedido  INT PRIMARY KEY,
    id_cliente INT NOT NULL,
    id_mesero  INT NOT NULL,
    FOREIGN KEY (id_cliente) REFERENCES Cliente (id_cliente),
    FOREIGN KEY (id_mesero)  REFERENCES Mesero (id_mesero)
);

CREATE TABLE Categoria (
    id_categoria INT PRIMARY KEY,
    nombre       VARCHAR(30) NOT NULL
);

CREATE TABLE Plato (
    id_plato     INT PRIMARY KEY,
    nombre       VARCHAR(30) NOT NULL,
    precio       DECIMAL(8,2) NOT NULL,
    id_categoria INT NOT NULL,
    FOREIGN KEY (id_categoria) REFERENCES Categoria (id_categoria)
);

CREATE TABLE Detalle_pedido (
    id_pedido       INT NOT NULL,
    id_plato        INT NOT NULL,
    cantidad        INT NOT NULL,
    precio_unitario DECIMAL(8,2) NOT NULL,
    PRIMARY KEY (id_pedido, id_plato),
    FOREIGN KEY (id_pedido) REFERENCES Pedido (id_pedido),
    FOREIGN KEY (id_plato)  REFERENCES Plato (id_plato)
);
```



---
###   🟡 Ejemplo 3: Clínica Médica:
💡 Descripción: 

Los pacientes solicitan citas; cada cita la atiende un médico a un paciente en fecha, hora y consultorio. De algunas citas se genera una receta que incluye medicamentos con dosis y duración. Cada médico pertenece a una especialidad.

####   🖥️ Diagrama Entidad-Relación:
<img width="1202" height="669" alt="image" src="https://github.com/user-attachments/assets/56105f83-c648-4295-a6d8-09613bcad5db" />

####   🗺️ Modelo Relacional:
<img width="970" height="1318" alt="image" src="https://github.com/user-attachments/assets/85aaf4b5-f6dc-4844-acdb-443dcad0fd83" />

####   📋 Codigo SQL:
```SQL
CREATE DATABASE ej3_clinica;
USE ej3_clinica;

CREATE TABLE Especialidad (
    id_especialidad INT PRIMARY KEY,
    nombre          VARCHAR(30) NOT NULL
);

CREATE TABLE Medico (
    id_medico       INT PRIMARY KEY,
    nombre          VARCHAR(50) NOT NULL,
    id_especialidad INT NOT NULL,
    FOREIGN KEY (id_especialidad) REFERENCES Especialidad (id_especialidad)
);

CREATE TABLE Paciente (
    id_paciente INT PRIMARY KEY,
    nombre      VARCHAR(50) NOT NULL
);

CREATE TABLE Cita (
    id_cita     INT PRIMARY KEY,
    fecha       DATE NOT NULL,
    hora        TIME NOT NULL,
    consultorio VARCHAR(20) NOT NULL,
    id_paciente INT NOT NULL,
    id_medico   INT NOT NULL,
    FOREIGN KEY (id_paciente) REFERENCES Paciente (id_paciente),
    FOREIGN KEY (id_medico)   REFERENCES Medico (id_medico)
);

CREATE TABLE Receta (
    id_receta INT PRIMARY KEY,
    dosis     VARCHAR(30) NOT NULL,
    duracion  VARCHAR(15)  NOT NULL,
    id_cita   INT NOT NULL UNIQUE,
    FOREIGN KEY (id_cita) REFERENCES Cita (id_cita)
);

CREATE TABLE Medicamento (
    id_medicamento INT PRIMARY KEY,
    nombre         VARCHAR(15) NOT NULL
);

CREATE TABLE Incluye (
    id_receta      INT NOT NULL,
    id_medicamento INT NOT NULL,
    PRIMARY KEY (id_receta, id_medicamento),
    FOREIGN KEY (id_receta)      REFERENCES Receta (id_receta),
    FOREIGN KEY (id_medicamento) REFERENCES Medicamento (id_medicamento)
);

```



---
###   🟢 Ejemplo 4: Sistema de Aerolínea:
💡 Descripción: 

Una aerolínea opera vuelos (cada uno con número, fecha, origen y destino), cada vuelo lo realiza un avión. Los pasajeros realizan reservas para un vuelo específico, indicando asiento y tarifa pagada en el momento de la reserva.

####   🖥️ Diagrama Entidad-Relación:
<img width="1409" height="560" alt="image" src="https://github.com/user-attachments/assets/ee260e5f-38b7-498f-ad94-24c8d644c5e6" />

####   🗺️ Modelo Relacional:
<img width="1006" height="1007" alt="image" src="https://github.com/user-attachments/assets/3641763b-fb5b-48fd-bfe0-718d9d781d7d" />

####   📋 Codigo SQL:
```SQL

```



---
###   🔵 Ejercicio 5: Empresa Discográfica:
💡 Descripción: 

Una empresa discográfica necesita modelar los datos sobre sus diferentes recursos según las siguientes características:

🔹 Manager: de cada mánager se almacena un identificador de manager y su nombre. Un manager representa a una serie de artistas.

🔹 Artista: un artista es representado por un manager. De los artistas se almacena su nombre completo (usando un único atributo) y su NIF.

🔹 Evento de promoción: los artistas participan en eventos de promoción para dar a conocer sus trabajos. En un evento de promoción pueden participar varios artistas. De un evento se almacena un identificador único, la fecha de celebración y el número de asistentes.


####   🖥️ Diagrama Entidad-Relación:
<img width="1349" height="352" alt="image" src="https://github.com/user-attachments/assets/5bd405b3-2cf6-400b-9322-0c976f3440a1" />

####   🗺️ Modelo Relacional:
<img width="1079" height="837" alt="image" src="https://github.com/user-attachments/assets/e33acbd3-f82e-4982-a6f6-359aa8a313a4" />

####   📋 Codigo SQL:
```SQL

```



---
###   🟡 Ejercicio 6: Tienda Informática:
💡 Descripción: 

Se desea crear una aplicación para la gestión de una tienda informática. La tienda dispone de una serie de productos que se venden a los clientes. De cada producto informático se desea guardar el código, descripción, precio y número de existencias. De cada cliente se desea guardar el código, nombre, apellidos, dirección y número telefónico. Un cliente puede comprar varios productos en la tienda y un mismo producto puede ser comprado por varios clientes. Cada vez que se compre un artículo quedará registrada la compra en la base de datos junto con la fecha en la que se compró el artículo. La tienda tiene contactos con varios proveedores que son los que suministran los productos. Un mismo producto puede ser suministrado por varios proveedores. De cada proveedor se desea guardar el código, nombres, apellidos, dirección, provincia y número de teléfono.

####   🖥️ Diagrama Entidad-Relación:
<img width="1859" height="366" alt="image" src="https://github.com/user-attachments/assets/f0ef1899-d412-4928-9bcd-ca65735a144f" />

####   🗺️ Modelo Relacional:
<img width="1001" height="1083" alt="image" src="https://github.com/user-attachments/assets/d0d7ed61-10f1-42b8-ac06-68a2612fbe52" />

####   📋 Codigo SQL:
```SQL

```



---
###   🟢 Ejercicio 7: Discos Musicales:
💡 Descripción:

🔹 La tienda vende discos de diferentes géneros musicales y cantantes

🔹 Cada género musical tiene un identificador

🔹 Cada disco tiene título, género musical, precio y cantante

🔹 De un cantante se registra el nombre y su país, Todo disco pertenece a un cantante y un cantante puede tener muchos discos. Además, un disco tiene un conjunto de canciones (identificador y título)

🔹 Un disco tiene muchas canciones y una canción puede estar en varios discos. Interesa conocer la posición de una canción en un determinado disco


####   🖥️ Diagrama Entidad-Relación:
<img width="1579" height="670" alt="image" src="https://github.com/user-attachments/assets/7b19d096-db7f-4ebb-ae77-cd370e65425e" />

####   🗺️ Modelo Relacional:
<img width="999" height="1307" alt="image" src="https://github.com/user-attachments/assets/c44b3140-8c15-431a-af60-d47bb850bc7f" />

####   📋 Codigo SQL:
```SQL

```



---
###   🔵 Ejercicio 8: Camiones:
💡 Descripción: 

Se desea informatizar la gestión de una empresa de transporte que reparte paquetes por toda España. Los encargados de llevar los paquetes son los camioneros, de los que se quiere guardar la cédula, nombre, teléfono, dirección, salario y población en que vive. De los paquetes transportados interesa conocer el código del paquete, descripción, destinatario y dirección del destinatario.

Un camionero distribuye muchos paquetes, y un paquete sólo puede ser distribuido por un camionero. De las provincias a las que llegan los paquetes interesa guardar el código de provincia y el nombre. Un paquete sólo puede llegar a una provincia. Sin embargo, a una provincia pueden llegar varios paquetes.

De los camiones que llevan los camioneros, interesa conocer la matrícula, modelo, tipo y potencia. Un camionero puede conducir diferentes camiones en fechas diferentes, y un camión puede ser conducido por varios camioneros.


####   🖥️ Diagrama Entidad-Relación:
<img width="1245" height="834" alt="image" src="https://github.com/user-attachments/assets/5b3e415d-1636-43c0-87e3-94223a868308" />

####   🗺️ Modelo Relacional:
<img width="1110" height="906" alt="image" src="https://github.com/user-attachments/assets/f054c39b-b983-4594-a91d-a68e18080805" />

####   📋 Codigo SQL:



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


####   🖥️ Diagrama Entidad-Relación:
<img width="1328" height="751" alt="image" src="https://github.com/user-attachments/assets/e468d47c-cc4b-4175-917d-94f9a2ce92b1" />

####   🗺️ Modelo Relacional:
<img width="1040" height="1762" alt="image" src="https://github.com/user-attachments/assets/2e5954f4-c114-43ac-946e-e2061743a083" />

####   📋 Codigo SQL:
```SQL

```



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




