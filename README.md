# 💻🖱️ Proyecto de Base de Datos para Bootcamp en PostgreSQL

## Descripción del Proyecto:
Este proyecto de base de datos está diseñado para gestionar la información necesaria para un bootcamp educativo. Utiliza PostgreSQL como sistema de gestión de bases de datos relacional para almacenar y manejar los datos críticos del bootcamp.

## 🎛️ Estructura de la Base de Datos:
El esquema de la base de datos está organizado en varias tablas principales que capturan diferentes aspectos del bootcamp, incluyendo:

- Usuarios: Información de los estudiantes, instructores y administradores.
- Cursos: Detalles sobre los cursos ofrecidos en el bootcamp.
- Matriculación: Relaciones entre usuarios y cursos matriculados.
- Evaluaciones: Registro de las evaluaciones realizadas durante el curso.
- Calificaciones: Resultados y calificaciones de los estudiantes en las evaluaciones.
- Además, se utilizan tablas auxiliares para almacenar información adicional como sesiones, materiales del curso y registros de asistencia.

## Configuración y Requisitos:
- PostgreSQL: Se requiere una instalación de PostgreSQL versión X.X o superior.
- Conexión: Asegúrese de tener los parámetros de conexión adecuados en el archivo de configuración.
- Creación de Tablas: Ejecute el script de creación de tablas (create_tables.sql) para configurar la estructura inicial de la base de datos.

## Uso y Funcionalidades:
- Inserción de Datos: Utilice los scripts proporcionados (insert_data.sql) para poblar la base de datos con datos de prueba.
- Consultas SQL: Se han incluido ejemplos básicos de consultas SQL (queries.sql) para obtener información relevante sobre los usuarios, cursos y evaluaciones.
- Mantenimiento: Revise y actualice periódicamente la base de datos según sea necesario para reflejar cambios en el bootcamp.

## Queries de prueba: 

SELECT * FROM cursos as c
INNER JOIN vertical as v ON v.verticalid = c.verticalid
where vertical = 'DS'

SELECT claustro.rol, claustro.nombre, cursos.verticalid, cursos.promocionid FROM claustro
INNER JOIN claustro_cursos ON claustro_cursos.claustroid = claustro.claustroid
INNER JOIN cursos ON cursos.cursoid= claustro_cursos.cursoid
WHERE verticalid = '2'

SELECT claustro.rol, claustro.nombre, cursos.verticalid, cursos.promocionid FROM claustro
INNER JOIN claustro_cursos ON claustro_cursos.claustroid = claustro.claustroid
INNER JOIN cursos ON cursos.cursoid= claustro_cursos.cursoid
WHERE rol = 'TA'

SELECT * FROM alumnos
INNER JOIN proyectosalumnos ON proyectosalumnos.alumnoid = alumnos.alumnoid

SELECT * FROM proyectos
INNER JOIN proyectosalumnos ON proyectosalumnos.proyectoid = proyectos.proyectoid


### Contacto:
Para cualquier pregunta o sugerencia sobre este proyecto de base de datos, no dude en contactar al equipo de desarrollo en desousaga@gmail.com, rafamarcos14.rm@gmail.com o acosta.luisc15@gmail.com.

### Notas Adicionales:
- Seguridad: Asegúrese de mantener la seguridad de la base de datos mediante la gestión adecuada de permisos y acceso.
- Documentación: Mantenga actualizada la documentación sobre el esquema de la base de datos y cualquier cambio importante realizado.
- Escalabilidad: Diseñe la base de datos con la escalabilidad en mente para soportar potenciales expansiones del bootcamp en el futuro.

Proyecto Creado por:
- Luis
- Rafael
- Gabriel
- Antonio

Fecha de Creación: 14/06/2024
