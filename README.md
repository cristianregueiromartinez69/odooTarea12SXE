# operaciones sobre la base de datos de una instalación de odoo. 😄

**Índice** 😎

- Creación de la base de datos e instalación de módulos.
- Apartado 1 de la tarea.
- Apartado 2 de la tarea.
- Apartado 3 de la tarea.
- Apartado 4 de la tarea.
- Apartado 5 de la tarea.
- Apartado 6 de la tarea.
- Apartado 7 de la tarea.
- Apartado 8 de la tarea.
- problemas que hubo en la tarea.

### 1. Creación de la base de datos e instalación de módulos 🤗

Primero tenemos que leer el enunciado.
```bash
# Realiza una instalación limpia de una base de datos y marca la opción de “Demo data”.
 Posteriormente instala las aplicaciones de facturación y contactos
```

Para hacer eso, primero tenemos que tener instalado docker y tener los servicios requeridos para la tarea. Dejo aquí un enlace [aquí](https://github.com/cristianregueiromartinez69/Tarea_10_SXE) por si no lo tenéis.

Dicho esto, levantamos los servicios.
```bash
#nos posicionamos en el directorio donde está el docker-compose
sudo docker compose up
```

Nos vamos a un navegador e introducimos.

```bash
http://(ip de tu entorno de trabajo):8069
```

Introducimos la contraseña maestra y nos redirigirá aquí. 🙂

![creaciondb1](https://github.com/user-attachments/assets/136117ef-8e23-4168-aadc-3a48010ad71d)

Le damos a ***create database***.

![creaciondb2](https://github.com/user-attachments/assets/7362046d-6467-4f8c-9c52-e917447933ed)

Introducimos los datos como en la imagen anterior o los datos que quieras y le damos a ***continue***.

**Atención** 😱

Hay que activar la opción de demo data para el ejercicio.

Una vez hemos creado la base nos redirigirá a una ventana donde tenemos que poner el correo y la contraseña, las ponemos y nos mandará a odoo.

![creacioncontactosfacturas1](https://github.com/user-attachments/assets/315056ef-2efe-441b-a71f-f8b3395e53a4)

Ahora vamos a activar el módulo de facturas, para eso le damos click en **activar** aquí.

![creacioncontactosfacturas2](https://github.com/user-attachments/assets/aacd84bf-5bf7-4916-8220-6453a784785d)

Lo mismo para contactos.

![creacioncontactosfacturas3](https://github.com/user-attachments/assets/62dff3f7-ac7b-4781-8b2d-974943657536)



### 2. Apartado 1 de la tarea 🤗

Enunciado del apartado.

```bash
Mediante la herramienta PgAdmin u otro método que estimes oportuno, elabora y ejecuta una sentencia que cree una tabla llamada “EmpresasFCT“con los siguientes campos:
● idEmpresa: autonumérico. Este campo será la clave primaria.
● nombre: Texto con tamaño máximo de 40 caracteres. -useChatgpt: booleano, por defecto a true
● quiereAlumnos: Booleano.
● numAlumnos: número entero.
● fechaContacto: tipo fecha
```

Nos vamos a un navegador e introducimos en la url.

```bash
http://(ip de tu entorno de trabajo):5050
```
Nos mandará a PgAdmin donde ponemos el correo y la contraseña.

Tenemos que buscar la base de datos donde vamos a crear la tabla. La base es la que creamos en el apartado 1.
Una vez estamos sobre la base, ejecutamos esta query.

![apartado1Consulta](https://github.com/user-attachments/assets/f5ecc3fb-f1b8-4af5-a9ec-ebe816fc9a07)

Le damos a ***ejecutar query*** y nos saldrá esto.

![apartado1resultado1](https://github.com/user-attachments/assets/153b3f48-662e-417a-bbe5-0db6ce6c8342)

Para comprobar que se creó la tabla, hay que recargar la página. Aquí la tenemos

![apartado1resultado2](https://github.com/user-attachments/assets/8ac8627a-0ee9-4005-a9e9-6b78948ee190)

### 3. Apartado 2 de la tarea 🤗

Enunciado del apartado.

```bash
Inserta 5 registros inventados en la tabla a través de una sentencia SQL.
```

Nos vamos al apartado de las querys en el PgAdmin, y ejecutamos esto.

![apartado2Consulta](https://github.com/user-attachments/assets/bebed270-8f3f-4cd7-8895-50bb7809f4b4)

Para comprobarlo, nos vamos a la tabla y le damos en **view/all rows**

![apartado2Resultado2](https://github.com/user-attachments/assets/97c8c24f-3fbe-40cb-84aa-536443072c30)

Nos saldrá esto.

![apartado2Resultado4](https://github.com/user-attachments/assets/5e880a5a-048a-4552-9d3c-2d94b2400944)


### 4. Apartado 3 de la tarea 🤗

Enunciado del apartado.

```bash
Realiza una consulta donde se muestren todos los datos de la tabla EmpresasFCT
 ordenados por fechaContacto, de modo que en la primera fi la salga el que tenga la fecha más reciente
```

Nos vamos al apartado de las querys en el PgAdmin, y ejecutamos esto.

![apartado3consulta](https://github.com/user-attachments/assets/3203c19d-7425-4845-aba3-8067f4b2febe)

Este es el resultado.

![apartado3resultado](https://github.com/user-attachments/assets/5b42174c-ca3c-4270-8832-7211d8e30121)

### 5. Apartado 4 de la tarea 🤗

Enunciado del apartado.

```bash
Realiza una consulta que permita obtener un listado de todos los contactos de Odoo (no empresas) con la siguiente información:
- Nombre
- Cuya ciudad sea Tracy, y código postal 95304
- Nombre comercial de la empresa
ordenados alfabéticamente por el nombre comercial de la empresa,
```

Nos vamos al apartado de las querys en el PgAdmin, y ejecutamos esto.

![apartado4consulta](https://github.com/user-attachments/assets/0d809fcb-e607-415c-b07f-7fc149211540)

### 6. Apartado 5 de la tarea 🤗

Enunciado del apartado.

```bash
Utilizando las tablas de odoo, obtén un listado de empresas proveedoras, que han emitido algún reembolso (facturas rectifi cativas de proveedor)
- Nombre de la empresa
- Número de factura
- Fecha de la factura -total de factura con impuestos
- Total factura SIN impuestos
Ordenadas por fecha de factura de modo que la primera sea la más reciente.
```

Nos vamos al apartado de las querys en el PgAdmin, y ejecutamos esto.

![apartado5](https://github.com/user-attachments/assets/ce5908eb-14bd-4a67-9c98-d1a46fb5e7c3)


### 7. Apartado 6 de la tarea 🤗

Enunciado del apartado.

```bash
Utilizando las tablas de odoo, obtén un listado de empresas clientes, a las que se les ha emitido más de dos facturas de venta (solo venta) confi rmadas, mostrando los siguientes datos:
- Nombre de la empresa
- Número de facturas -total de factura con impuestos
- Total facturado SIN IMPUESTOS
```

Nos vamos al apartado de las querys en el PgAdmin, y ejecutamos esto.

![apartado6](https://github.com/user-attachments/assets/38d116dd-5af1-49d9-afb8-56626ffa873a)


### 8. Apartado 7 de la tarea 🤗

Enunciado del apartado.

```bash
Crea una sentencia que actualice el correo de los contactos cuyo dominio es @bilbao.example.com a @bilbao.bizkaia.neus
```

Nos vamos al apartado de las querys en el PgAdmin, y ejecutamos esto.

![apartado7](https://github.com/user-attachments/assets/66cfe599-4612-4c79-94ed-203f41f7005a)

Lo comprobamos.

![apartado7parte2](https://github.com/user-attachments/assets/5a521da3-8b43-4b04-ae2b-7a6000052ae2)








