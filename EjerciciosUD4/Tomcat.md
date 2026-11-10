## INTRODUCCIÓN
### Catalina:
Catalina es el motor contenedor de servlets y JSP (JavaServer Pages), tecnologías web basadas en Java. Procesa y ejecuta los servlets y páginas JSP, se encarga del ciclo de vida de los componentes web
y gestiona la seguridad estándar definida para los contenedores y procesa credenciales. Un servlet es una clase de Java que se ejecuta dentro de un servidor web o de aplicaciones para gestionar
peticiones HTTP
### Coyote
Coyote es el componente conector encargado de gestionar la comunicación de red escuchando las conexiones entrantes de los clientes en puertos TCP específicos.
Traduce y maneja protocolos web estándar, principalmente HTTP y AJP. Analiza la petición y los encabezados HTTP y reenvía la solicitud a Catalina para que
ejecute la lógica de Java y devuelva la respuesta. Es gracias a esto que Tomcat funciona como un servidor.
### Jasper
Como Catalina solo puede leer servlets, y para que los archivos se traduzcan a servlets de Java está Jasper ya que se encarga de leer el archivo .jsp y
convertirlo en código fuente Java, después compila ese archivo Java en código de bytes (.class)
para que Catalina pueda procesarlo y devolver la respuesta al cliente. Necesita un server en común puesto que es el intermediario del cliente y de la base de datos.
### Manager
El Manager es la herramienta encargada de administrar el ciclo de vida de las aplicaciones web desplegadas (archivos .war o carpetas) dentro de la instancia de Tomcat.
Instala y subir nuevas aplicaciones web en caliente las cuales se pueden encender, reiniciar o apagar sin tener que apagar otras páginas. También las puede monitorear y eliminar.
### Host Manager
El Host Manager es la aplicación administrativa diseñada para gestionar los Virtual Hosts de Tomcat, tiene la capacidad de alojar múltiples dominios o sitios web independientes
dentro de una misma instancia del servidor. Crea Virtual Hosts añadiendo nuevos dominios o nombres de host al archivo de configuración server.xml de forma dinámic.
Elimina Hosts, es decir, da de baja hosts existentes.
Y gestiona alias, asocia alias o nombres alternativos de DNS a un host virtual.

### Estructura de datos
Localizado en Catalina_Home, podemos encontrar el bin, conf, webapps, lib, logs
Bin:  Contiene los scripts de inicio y parada del servidor.
Conf:  Almacena los archivos de configuración global del servidor.
Webapps: Es el directorio de despliegue donde se colocan las aplicaciones web.
lib: Guarda las librerías de archivos JAR compartidas y utilizadas por el propio motor de Tomcat.
logs: 
