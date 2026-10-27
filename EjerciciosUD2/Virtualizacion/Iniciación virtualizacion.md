## INICIACIÓN DE LA VIRTUALIZACIÓN
### INSTALACIÓN DE LA MÁQUINA VIRTUAL
Primero, descargamos la ISO de Ubuntu

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD2/Virtualizacion/Iniciaci%C3%B3n%20virtualizaci%C3%B3n/2026-10-27_17-10.png)

Después creamos la máquina virtual

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD2/Virtualizacion/Iniciaci%C3%B3n%20virtualizaci%C3%B3n/2026-10-27_17-11.png)

Y empezamos a configurar la máquina virtual antes de ejecutarla

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD2/Virtualizacion/Iniciaci%C3%B3n%20virtualizaci%C3%B3n/2026-10-27_17-11_1.png)

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD2/Virtualizacion/Iniciaci%C3%B3n%20virtualizaci%C3%B3n/2026-10-27_17-11(2).png)

Y por fin podemos ejecutar la máquina

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD2/Virtualizacion/Iniciaci%C3%B3n%20virtualizaci%C3%B3n/2026-10-27_17-11(3).png)

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD2/Virtualizacion/Iniciaci%C3%B3n%20virtualizaci%C3%B3n/2026-10-27_17-12.png)

### INSTALACIÓN DE DOCKER EN UBUNTU
Para poder instalar docker, hay que empezar con revisar que todo esté actualizado y al día.

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD2/Virtualizacion/Iniciaci%C3%B3n%20virtualizaci%C3%B3n/2026-10-27_17-12_1.png)

Después instalamos los certificados que servirán para que comprueben que todo lo que instalamos es completamente seguro y son archivos originales.

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD2/Virtualizacion/Iniciaci%C3%B3n%20virtualizaci%C3%B3n/2026-10-27_17-12(2).png)

Revisamos que Docker es seguro, lo añadimos al repositorio y lo instalamos

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD2/Virtualizacion/Iniciaci%C3%B3n%20virtualizaci%C3%B3n/2026-10-27_17-13.png)

Como el proporcionado por los archivos está des actualizado usaremos el que encontró Juan Ángel

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD2/Virtualizacion/Iniciaci%C3%B3n%20virtualizaci%C3%B3n/2026-10-27_17-13_1.png)

Terminamos de descargar

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD2/Virtualizacion/Iniciaci%C3%B3n%20virtualizaci%C3%B3n/2026-10-27_17-14.png)

Para comprobar que Docker se ha instalado como debe, vamos a hacer que ejecute un hola mundo

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD2/Virtualizacion/Iniciaci%C3%B3n%20virtualizaci%C3%B3n/2026-10-27_17-14(1).png)

### INSTALACIÓN IMÁGENES EN DOCKER

Sabemos que imágenes vamos a descargar, que son el nginx y el tomcat
Primero de todo, vamos a buscar las imágenes

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD2/Virtualizacion/Iniciaci%C3%B3n%20virtualizaci%C3%B3n/2026-10-27_17-14(2).png)

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD2/Virtualizacion/Iniciaci%C3%B3n%20virtualizaci%C3%B3n/2026-10-27_17-14(3).png)

Después de revisar que lo hemos escrito bien y que los contenedores existen, vamos a empezar con la instalación de los mismos

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD2/Virtualizacion/Iniciaci%C3%B3n%20virtualizaci%C3%B3n/2026-10-27_17-15.png)

Y para comprobar que están bien instalados, podemos ir a las páginas en concreto de cada navegador, si funciona, nos mostrará información

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD2/Virtualizacion/Iniciaci%C3%B3n%20virtualizaci%C3%B3n/2026-10-27_17-15_1.png)

Aunque parece que Tomcat dió error, en realidad está funcionando, solo no llegó a cargar la página web
