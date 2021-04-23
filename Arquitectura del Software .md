# Diseño y Arquitectura de Software
## Estilos
- Capas  (con frecuencia de tres capas)
- Modelo-Vista-Controlador
- Tuberias y Filtros
- Arquitectura de maquinas virtuales
- Sistema de Pizarra o Repositorio
- Peer-to-peer
- Orientada a objetos
- Arquitectura basada en componentes

### Capas (con frecuencia de tres capas)
> Garlan y Shaw definen el modelo de capas como una organizacion jerarquica tal que cada una proporcion servicios a la capa inmediatamente superior y se sirve de las prestaciones que le brinda la inmediatamente inferior.
- Existen mas de 100 patrones o variantes a este estilo.

![IMAGE](http://gyazo.com/2ab8525e7aa764709a7d22e28ffba0bc.png?raw=true)
### Modelo-Vista-Controlador
> El modelo administra comportamiento y los datos del dominio de aplicacion, responde a los requerimientos de informacion sobre su estado(usualmente formulado desde la vista) y responde a instrucciones de cambiar el estado(habitualmente desde el controlador).
-La vista maneja la visualizacion de la informacion
-El controlador interpreta, es el intermediario entre el modelo y la vista.

![IMAGE](http://gyazo.com/06c6f0ad5e6a812a072cd17d533f86af.png?raw=true)
### Tuberias y Filtros
> Una tuberia es el medio por el cual se mueve la informacion y un filtro es un proceso por el cual se puede obtener informacion.
- La secuencia de datos es de tipo FIFO(primero entrar primero salir)
- Sirve para dividir tareas en una secuencia de datos y se utiliza cuando existe gran cantidad de procesos o transformaciones a realizar.

![IMAGE](http://gyazo.com/a4dc78050c94fcfa43fb57d8aada597b.png?raw=true)
### Arquitectura de maquinas virtuales
> Es un software que emula una computadora y puede ejecutar programas como si fuese un ordenador real. Tipos: maquina virtual de sistema: Vthere, ATL, CoLinux, Denali, etc, y Maquina virtual de proceso: Maquina virtual de java.

![IMAGE](http://gyazo.com/e8976e3607dcfbb5b046a4738da93547.png?raw=true)
### Sistema de Pizarra o Repositorio
> En esta estructura hay 2 componentes principales: Una estructura de datos que representa el estado actual y una coleccion de componentes independientes que operan sobre el.
Ejemplos:
- Reconocimiento de patrones.
- Reconocimiento de habla.
- Programacion genetica.
- Evolutiva.
- Grandes motores de busqueda o agentes inteligentes.

![IMAGE](http://gyazo.com/8bbe35d31423e597c36146a020a753a2.png?raw=true)
### Peer-to-peer
> Es una arquitectura muy utilizada en la actualidad. Se usa para compartir archivos de cualquier tipo. Las maquinas pueden ser clientes y servidores a la vez. Ejemplos Ares,Emule, etc.

![IMAGE](http://gyazo.com/408905ffbab4935e107c41f5f84e74a9.png?raw=true)
### Orientada a objetos
> Sus componentes son los objetos, los cuales basan sus principios en encapsulamiento, herencia y polimorfismo.
- Sus interfaces estan separadas de las implementaciones.
- Ejemplo aplicaciones CORBA

![IMAGE](http://gyazo.com/85eee28db7cee93607bb58f58f1ad813.png?raw=true)
### Arquitectura basada en componentes
> Un componente es una unidad de composicion con interfaces especificadas contractualmente y dependencias del contexto explicitas. Que sea una unidad de composicion y no de construccion quiere decir que no es preciso confeccionarla: se puede comprar hecha, o se puede producir en casa para que otras aplicaciones de la empresa la utilcen en sus propias composiciones.

![IMAGE](http://gyazo.com/85d97043e9b3b070563e5efbeeb9d043.png?raw=true)

## ADL
- “Un ADL enfoca en la descripción de la estructura de la aplicación a alto nivel, en lugar de la descripción de la implementación de cualquier módulo específico.”
- ADL es un lenguaje que provee elementos para modelar la arquitectura conceptual de un sistema software, distinguiéndola de la implementación del sistema (Medvidovic&Taylor).
- Constructores básicos de un ADL: Componentes, Conectores, Configuraciones y Restricciones (Tracz, 1993).

![IMAGE](http://gyazo.com/a52ce922d81c9742da10a1d9bfcf7879.png?raw=true)

_**Componentes**_

- Interfaz 
- Tipos 
- Semántica 
- Restricciones (constraints) 
- Evolución 
- Propiedades no funcionales 

_**Conectores**_ 

- Interfaz 
- Tipos 
- Semántica 
- Restricciones 
- Evolución 
- Propiedades no funcionales 

_**Configuraciones arquitectónicas**_ 

- Comprensibilidad 
- Composicionalidad 
- Heterogeneidad 
- Restricciones 
- Refinamiento y trazabilidad 
- Escalabilidad 
- Evolución 
- Dinamismo
- Propiedades no funcionales 

_**Soporte de herramientas**_ 

- Especificación activa 
- Múltiples vistas 
- Análisis 
- Refinamiento 
- Generación de código 
- Dinamismo 

### Componentes
> Representan los elementos computacionales primarios de un sistema. 
Intuitivamente, corresponden a las cajas de las descripciones de caja-y-línea de las 
arquitecturas de software. Ejemplos típicos serían clientes, servidores, filtros, objetos, 
pizarras y bases de datos. En la mayoría de los ADLs los componentes pueden 
exponer varias interfaces, las cuales definen puntos de interacción entre un 
componente y su entorno. 

### Conectores
> Representan interacciones entre componentes. Corresponden a las líneas de las descripciones de caja-y-línea. Ejemplos típicos podrían ser tuberías (pipes), llamadas a procedimientos, broadcast de eventos, protocolos cliente-servidor, o conexiones entre una aplicación y un servidor de base de datos. Los conectores también tienen una especie de interfaz que define los roles entre los componentes participantes en la interacción. 

### Configuraciones o sistemas
> Se constituyen como grafos de componentes y conectores. En los ADLs más avanzados la topología del sistema se define independientemente de los componentes y conectores que lo conforman. Los sistemas también pueden ser jerárquicos: componentes y conectores pueden subsumir la representación de lo que en realidad son complejos subsistemas. 

### Propiedades
> Representan información semántica sobre un sistema más allá de su estructura. Distintos ADLs ponen énfasis en diferentes clases de propiedades, pero todos tienen alguna forma de definir propiedades no funcionales, o pueden admitir herramientas complementarias para analizarlas y determinar, por ejemplo, el throughput y la latencia probables, o cuestiones de seguridad, escalabilidad, dependencia de bibliotecas o servicios específicos, configuraciones mínimas de hardware y tolerancia a fallas. 

### Restricciones
> Representan condiciones de diseño que deben acatarse incluso en el caso que el sistema evolucione en el tiempo. Restricciones típicas serían restricciones en los valores posibles de propiedades o en las configuraciones topológicas admisibles. Por ejemplo, el número de clientes que se puede conectar simultáneamente a un servicio.

### Estilos
> Representan familias de sistemas, un vocabulario de tipos de elementos de diseño y de reglas para componerlos. Ejemplos clásicos serían las arquitecturas de flujo de datos basados en grafos de tuberías (pipes) y filtros, las arquitecturas de pizarras basadas en un espacio de datos compartido, o los sistemas en capas. Algunos estilos prescriben un framework, un estándar de integración de componentes, patrones arquitectónicos o como se lo quiera llamar. 

### Evolución
> Los ADLs deberían soportar procesos de evolución permitiendo derivar subtipos a partir de los componentes e implementando refinamiento de sus rasgos. Sólo unos pocos lo hacen efectivamente, dependiendo para ello de lenguajes que ya no son los de diseño arquitectónico sino los de programación. 

### Propiedades no funcionales
> La especificación de estas propiedades es necesaria para simular la conducta de runtime, analizar la conducta de los componentes, imponer restricciones, mapear implementaciones sobre procesadores determinados, etcétera. 

Atributos de Calidad /Escenarios de calidad
Para identificar los escenarios de calidad se seguirá la siguiente estructura:

	1. Fuente del estímulo: quien o que genera el estímulo. 
	2. Estímulo: lo que se quiere llevar a cabo.
	3. Entorno: condiciones dentro de las cuales se presenta el estímulo.
	4. Artefacto: parte del sistema que recibe el estímulo.
	5. Respuesta: actividad que ocurre luego de la llegada del estímulo.
	6. Medida de la Respuesta: criterio para testear el requerimiento.
	7. Atributo de calidad afectado: Atributo de calidad relacionado con el escenario

Escenario de flexibilidad:
	
“El contratista desea hacer unas modificaciones en el sistema antes de su versión final”

	1. Fuente: Contratista
	2. Estímulo: Modificaciones en el proyecto
	3. Entorno: Sistema casi finalizado (aun en tiempo de diseño)
	4. Artefacto: Código
	5. Respuesta: Cambios realizados sin excesiva dificultad y sin efectos secundarios
	6. Medida de la Respuesta: Los cambios deben hacerse en el menor tiempo posible
	7. Atributo de calidad afectado: AT01

Escenario de Modificabilidad

El sistema debe estar abierto a la hora de realizar cambios en los algoritmos y métodos de los que se compone, sin perjudicar la funcionalidad que este ya posee.

	1. Fuente: agregación o actualización de un algoritmo
	2. Estímulo: cambio de versión del algoritmo
	3. Entorno: Explotación
	4. Artefacto: Sistema
	5. Respuesta: Actualización del algoritmo del sistema
	6. Medida de la Respuesta: numero de paquetes procesados con el nuevo algoritmo
	7. Atributo de calidad afectado: AT02

Escenario de Rendimiento

El sistema deberá facilitar un mínimo de información al mes, con la finalidad de que los usuarios no dejen de utilizar el portal por inanición. 

	1. Fuente: Actualización de la información
	2. Estímulo: Actividad en la pagina web
	3. Entorno: Explotación
	4. Artefacto: Pagina web
	5. Respuesta: Se incrementa el numero de visitas e interacción en la página 
	6. Medida de la Respuesta: numero de visitas a la pagina
	7. Atributo de calidad afectado: AT03

Escenario de Testabilidad

El sistema deberá facilitar la realización de pruebas sobre si los cálculos de los datos estadísticos realizados por los algoritmos son correctos, o de si la información obtenida es veraz.

	1. Fuente: Operaciones de pruebas
	2. Estímulo: Operaciones de comunicación de datos 
	3. Entorno: Explotación
	4. Artefacto: Pagina web y servidor
	5. Respuesta: log con los cálculos realizados sobre los datos
	6. Medida de la Respuesta: es posible trazar las operaciones relacionadas con los cálculos
	7. Atributo de calidad afectado: AT04

Escenario de Seguridad

El sistema deberá impedir, en la medida de todo lo posible , los fallos de seguridad como intrusos que puedan acceder a la pagina web haciéndose pasar por usuarios con determinados permisos dentro de esta, o el acceso a los datos, pudiendo modificarlos, borrarlos o extraerlos.

	1. Fuente: Acceso a la información privada o intrusión 
	2. Estímulo: Restringir acceso a datos 
	3. Entorno: Explotación
	4. Artefacto: Pagina web, servidor y base de datos
	5. Respuesta: Acceso mediante claves seguras
	6. Medida de la Respuesta: numero de intrusiones y acceso a datos de forma ilícita:0
	7. Atributo de calidad afectado: AT05

Escenario de Confiabilidad

La pagina web deberá proteger que los equipos de los usuarios queden infectados con virus al acceder a la pagina web, protegiéndolos de cross site scripting o que los datos descargables contengan algún tipo de software malicioso.

	1. Fuente: Equipos de los usuarios
	2. Estímulo: Acceso a la pagina o descarga de datos
	3. Entorno: Explotación
	4. Artefacto: Pagina web
	5. Respuesta: Aumento de la seguridad de la pagina web
	6. Medida de la Respuesta: numero de reportes sobre malware:0
	7. Atributo de calidad afectado: AT06

Escenario Time to market

Los desarrolladores deben implementar el sistema en el menor tiempo posible
 
	1. Fuente: Desarrolladores
	2. Estímulo: Implementación rápida del sistema
	3. Entorno: Sistema en desarrollo
	4. Artefacto: Código
	5. Respuesta: El sistema estará disponible en un margen de tiempo razonable
	6. Medida de la Respuesta: Cumplimiento del plazo establecido para sacar el producto
	7. Atributo de calidad afectado: AT07

Escenario de Adaptabilidad

La pagina web deberá ser visible desde cualquier tipo de explorador de internet que hay en el mercado.

	1. Fuente: Equipos de los usuarios
	2. Estímulo: Acceso a la pagina
	3. Entorno: Explotación
	4. Artefacto: Pagina web
	5. Respuesta: Debe visualizarse todo el contenido desde distintos exploradores
	6. Medida de la Respuesta: Debe estar probado en diferentes exploradores
	7. Atributo de calidad afectado: AT08

Escenario de Usabilidad:
	
“Usuarios novatos usan por primera vez el sistema”

	1. Fuente: Usuario
	2. Estímulo: Usar el sistema
	3. Entorno: Sistema finalizado y operativo
	4. Artefacto: Sistema
	5. Respuesta: El sistema presentará un estructura simple y fácil de utilizar
	6. Medida de la Respuesta: El usuario debe aprender a utilizar el sistema en el menor tiempo posible
	7. Atributo de calidad afectado: AT09

Escenario de Integridad:
	
“Usuarios no privilegiados intentan modificar la base de datos”

	1. Fuente: Usuarios no privilegiados
	2. Estímulo: Intentar modificar la base de datos
	3. Entorno: Sistema finalizado y operativo
	4. Artefacto: Base de datos
	5. Respuesta: El sistema negará dicha operación indicando el motivo
	6. Medida de la Respuesta: El usuario no debe de haber podido realizar los cambios que quería efectuar
	7. Atributo de calidad afectado: AT10

Escenario de Fiabilidad:
	
“Usuarios realizan cualquier operación (siempre que estén autorizados) del sistema”

	1. Fuente: Usuario
	2. Estímulo: Realizar una operación
	3. Entorno: Sistema finalizado y operativo
	4. Artefacto: Sistema
	5. Respuesta: El sistema realizará la operación de una manera rápida y sin fallos
	6. Medida de la Respuesta: El usuario no debe abandonar el sistema debido a un largo tiempo de espera
	7. Atributo de calidad afectado: AT11

Escenario de Disponibilidad:
	
El sistema deberá facilitar una alta disponibilidad, el portal será accesible el 90% del tiempo, en alguna de esas ocasiones la página no será visible y en otras el servicio será denegado al usuario, pidiéndole que trate de acceder más tarde.

	1. Fuente: Interacción de los usuarios
	2. Estímulo: Interación en la página
	3. Entorno: Explotación
	4. Artefacto: Sistema
	5. Respuesta: Visualización e interacción con el portal o denegación de servicio
	6. Medida de la Respuesta: Tratar de denegar el servicio del Sistema el menor tiempo posible.
	7. Atributo de calidad afectado: AT12

Escenario de Accesibilidad:
	
“Usuarios de diferentes países acceden al sistema los cuales deberán adaptar su idioma”

	1. Fuente: Usuario
	2. Estímulo: Establecer el idioma para el mayor número de países
	3. Entorno: Sistema finalizado y operativo
	4. Artefacto: Idioma del sistema
	5. Respuesta: Presentar el sistema al usuario con el idioma escogido
	6. Medida de la Respuesta: El cambio de idioma debe hacerse de forma correcta y sin afectar al propio funcionamiento
	7. Atributo de calidad afectado: AT13

Escenario de Escalabilidad

El sistema deberá diseñarse de forma que aunque en un inicio el número de usuarios sea bajo, si en un
periodo corto de tiempo aumentasen, la disponibilidad y rendimiento de este no se vea afectado.

	1. Fuente: incremento de usuarios
	2. Estímulo: gran número de peticiones de logeo o de datos
	3. Entorno: Explotación
	4. Artefacto: Servidor central, base de datos
	5. Respuesta: Se incrementa la capacidad de proceso del servidor y la base de datos
	6. Medida de la Respuesta: tiempo de logeo de los usuarios, número de peticiones denegadas:0
	7. Atributo de calidad afectado: Escalabilidad
