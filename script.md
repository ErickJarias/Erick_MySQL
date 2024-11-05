 ``` sql

CREATE DATABASE pizzame;

USE pizzame;

CREATE TABLE pais(
id INT,
nombre VARCHAR(20)
CONSTRAINT PK_pais_Id PRIMARY KEY(id);

CREATE TABLE sucursal(
id_sucursal INT(20),
nombre VARCHAR(30),
dirección VARCHAR(50),
ciudad VARCHAR(30),
CONSTRAINT PK_sucursal_Id PRIMARY KEY(id_sucursal)
);


CREATE TABLE clientes(
cliente_id INT PRIMARY KEY AUTO_INCREMENT,
nombre VARCHAR(50),
email VARCHAR(50) UNIQUE,
telefono VARCHAR(15),
direccion VARCHAR(100),
ciudad VARCHAR(50),
pais VARCHAR(50),
fecha_registro DATE
);
 
CREATE TABLE productos (
producto_id INT PRIMARY KEY AUTO_INCREMENT,
nombre VARCHAR(50),
categoria VARCHAR(50),
precio DECIMAL(10, 2),
stock INT
);


CREATE TABLE empleados (
empleado_id INT PRIMARY KEY AUTO_INCREMENT,
nombre VARCHAR(50),
puesto VARCHAR(50),
fecha_contratacion DATE,
salario DECIMAL(10, 2)
);


CREATE TABLE pedidos (
pedido_id INT PRIMARY KEY AUTO_INCREMENT,
cliente_id INT,
empleado_id INT,
fecha_pedido DATE,
estado VARCHAR(20),
FOREIGN KEY (cliente_id) REFERENCES clientes(cliente_id),
FOREIGN KEY (empleado_id) REFERENCES empleados(empleado_id)
);

CREATE TABLE detalles_pedidos (
detalle_id INT PRIMARY KEY AUTO_INCREMENT,
pedido_id INT,
producto_id INT,
cantidad INT,
precio_unitario DECIMAL(10, 2),
FOREIGN KEY (pedido_id) REFERENCES pedidos(pedido_id),
FOREIGN KEY (producto_id) REFERENCES productos(producto_id)
);

CREATE TABLE pizza(
id_pizza INT(20),
tamaño VARCHAR(50),
ingredientes VARCHAR(100),
cliente_id INT,
empleado_id INT,
estado VARCHAR(20),
FOREIGN KEY (cliente_id) REFERENCES clientes(cliente_id),
FOREIGN KEY (empleado_id) REFERENCES empleados(empleado_id)
);

CREATE TABLE panzarotti(
id_panzarotti INT,
tamaño VARCHAR(50),
id_ingredientes VARCHAR(100),
cliente_id INT,
empleado_id INT,
pedido_id INT,
estado VARCHAR(20),
FOREIGN KEY (cliente_id) REFERENCES clientes(cliente_id),
FOREIGN KEY (pedido_id) REFERENCES pedidos(pedido_id)
);
