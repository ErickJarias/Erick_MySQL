```mysql

INSERT INTO clientes (nombre, email, telefono, direccion, ciudad, pais,
fecha_registro) VALUES
('Andrés Ortega', 'andres.ortega@hotmail.com', '555-9876', 'Av. Buenavista 67',
'cucuta', 'colombia', '2022-07-14'),
('Laura Morales', 'laura.morales@hotmail.com', '555-3333', 'Calle Luna 8',
'Pamplona', 'colombia', '2023-01-11'),
('Iván Navarro', 'ivan.navarro@gmail.com', '555-2222', 'Av. del Rey 21',
'bucaramanga', 'colombia', '2022-02-05'),
('Daniel Ruiz', 'daniel.ruiz@yahoo.com', '555-4444', 'Calle Grande 99',
'cucuta', 'colombia', '2023-02-17'),
('Esther Blanco', 'esther.blanco@gmail.com', '555-1111', 'Av. Colón 3',
'Valledupar', 'colombia', '2022-10-20');

INSERT INTO empleados (nombre, puesto, fecha_contratacion, salario) VALUES
('Juan Díaz', 'Coordinadora de Logística', '2019-08-19', 3100.00),
('Juan Cruz', 'Asistente Administrativo', '2020-12-01', 1900.00),
('Daniel Rueda', 'Jefe de Compras', '2018-05-10', 3600.00),
('Miguel Angel', 'Consultor de Negocios', '2021-04-12', 2900.00),
('Rocío López', 'Especialista en Ventas', '2022-02-20', 2300.00),
('Andrés Navas', 'Desarrollador', '2021-12-13', 3100.00);


INSERT INTO pedidos (cliente_id, empleado_id, fecha_pedido, estado) VALUES
(1, 1, '2023-02-10', 'Completado'),
(2, 2, '2023-02-12', 'Pendiente'),
(3, 3, '2023-03-15', 'Cancelado'),
(4, 4, '2023-03-16', 'Completado'),
(5, 5, '2023-04-10', 'Pendiente'),
(6, 6, '2023-04-12', 'Completado'),
(7, 7, '2023-05-05', 'Pendiente'),
(8, 8, '2023-05-07', 'Pendiente'),
(9, 9, '2023-05-10', 'Completado');
