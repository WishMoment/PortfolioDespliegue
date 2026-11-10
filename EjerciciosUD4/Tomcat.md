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
logs: Almacena los archivos de registro y trazas del servidor.
temp: Espacio temporal donde Tomcat guarda archivos de trabajo mientras se encuentra en ejecución.

### Flujo interno de funcionamiento
#### Recepción de la petición
  El navegador envía una petición HTTP al servidor. Coyote la recibe a través del puerto configurado.
#### Procesamiento mediante los contenedores
  Coyote entrega la petición a Catalina, que la dirige a través de su jerarquía de contenedores.
#### Ejecución de la aplicación
  El servlet correspondiente procesa la petición y genera una respuesta. Si se solicita una página JSP, Jasper se encarga de transformarla y compilarla como servlet.
#### Envío de la respuesta
  Catalina devuelve el resultado a Coyote, que se encarga de enviarlo al navegador mediante HTTP.
### Despliegue de aplicaciones
Tomcat permite instalar aplicaciones web mediante archivos .war o directorios que contienen sus archivos. Normalmente, al colocar un archivo .war en webapps, Tomcat puede desplegarlo automáticamente, extrayendo su contenido y preparándolo para recibir peticiones.

## Ubicación
Catalina, Coyote y Jasper se encuentran en la carpeta de lib mientras que los manager tienen sus propias carpetas.
## Instalar tomcat
Buscamos con el apt search tomcat qué versiones de tomcat hay.
Como a mi me sale la versión 10 instalamos la versión 10.
La instalamos con sudo apt install tomcat 10
### Archivos server.xml, web.xml, tomcat-users.xml y context.xml
Los archivos se encuentran en etc/tomcat10

### Función elementos

1. server.xml

Es el archivo de configuración principal de Tomcat. Define la estructura y el funcionamiento general del servidor.

Se pueden configurar:
- Server: configuración general y ciclo de vida del servidor.
- Service: agrupa los conectores y el motor que procesan las peticiones.
- Connector: puertos y protocolos de comunicación, como HTTP y HTTPS.
- Engine: motor que procesa las peticiones recibidas.
- Host: configuración de los hosts virtuales o dominios.
- Context: configuración de las aplicaciones web.

2. web.xml

Es el archivo de configuración global de las aplicaciones web de Tomcat. Establece parámetros y comportamientos predeterminados que pueden aplicarse a todas las aplicaciones desplegadas.

Se pueden configurar:
- Servlets y sus asignaciones de URL.
- Tipos MIME para identificar los formatos de los archivos.
- Páginas de bienvenida (welcome files).
- Páginas de error personalizadas.
- Configuración de sesiones.
- Filtros para procesar las peticiones y respuestas.

3. tomcat-users.xml

Es el archivo encargado de definir los usuarios, contraseñas y roles que pueden acceder a determinadas funciones de administración de Tomcat.

Se pueden configurar:
- Usuarios y sus nombres.
- Contraseñas de acceso.
- Roles o permisos asignados a cada usuario.

4. conf/context.xml

Es el archivo que contiene la configuración predeterminada de los contextos de las aplicaciones web. Permite establecer opciones que afectan al comportamiento de las aplicaciones desplegadas.

Se pueden configurar:
- Gestión de sesiones y cookies.
- Recursos externos, como conexiones a bases de datos mediante JNDI.
- Recarga automática de aplicaciones.
- Recursos y archivos que deben supervisarse para detectar cambios.
