
sudo a2enmod proxy
sudo a2enmod proxy_http

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD4/4_11.png)

sudo nano /etc/apache2/sites-available/000-default.conf
sudo nano /etc/apache2/sites-available/default.ssl.conf

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD4/4_13.png)

ProxyPreserveHost On
ProxyPass /hola/ http://localhost:8080/hola/
ProxyPassReverse /hola/ http://localhost:8080/hola/

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD4/4_14.png)

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD4/4_16.png)

![](https://github.com/WishMoment/PortfolioDespliegue/blob/main/EjerciciosUD4/4_15.png)



Instala Apache en tu máquina virtual, si no está ya instalado.
Configura un conector AJP o un reverse proxy hacia Tomcat.
Verifica que la aplicación web responde a través del servidor web.
Documenta los pasos realizados
