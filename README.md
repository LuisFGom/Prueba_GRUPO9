# Prueba_GRUPO9

PASOS PARA EL USO DEL REPOSITORIO 
 1.- Abrir el proyecto en visual studio.
 2.- Dirigirnos a herramientas e ingresar a "Administrador de paquetes NuGet"
 3.- Ingresamos en Consola del Administrador de paquetes 
 4.- Una vez dentro ingresamos los siguientes comandos:
     -   Add-Migration GestionEstudiantes
     -   Update-Database

EXPLICACION:

Alumnos participantes:
-	Gómez Llerena Luis Fernando
-	Laura Laura Stalin Alejandro
-	Pico Chuiza Antonio Damían

Asignatura:	Programación Avanzada

Docente:	Ing. Jose Caiza Mg.

II.	INFORME DE GUÍA PRÁCTICA

1.	Objetivos

1.1.	Objetivo General

Diseñar e implementar un sistema web de gestión académica que facilite a la Secretaría de la institución educativa la administración eficiente de estudiantes, docentes, matrículas, materias y horarios, optimizando los procesos internos mediante el uso de tecnologías web modernas y una base de datos relacional, usando una API RESTful y además ayudándonos de tecnologías modernas basadas en ASP.NET Core y una base de datos SQL Server.
1.2.	Objetivos Específicos
	Desarrollar un módulo de registro y actualización de estudiantes, que permita a la Secretaría almacenar y gestionar información personal, académica y de contacto de manera segura y estructurada.
	Implementar un módulo de gestión de docentes, con funciones para registrar, editar y eliminar datos personales y académicos, asegurando la integridad de la información del cuerpo docente.
	Diseñar un sistema de matrícula académica, que permita a la Secretaría asignar materias a los estudiantes, relacionándolas con semestres y carreras de forma controlada y coherente.
	Desarrollar un sistema de inicio de sesión con control de roles, diferenciando accesos para secretaría, docentes, estudiantes y superusuarios, garantizando la seguridad y la confidencialidad de los datos.
 
	Implementar una base de datos optimizada en SQL Server, que respalde todos los módulos del sistema, asegurando consistencia, disponibilidad y escalabilidad de la información.
	Diseñar una interfaz web intuitiva y responsiva, utilizando Razor Pages y buenas prácticas de desarrollo, que facilite el uso del sistema a usuarios no técnicos.
2.	Introducción
En la actualidad, las instituciones de educación requieren herramientas tecnológicas que garanticen la eficiencia, seguridad y accesibilidad en la gestión de sus procesos académicos. Entre los departamentos más críticos se encuentra la Secretaría Académica, responsable de organizar la información de estudiantes, docentes, materias, matrículas, horarios y aulas, tareas que tradicionalmente se han llevado a cabo de forma manual o mediante sistemas limitados, propensos a errores, duplicidad de datos y pérdida de información. En este contexto, el desarrollo de un sistema web robusto y adaptable se convierte en una necesidad estratégica.
Este proyecto tiene como finalidad el diseño e implementación de un sistema de gestión académica basado en arquitectura web, orientado a cubrir las necesidades específicas de la Secretaría Académica de una institución educativa. El sistema contempla múltiples módulos funcionales interrelacionados, incluyendo el registro de estudiantes y docentes, la gestión de materias por semestres, la matrícula académica, la asignación de horarios y aulas, así como la generación automática de horarios individuales para estudiantes y docentes. Todo esto estará controlado mediante un sistema de autenticación con gestión de roles, que delimita los permisos y accesos según el tipo de usuario (secretaría, estudiante, docente y superusuario).
La propuesta será construida empleando C# dentro del framework ASP.NET Core junto con SQL Server como motor de base de datos, lo que permitirá una solución robusta, escalable y de fácil mantenimiento. Se priorizará una interfaz clara y adaptable a cualquier dispositivo, favoreciendo la experiencia del usuario desde distintos navegadores.
Este sistema busca solucionar problemas comunes como la repetición de matrículas, conflictos en los horarios o falta de control en la asignación docente. A su vez, permitirá un registro preciso de cada acción realizada, lo cual será clave para llevar un control administrativo efectivo y facilitar la toma de decisiones basada en información confiable.
En el presente documento se expone el desarrollo completo del sistema, desde su concepción hasta su implementación, abarcando tanto los aspectos funcionales como los técnicos que garantizan un producto final eficiente y bien estructurado.
3.	Marco Teórico

3.1.	Sistemas de Gestión Académica (SGA)
Un Sistema de Gestión Académica (SGA) es una herramienta tecnológica diseñada para facilitar y automatizar los procesos tanto administrativos como académicos dentro de una institución educativa. Gracias a estos sistemas, es posible manejar información relacionada con estudiantes, docentes, materias, matrículas, horarios, y evaluaciones, entre otros aspectos clave. Su implementación contribuye a reducir errores manuales, agilizar tareas repetitivas y permitir un acceso seguro y controlado a la información.
Principales funciones de un SGA:
	Registro de estudiantes y docentes: Permite llevar un control organizado de los datos personales y académicos de los involucrados.
	Matrícula por semestre: Facilita la inscripción de los estudiantes en las materias correspondientes.
	Gestión de horarios: Ayuda a estructurar los tiempos de clases, asignando aulas y docentes de forma adecuada.
	Generación de reportes: Automatiza la elaboración de informes académicos y administrativos.
3.2.	Arquitectura Web
La arquitectura web define cómo se organiza y estructura una aplicación que funciona a través de un navegador. Este enfoque ofrece la ventaja de que el sistema puede ser utilizado desde cualquier lugar, siempre que se cuente con conexión a internet. En este proyecto se usa una arquitectura moderna que aprovecha tecnologías como ASP.NET Core, lo cual permite desarrollar aplicaciones eficientes, multiplataforma y fáciles de mantener.
Entre sus beneficios están:
	Acceso desde cualquier lugar: No es necesario instalar programas adicionales.
	Escalabilidad: El sistema puede crecer según las necesidades sin perder rendimiento.
	Mantenimiento centralizado: Las actualizaciones se realizan en un solo lugar, reduciendo problemas técnicos.
3.3.	Framework ASP.NET Core con API RESTful
ASP.NET Core es un entorno de desarrollo moderno que permite crear aplicaciones web dinámicas. En este proyecto se emplean API RESTful, una forma eficiente de crear páginas que reaccionan a la interacción del usuario. Nuestra API facilita separar claramente la lógica del sistema y la presentación visual, lo que resulta en un código más organizado y fácil de mantener.
Ventajas principales:
	Crea páginas dinámicas desde el servidor.
	Permite una mejor organización del código.
	Es ideal para aplicaciones como este SGA, donde el usuario accede a diversas funciones constantemente.






	 
3.4.	Bases de Datos Relacionales (SQL Server)
Para almacenar los datos del sistema, se utilizan bases de datos relacionales. En este caso, se opta por SQL Server, un sistema robusto y confiable que permite organizar y acceder a grandes volúmenes de información de manera rápida y segura.
                  Puntos fuertes:
	Integridad de datos: Se mantienen relaciones claras entre tablas mediante claves primarias y foráneas.
	Consultas potentes: Se pueden realizar búsquedas complejas mediante SQL.
	Buen rendimiento: Funciona bien incluso con grandes cantidades de información.
3.5.	Autenticación y Roles de Usuario
Una parte fundamental del sistema es controlar quién puede acceder a qué. Para esto, se implementa un modelo de autenticación y roles. Esto asegura que cada usuario tenga acceso solamente a las funciones que le corresponden según su perfil: por ejemplo, el estudiante solo puede ver su matrícula, mientras que el docente puede consultar su horario y calificar.
Aspectos clave:
	Autenticación: Verifica la identidad del usuario (normalmente con usuario y contraseña).
	Gestión de roles: Asigna permisos dependiendo del tipo de usuario.
	Control de acceso (RBAC): Sistema que asigna permisos según el rol de cada usuario.
3.6.	 Diseño de Interfaz y Experiencia de Usuario
La interfaz del sistema debe ser clara, sencilla y fácil de usar, para que cualquier usuario, sin importar su nivel técnico, pueda navegarla sin problemas. El diseño responsive garantiza que la aplicación se vea bien tanto en computadoras como en celulares o tabletas.
Principios aplicados:
	Consistencia visual: Uso uniforme de colores, fuentes y botones.
	Simplicidad: Se evitan menús confusos o sobrecarga de elementos.
	Adaptabilidad: Funciona correctamente en cualquier tamaño de pantalla.
	 
4.	Herramientas empleadas

-	Visual Studio 2022

-	ASP.NET Core Web API

-	Microsoft SQL Server Management Studio (SSMS)

-	Entity Framework Core

-	Swagger

-	GitHub

-	Inteligencia Artificial

-	Internet y Laptops

-	Plataformas educativas (Youtube)

5.	Requisitos Funcionales y no Funcionales 

REQUISITOS FUNCIONALES

Requisito	Descripción	Nivel de Importancia
Registrar estudiantes	Ingreso de nuevos estudiantes con sus datos básicos.	Muy alto
Modificar y eliminar estudiantes	Actualización y eliminación de registros de estudiantes.	Alto
Registrar docentes	Guardar la información personal y académica de los docentes.	Alto
Asignar docentes a materias	Relacionar docentes con las materias que impartirán.	Muy alto
Registrar Materias	Crear nuevas materias con créditos, semestre y nombre.
	Muy alto
Gestionar semestres académicos	Clasificar materias por semestre.	Alto
Matricular estudiantes en materias	Inscribir estudiantes en materias de uno o más semestres.	Muy alto
Consultar información	Consultar estudiantes por materia, materias por estudiante, etc.	Alto
Eliminar registros	Eliminar estudiantes, materias o inscripciones.	Medio
Generar reportes	Crear reportes de matrícula, docentes, y materias.	Alto

REQUISITOS NO FUNCIONALES

Requisito	Descripción	Nivel de Importancia
Desarrollado en Visual Studio	Front End	Muy alto
Persistencia con SQL Server	Conexión estable a base de datos SQL Server.	Muy alto
Estructura en capas y uso de interfaces	Arquitectura limpia y mantenible.	Alto

Interfaz fácil de usar
Formularios claros y con buena experiencia de usuario.	Muy alto
Validación de entradas	
Validaciones para evitar errores y datos incorrectos.	Muy alto
Rendimiento fluido	Respuesta rápida del sistema en las operaciones.	Alto
Funcionamiento local sin internet	
El sistema debe ejecutarse sin conexión.	Alto
Publicación local	El sistema debe poder ser publicado localmente.	Alto


6.	Desarrollo del Sistema

	Planificación General del Proyecto
El desarrollo de este sistema comenzó con una etapa de planificación funcional y técnica, donde se definió con claridad el objetivo general: crear un sistema de matrículas académico que gestione estudiantes, docentes, materias, semestres, horarios y notas, diferenciando los permisos según los roles de los usuarios.
En esta etapa también se establecieron los cuatro tipos de usuarios que podrían ingresar al sistema:
•	Secretaría: responsable de registrar y gestionar estudiantes, docentes, materias, horarios y realizar matrículas.
•	Docente: puede ver sus horarios y registrar calificaciones.
•	Estudiante: tiene acceso a su horario, materias inscritas y sus calificaciones.
•	Superusuario: tiene control total sobre el sistema, actuando como administrador general.
Nos aseguramos de que cada módulo estuviera bien pensado desde el punto de vista de la funcionalidad y de la experiencia de usuario. Este análisis inicial permitió tomar decisiones sobre la estructura del sistema, la base de datos y la forma en que interactuarían los formularios con la lógica interna.



 
 
 

 
 
	Creación del Proyecto y Estructura Base
El proyecto fue creado como ASP.NET Core Web API en Visual Studio 2022.
Estructura del proyecto:
•	Controllers: Exponen los endpoints HTTP.
•	Models: Clases que representan las entidades (Estudiante, Docente, Materia...).
•	DTOs: Objetos que trasladan información entre capas.
•	Services: Encapsulan la lógica de negocio.
•	Repositories: Acceso a datos mediante Entity Framework Core.
Esto nos permitió mantener el código limpio, separado por responsabilidades y fácil de mantener o escalar en el futuro.

   
	Diseño e Implementación de la Base de Datos
Uno de los pasos fundamentales fue el diseño y la creación de la base de datos en SQL Server. Se diseñaron las tablas siguiendo principios de normalización para garantizar integridad y eficiencia. Las tablas más importantes creadas fueron:
•	Estudiantes: contiene la información personal y académica de los alumnos.
•	Docentes: registra los datos de los profesores.
•	Materias: lista de asignaturas con su respectivo semestre y carga académica.
•	Semestres: registra periodos académicos como “2025-I”, “2025-II”, etc.
•	Horarios: define en qué días, horas y aulas se imparten las materias, y qué docente las imparte.
•	Usuarios: datos de acceso (usuario y contraseña) vinculados con la tabla de roles.
•	Roles: define los cuatro perfiles del sistema.
•	Matriculas: vincula estudiantes con las materias en las que se inscriben.
•	Notas: permite registrar calificaciones por estudiante y por materia.
Cada tabla cuenta con claves primarias, foráneas y restricciones para asegurar la integridad referencial. Por ejemplo, no se puede eliminar un docente si está asignado a un horario, o un estudiante si ya tiene notas registradas.
	Conexión a la Base de Datos desde la Aplicación
Para facilitar el acceso a la base de datos desde nuestra aplicación, creamos una clase DataBaseManager que se encarga de manejar la cadena de conexión y ejecutar consultas SQL utilizando objetos como SqlConnection, SqlCommand y SqlDataReader.
Esto nos permitió crear clases Repository específicas para cada entidad, que encapsulan todas las operaciones CRUD. Por ejemplo, EstudianteRepository maneja la creación, edición, eliminación y consulta de estudiantes.
Esta separación entre la lógica de presentación (formularios) y la lógica de datos (repositorios) sigue el patrón MVC básico, y mejora la mantenibilidad del sistema.
 
 

	Pantalla de Inicio de Sesión (Login)
El primer formulario funcional fue el LoginForm. En él, el usuario debe ingresar su nombre de usuario y contraseña. Cuando hace clic en “Iniciar sesión”, el sistema consulta en la base de datos si las credenciales existen y obtiene el rol del usuario.
Según el rol, se abre una interfaz diferente:
•	Si es Secretaría, se abre el SecretariaForm, con acceso completo a los módulos de gestión.
•	Si es Docente, accede a su panel con materias asignadas y opción de ingresar notas.
•	Si es Estudiante, ve su horario y sus calificaciones.
•	Si es Superusuario, tiene una interfaz administrativa con todos los módulos disponibles.
Esto garantiza que cada usuario solo acceda a las funciones que le corresponden.
	Gestión de Estudiantes
La gestión de estudiantes se realiza desde el formulario EstudiantesForm, al que acceden tanto la secretaría como el superusuario. Desde aquí se pueden realizar las siguientes acciones:
•	Agregar un nuevo estudiante, ingresando datos como nombres, apellidos, cédula, fecha de nacimiento, sexo y correo electrónico.
•	Editar datos de un estudiante existente, donde los datos se cargan en los campos correspondientes y se permite modificarlos.
•	Eliminar estudiantes, siempre que no tengan matrículas o notas asociadas.
Además, se realizan validaciones automáticas antes de guardar:
•	Nombres solo deben contener letras y espacios.
•	Fecha de nacimiento válida (mínimo 18 años).
•	Correo con formato correcto.
Los estudiantes se listan en un DataGridView, con botones personalizados para editar o eliminar directamente desde cada fila.
 
 
 
	Gestión de Docentes
El módulo DocentesForm tiene una lógica muy parecida. Aquí se permite:
•	Registrar docentes nuevos, con validaciones similares (edad mínima de 20 años, nombres válidos, correo institucional, etc.).
•	Editar o eliminar docentes según las restricciones del sistema.
•	Consultar las materias asignadas a cada docente.
Este formulario está diseñado pensando en facilitar a la secretaría la gestión de personal académico.
 

 

 
 
	Gestión de Materias y Semestres
En el formulario de materias, la secretaría puede:
•	Crear nuevas materias especificando su nombre, código, número de créditos y semestre correspondiente.
•	Asignar si tiene prerrequisitos o correquisitos (a futuro se podría implementar la validación de estos).
Desde el módulo de semestres, también es posible registrar nuevos periodos académicos y asociarlos a las materias. Esto permite organizar la oferta académica por ciclos.
 
 
	Matrícula de Estudiantes
Desde este módulo, la secretaría puede seleccionar un estudiante y ver las materias disponibles por semestre. Luego, se pueden seleccionar las materias a matricular.
Una vez guardada la matrícula:
•	Se registra la relación en la tabla Matriculas.
•	Se actualiza el horario del estudiante automáticamente.
Se asegura que un estudiante no se matricule dos veces en la misma materia, y que las materias estén disponibles en su semestre actual.

 
 
	Panel del Docente
Al iniciar sesión, el docente ve una interfaz personalizada donde se muestra:
•	La lista de materias que imparte.
•	El horario de clases.
•	Los estudiantes inscritos en cada materia.
Además, tiene la opción de ingresar calificaciones por cada estudiante. El sistema valida que las notas estén entre 0 y 10, y luego se guardan en la tabla Notas.
	Panel del Estudiante
El estudiante accede a su propia interfaz, donde puede:
•	Ver su horario completo, con materias, docentes y aulas.
•	Consultar sus notas registradas hasta el momento.
Este panel fue diseñado para ser simple, claro y fácil de usar, ya que es el usuario con menos funciones del sistema.
	Pruebas y Validaciones del Sistema
Durante la etapa final del desarrollo realizamos múltiples pruebas:
•	Validamos que no se permitan registros con datos inválidos.
•	Comprobamos que las ediciones se reflejan correctamente.
•	Probamos la matriculación con múltiples estudiantes.
•	Simulamos colisiones de horario para probar las validaciones.
•	Probamos el login con diferentes roles.
Estas pruebas garantizaron que el sistema se comporte de forma estable y que la experiencia del usuario sea correcta.
 
 
7.	Conclusiones
	El desarrollo de este sistema de matrículas permitió aplicar de forma práctica los conocimientos adquiridos en programación orientada a objetos, diseño de interfaces, validación de datos y conexión a bases de datos, integrando todo en un solo proyecto funcional.

	Aprendimos a organizar y estructurar correctamente una aplicación real, separando la lógica en capas para que fuera más mantenible, limpia y fácil de entender.

	Nos dimos cuenta de la importancia de validar los datos correctamente desde el formulario, ya que incluso un pequeño error puede afectar la funcionalidad general del sistema.

	El uso de roles dentro del sistema nos permitió personalizar la experiencia de cada tipo de usuario, mejorando la seguridad y facilitando el acceso solo a las funciones que le corresponden.

	Implementar funcionalidades como el control de horarios, la matrícula por semestres y la gestión de calificaciones nos ayudó a entender mejor cómo se conectan los diferentes procesos dentro de una institución educativa.

	Este proyecto también nos enseñó a trabajar con bases de datos relacionales más completas, aplicando relaciones uno a muchos y muchas a muchos, lo cual fue fundamental para poder manejar información como notas, horarios y materias inscritas.

	En general, fue un proyecto muy completo que nos permitió simular un escenario real, y que nos dejó listos para enfrentar desafíos más grandes a nivel profesional.
8.	Referencias bibliográficas
[1] R. Rojas, Programación orientada a objetos con C#. Alfaomega Grupo Editor, 2020.
[2] F. Charte, C# 10 y .NET 6 – Desarrollo moderno para multiplataforma. Marcombo,   2022.
[4] Microsoft, “Conectarse a bases de datos con ADO.NET,” Microsoft Learn, en línea: https://learn.microsoft.com/es-es/dotnet/framework/data/adonet/ado-net-overview.
[5] J. Castro y R. Escobar, Desarrollo de aplicaciones empresariales con C# y SQL Server. Universidad de Antioquia, 2018.
[6] S. Coronel y S. Morris, Bases de datos: Diseño y aplicación, 12.ª ed., Cengage Learning, 2019.
[7] M. Sierra, “Diseño e implementación de un sistema de gestión académica en C# y SQL Server para una institución educativa,” Tesis de grado, Universidad Técnica de Ambato, Ecuador, 2020.
[8] F. Prieto, “Diseño de sistemas de matrícula académica en entornos de desarrollo .NET con acceso a bases de datos relacionales,” Revista Iberoamericana de Tecnología Educativa, vol. 12, no. 1, pp. 45–52, 2021.
