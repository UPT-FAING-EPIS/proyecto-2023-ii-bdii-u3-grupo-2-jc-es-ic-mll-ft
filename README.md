[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/UWDcn9m9)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=13075476&assignment_repo_type=AssignmentRepo)

# API COMPRA DE PASAJES - NOTIFICACIONES

## Resumen 
La empresa de transporte requiere implementar un sistema de envío de
mensajes por correo notificando al cliente cada vez que su registro se realiza con
éxito.
Actualmente cuentan con un sistema de registro de pasajes, y para evitar la
saturación del servicio es que se va a implementar un sistema de envío de
mensajes de correo.
Debido a la gran demanda en la venta de pasajes, se implementará un servicio
intermediario como Amazon SQS el cual gestiona una cola de notificaciones.
El sistema de envío de mensajes leerá las notificaciones en la cola de AWS SQS
e irá enviando mensajes en segundo plano.
## Abstract
The transportation company needs to implement an email messaging system to
notify the customer each time their registration is successfully completed.
Currently, they have a ticket registration system, and to prevent service
saturation, an email messaging system will be implemented. Due to the high
demand in ticket sales, an intermediary service such as Amazon SQS will be
implemented, which manages a notification queue. The messaging system will
read notifications from the AWS SQS queue and send messages in the
background.
## 1. Antecedentes e Introducción
La presente documentación describe el proceso de la implementación de
dos sistemas API REST para el registro de venta de pasajes y el envío de
mensajes por correo, para lo cual se hizo uso de una base de datos no
relacional (couchdb) y de un servicio externo de cola de mensajes
AMAZON SQS.
## 2. Título
“API COMPRA DE PASAJES - NOTIFICACIONES”
## 3. Autores

a. Brant Antony Chata Choque
b. Marjiory Grace Llantay Machaca
c. Fiorela Milady Ticahuanca Cutipa

## 4. Planteamiento del problema
a. Problema:
La empresa de compra de pasajes requiere enviar mensajes por
correo cada vez que un cliente compra un pasaje, sin embargo
debido a la alta demanda de la venta de pasajes, el envío de
mensajes a través del sistema requiere de tiempo para proceso de
envío del correo, tiempo el cual puede perjudicar el flujo normal.
b. Justificación
Para dar solución al problema se implementará segundo sistema
cuya finalidad es el envío de mensajes, este segundo sistema hará
uso de una cola de notificaciones donde se mantendrán en cola los
mensajes por enviar.
c. Alcance
Se implementará una cola de notificaciones con Amazon SQS y un
sistema que estará pendiente de nuevas notificaciones en la cola y
que procesará en envío de los mensajes a los correos de los
clientes.
## 5. Objetivos
a. General
Implementar el envío de mensajes de correo utilizando un servicio
de cola de mensajes
b. Específico
Desarrollar el sistema de envío de mensajes utilizando el servicio
de correo y Amazon SQS para la cola de notificaciones.
## 6. Desarrollo de la Propuesta
a. Diagrama de casos de uso
b. Diagrama de Clases
c. Diagrama de Componentes
d. Arquitectura
La arquitectura es cliente servidor con consumo de API REST
e. Diagrama de base de datos
IMPORTANTE: Para una base de datos no relacional no se consideran
las relaciones debido a que un documento puede tener otros
documentos internos, en el caso de este sistema, el cliente está
integrado dentro del registro de COMPRA DE PASAJES.

## 7. Bibliografía
a. Instalación de couchDB en Ubuntu
https://docs.couchdb.org/en/stable/install/index.html
b. Uso de API REST de CouchDB
https://docs.couchdb.org/en/stable/api/index.html
c. Paquete Simple SQS para laravel
https://github.com/tedicela/sqs-simple
d. Generación de comandos en laravel
https://laravel.com/docs/10.x/artisan#generating-commands
## 8. Anexos
Para el desarrollo de los sistemas se requirió lo siguiente:
a. Sistema Operativo Ubuntu 22.04.03 LTS
b. Apache CouchDB
c. Amazon SQS
d. Laravel 10
e. Servidor Web Apache
f. Lenguaje de programación PHP v8
