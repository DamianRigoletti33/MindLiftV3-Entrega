# MindLiftV3-Entrega
Repositorio principal de documentación del proyecto MindLift. Contiene la documentación técnica, evidencias, plan de pruebas, gestión del proyecto y enlaces a los repositorios del backend, aplicación Android y plataforma web.


# MindLift - Plataforma de Rehabilitación y Movilidad Reducida

## Descripción del Proyecto

MindLift es una plataforma desarrollada para apoyar el proceso de rehabilitación física de personas con movilidad reducida y adultos mayores. El sistema permite la gestión de pacientes, profesionales de la salud y administradores mediante una arquitectura cliente-servidor, facilitando el seguimiento terapéutico, la asignación de rutinas y el monitoreo del progreso de cada paciente.

El proyecto fue desarrollado utilizando una arquitectura basada en una aplicación Android, un backend desarrollado en Spring Boot y una base de datos MySQL. La comunicación entre la aplicación móvil y el backend se realiza mediante Retrofit, permitiendo el consumo de servicios REST y dejando preparada la solución para una futura migración a infraestructura cloud utilizando AWS EC2 y AWS RDS.

---

### REPOSITORIOS DEL PROYECTO
* App y Backend:
* https://github.com/DamianRigoletti33/MindLift-AppV3
* https://github.com/DamianRigoletti33/Mindlift-BackendV3
* 

* Web Frontend y Backend:
* https://github.com/DamianRigoletti33/Mindlift-Frontend-WebV3
* https://github.com/DamianRigoletti33/MindLift-Backend-WebV3
* 

# Objetivos

* Facilitar el seguimiento del proceso de rehabilitación.
* Gestionar pacientes y profesionales desde una plataforma centralizada.
* Permitir la asignación de rutinas terapéuticas personalizadas.
* Registrar el progreso clínico del paciente.
* Incorporar apoyo mediante Inteligencia Artificial supervisada.
* Mantener una arquitectura escalable preparada para infraestructura cloud.

---

# Arquitectura del Proyecto

```
Android App (Java)
        │
     Retrofit
        │
REST API (Spring Boot)
        │
Spring Data JPA
        │
MySQL
```

La aplicación consume servicios REST mediante Retrofit, los cuales son procesados por el backend desarrollado en Spring Boot. Toda la información es almacenada en una base de datos MySQL.

---

# Tecnologías Utilizadas

## Aplicación Móvil

* Java
* Android Studio
* Retrofit
* Material Design

## Backend

* Java 21
* Spring Boot
* Spring Web
* Spring Data JPA
* Maven

## Base de Datos

* MySQL
* MySQL Workbench
* XAMPP (entorno local)

## Herramientas

* Postman
* Git
* GitHub
* JUnit
* Mockito
* Vitest (pruebas desarrolladas durante el proceso de validación)

---

# Funcionalidades

## Paciente

* Inicio de sesión.
* Visualización de rutinas.
* Registro del progreso.
* Actualización de ficha médica.
* Consulta de respuestas asistidas por IA.

## Profesional

* Inicio de sesión.
* Gestión de pacientes.
* Creación y modificación de rutinas.
* Revisión de consultas mediante IA.
* Seguimiento clínico.

## Administrador

* Gestión de usuarios.
* Administración de profesionales.
* Administración de pacientes.
* Control general de la plataforma.

---

# Instalación

## Clonar el repositorio

```bash
git clone https://github.com/USUARIO/MindLift.git
```

---

## Backend

```bash
cd backend
```

Ejecutar

```bash
mvn spring-boot:run
```

El servidor iniciará en:

```
http://localhost:8080
```

---

## Base de Datos

Crear una base de datos MySQL denominada:

```
mindlift_db
```

Configurar las credenciales correspondientes en el archivo:

```
application.properties
```

---

## Aplicación Android

Abrir el proyecto desde Android Studio.

Configurar la URL del backend en Retrofit:

```
http://10.0.2.2:8080/
```

para emulador Android.

---

# Servicios REST

Algunos endpoints disponibles:

```
POST /api/auth/login
```

```
GET /api/patients
```

```
POST /api/patients
```

```
GET /api/professionals
```

```
POST /api/professionals
```

```
GET /api/exercises
```

```
GET /api/routines
```

---

# Base de Datos

El sistema almacena información en las siguientes tablas principales:

* usuarios
* pacientes
* profesionales
* rutinas
* ejercicios

---

# Pruebas Realizadas

Durante el desarrollo del proyecto se realizaron diferentes pruebas para validar el funcionamiento de la plataforma.

### Pruebas Unitarias

* Validación del proceso de autenticación.
* Verificación de componentes principales.
* Validación de lógica de negocio.

### Pruebas mediante Postman

* Inicio del backend.
* Login exitoso de pacientes.
* Login exitoso de profesionales.
* Validación de credenciales incorrectas.
* Consulta de pacientes.
* Consulta de profesionales.
* Registro de nuevos profesionales.
* Consulta de ejercicios terapéuticos.
  
  

### Validación Base de Datos

Se comprobó el correcto almacenamiento de la información en las tablas:

* usuarios
* pacientes
* profesionales

---

### Documentación del Proyecto
#Documentacion APP

[EVIDENCIAS PRINCIPAL FUNCIONAMIENTO DE APP.docx](https://github.com/user-attachments/files/29389354/EVIDENCIAS.PRINCIPAL.FUNCIONAMIENTO.DE.APP.docx)
[PRUEBAS UNITARIAS Y MYSQL- MINDLIFT.docx](https://github.com/user-attachments/files/29389414/PRUEBAS.UNITARIAS.Y.MYSQL-.MINDLIFT.docx)

---

#Documentacion WEB
[pruebas_unitarias.docx](https://github.com/user-attachments/files/29389472/pruebas_unitarias.docx)
[documentacion_pagina_web.docx](https://github.com/user-attachments/files/29389384/documentacion_pagina_web.docx)
[PRUEBAS POSTMAN MINDLIFT.docx](https://github.com/user-attachments/files/29389371/PRUEBAS.POSTMAN.MINDLIFT.docx)


### Escalabilidad

La aplicación fue diseñada considerando una futura implementación sobre infraestructura cloud.

Actualmente la comunicación entre la aplicación Android y el backend se realiza mediante Retrofit utilizando un entorno local. Gracias a esta arquitectura, la migración hacia servicios como AWS EC2 y AWS RDS requerirá únicamente modificar la configuración de conexión, manteniendo la misma lógica de funcionamiento del sistema.

---
- Taller de Programación - 
Damián Rigoletti
Benjamín Sanez 
