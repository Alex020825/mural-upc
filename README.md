# Project Plan - Mural UPC-SA

## Nombre Del Proyecto
Mural UPC-SA

## Descripción General
Plataforma web académica orientada a la comunidad de la Universidad Popular del Cesar (seccional Aguachica) para compartir y consultar parciales y material de estudio de manera organizada, segura y restringida.

## Problema
En la Universidad Popular del Cesar muchos estudiantes experimentan ansiedad frente a los parciales cuando un docente es nuevo o desconocen su metodología de evaluación. La falta de un repositorio centralizado de material de práctica dificulta su preparación académica.

## Objetivo
Desarrollar una solución web donde los alumnos puedan subir, organizar y consultar archivos de exámenes anteriores para practicar de forma segura y colaborativa.

## Actores
* Estudiantes de la Universidad Popular del Cesar.
* Administradores / Moderadores de la plataforma.

## Reglas De Negocio

### Registro Y Autenticación
* Solo podrán inscribirse personas con correo institucional único (dominio @unicesar.edu.co).
* La autenticación mediante tokens (JWT) es obligatoria para acceder a las funciones de consulta y subida.
* Los usuarios solo podrán editar o eliminar el contenido publicado por ellos mismos.

### Gestión De Parciales
* Cada publicación debe contener los siguientes campos obligatorios:
  * Título del recurso.
  * Curso / Asignatura.
  * Profesor de la materia.
  * Archivo adjunto.
* El formato permitido es exclusivamente PDF.
* El tamaño máximo de archivo soportado es de 10 MB.

### Registro De Fechas Y Auditoría
* Cada registro guardará automáticamente su fecha de creación.
* Se mantendrá una auditoría de publicaciones para evitar spam o contenido ajeno al propósito académico.

## Estructura Y Módulos Del Sistema

### Módulo De Autenticación
* Registro de usuario.
* Inicio de sesión.
* Gestión de perfil.

### Módulo De Parciales
* Carga de archivos PDF.
* Búsqueda con filtros por curso, profesor y fecha.
* Visualización e historial de parciales del usuario.

## Stack Tecnológico
* Backend: Node.js, NestJS, TypeScript.
* Frontend: React.
* Base de Datos: PostgreSQL.
* Control de Versiones: Git, GitHub.