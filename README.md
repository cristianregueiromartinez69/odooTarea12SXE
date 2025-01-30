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





