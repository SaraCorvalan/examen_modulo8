# examen_modulo8
Requisitos previos
Antes de comenzar, asegúrate de tener instalado lo siguiente en tu sistema:

Python: Django está construido sobre Python, así que necesitas tenerlo instalado. Puedes descargar Python desde python.org.

Pip: Pip es un administrador de paquetes para Python. Es necesario para instalar Django y otras dependencias. La mayoría de las instalaciones de Python incluyen Pip, pero si no lo tienes, puedes encontrar instrucciones de instalación en la documentación oficial.

PostgreSQL: Necesitas tener PostgreSQL instalado y configurado en tu sistema. Puedes descargarlo desde postgresql.org.

Configuración del Ambiente Virtual
Para mantener las dependencias de tu proyecto aisladas, usaremos un ambiente virtual. Sigue estos pasos para configurarlo:

Abre una terminal o línea de comandos.

Navega al directorio de tu proyecto usando cd.

Crea un nuevo ambiente virtual ejecutando el siguiente comando:

bash
Copy code
python -m venv venv
Activa el ambiente virtual:

En Windows:

bash
Copy code
venv\Scripts\activate
En macOS y Linux:

bash
Copy code
source venv/bin/activate
Ahora estás dentro del ambiente virtual, y cualquier instalación de paquetes de Python se hará solo en este ambiente.

Instalación de Django y PostgreSQL
Instala Django ejecutando el siguiente comando:

bash
Copy code
pip install django
Instala la biblioteca de PostgreSQL para Django:

bash
Copy code
pip install psycopg2
Configuración de la Base de Datos
Abre el archivo settings.py en la carpeta del proyecto y encuentra la sección DATABASES. Cambia la configuración para que coincida con tu base de datos PostgreSQL:

python
Copy code
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'nombre_de_tu_base_de_datos',
        'USER': 'tu_usuario_de_postgres',
        'PASSWORD': 'tu_contraseña_de_postgres',
        'HOST': 'localhost',  # Puedes cambiarlo si tu base de datos está en otro lugar
        'PORT': '',           # Puedes especificar un puerto si es necesario
    }
}
Ejecuta las migraciones para crear las tablas en la base de datos:

bash
Copy code
python manage.py migrate
Ejecutar el Proyecto
Ejecuta el servidor de desarrollo de Django:

bash
Copy code
python manage.py runserver
Abre tu navegador y ve a http://localhost:8000/ para ver tu aplicación en funcionamiento.






