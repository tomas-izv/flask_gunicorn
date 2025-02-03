# Despliegue

- Comprobamos que está instalado correctamente mostrando su versión.
Crear el directorio en el que se almacena el proyecto <b>trobmor</b> y darle sus privilegios correspondientes.

<img src="/conf_project/imgs/img.png" alt="Primer Resultado"></img>

- Crear un archivo oculto dentro del directorio con <b>variables de entorno necesarias</b>

<img src="/conf_project/imgs/img1.png" alt="Segundo Resultado"></img>

- Iniciamos ahora nuestro entorno virtual. Pipenv cargará las variables de entorno desde el fichero .env de forma automática.

<img src="/conf_project/imgs/img2.png" alt="Tercero Resultado"></img>

- Instalar las dependencias necesarias para nuestro proyecto.

<img src="/conf_project/imgs/img3.png" alt="Cuarto Resultado"></img>

- Crear y editar un archivo <a href="./conf_project/application.py"><b>application.py</b></a>

<img src="/conf_project/imgs/img4.png" alt="Quinto Resultado"></img>

- Crear y editar un archivo <a href="./conf_project/wsgi.py"><b>wsgi.py</b></a>

<img src="/conf_project/imgs/img5.png" alt="Sexto Resultado"></img>

- Despliegue con el servidor web integrado de Flask.

<img src="/conf_project/imgs/img6.png" alt="Septimo Resultado"></img>
<img src="/conf_project/imgs/img7.png" alt="Septimo Resultado"></img>

- Ruta desde la que se ejecuta <b>gunicorn</b> para poder configurar más adelante un servicio del sistema.

<img src="/conf_project/imgs/img8.png" alt="Noveno Resultado"></img>

- Crear y editar un archivo <a href="./conf_project/flask_app.service"><b>flask_app.service</b></a>

<img src="/conf_project/imgs/img9.png" alt="Decimo Resultado"></img>

- Crear y editar un archivo <a href="./conf_project/trobmor.conf"><b>trobmor.conf</b></a>

<img src="/conf_project/imgs/img10.png" alt="Once Resultado"></img>

- Nos aseguramos de que se ha creado dicho link simbólico, que la configuración de Nginx no contiene errores, reiniciamos Nginx y comprobamos que se estado es activo

<img src="/conf_project/imgs/img11.png" alt="Doce Resultado"></img>

- Despliegue servida por <b>Gunicorn y Nginx</b>.

<img src="/conf_project/imgs/img12.png" alt="Trece Resultado"></img>

# Ampliacion

- Darle sus privilegios correspondientes.

<img src="/conf_project/imgs/image1.png" alt="Catorce Resultado"></img>

- Crear un archivo oculto dentro del directorio con <b>variables de entorno necesarias</b>

<img src="/conf_project/imgs/image2.png" alt="Quince Resultado"></img>

- Iniciamos ahora nuestro entorno virtual. Pipenv cargará las variables de entorno desde el fichero .env de forma automática.

<img src="/conf_project/imgs/image3.png" alt="Dieciseis Resultado"></img>

- Y, tras activar el entorno virtual dentro del directorio del repositorio clonado, para instalar las dependencias del proyecto de la aplicación deberás hacer:

<img src="/conf_project/imgs/image4.png" alt="Diecisiete Resultado"></img>

- Y un último detalle, Gunicorn debe iniciarse ahora así:

<img src="/conf_project/imgs/image5.png" alt="Dieciocho Resultado"></img>

- Despliegue

<img src="/conf_project/imgs/image6.png" alt="Diecinueve Resultado"></img>

<img src="/conf_project/imgs/image7.png" alt="Veinte Resultado"></img>