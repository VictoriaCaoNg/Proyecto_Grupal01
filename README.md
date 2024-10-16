## Tabla de clasificación
En el ámbito de los videojuegos multijugador en tiempo real es común que los jugadores deseen comparar su rendimiento con respecto al de otros, una forma de lograrlo es mediante la revisión de su posición en una tabla de clasificación. Para lograr afrontar el objetivo de este reto se requiere implementar una solución que permita mantener el orden de los jugadores por sus puntuaciones y mostrar las posiciones (rankings) de manera rápida, eficiente y actualizada al instante a manera de tabla de clasificación en tiempo real. Por lo que se utilizarán bases de datos no relacionales del tipo key-value mediante los softwares Redis y Memcached, lo cual permitiría que la información sea accesible rápidamente, precisa y, a su vez, mejorar la experiencia competitiva en el juego.

## Guía de instalación
# Redis
1. Ingresar a la página web de Redis en https://redis.io/es/
2. Estaremos usando la versión gratuita por lo que seleccionaremos la opción de Probar Gratis
3. Crear usuario y una vez dentro crear una base de datos
4. Darle click a la base de datos creada y una vez dentro darle al botón Connect, donde se abrirá una pestaña
5. En la pestaña darle a la opción RedisInsight e instalar la aplicación. Una vez instalada la aplicación darle click a la opción Open with Redis Insight
6. En la misma pestaña seleccionar la opción Redis Client y escoger el lengiaje a utilizar para vincularlo con Redis, en este caso usaremos Python
7. Copiar el código que Redis le brina y pegarlo en cualquier entorno en que se pueda utilizar Python.
8. Instalar el paquete de redis con pip install redis

# Memcached
1. En el caso de tener un sistema operativo Windows, se debe instalar un subsistema de Linux. Pueden seguir los pasos en este video https://www.youtube.com/watch?v=hjRJ-CZNUmw
2. Una vez instalado Linux, en la terminal de Linux escribir apt install memcached libmemcached-tools -y
3. Para comprobar que todo se instaló bien escribir systemctl status memcached en la terminal. Deberá aparecerles Apr 10 19:48:33 memcached systemd[1]: Started memcached daemon al final.
4. Instalar el paquete pymemcache en Python con pip intall pymemcache
5. Conectarlo a la terminal con mc = memcache.Client(['XXXX'], debug=0), donde XXX es el IP Linux de la computadora y la terminal en donde Memcached está conectada (usualmente 11211)
   
