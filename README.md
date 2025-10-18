# tp-6
Diseño de Software 3 - Trabajo practico 6- Gestion Estudiantes 

1.Crear un directorio donde se creara el entorno virtual, posicionarse en el directorio ejecutar: python -m venv nombre_del_entorno (se sugiere que tenga el mismo nombre que el proyecto)... 
2.A continuacion activar el entorno virtual ejecutando: nombre_del_entorno\Scripts\activate
3. Instalar setuptools con: pip install setuptools
4. Instalar django con: pip install django

Finalizadas las instalaciones, volvemos al directorio raiz y creamos un proyecto de django

Ejecutar: django-admin startproject nombre_del_proyecto

No olvidar hacer un .gitignore 
Contenido sugerido:
venv/
env/
entorno_virtual/  (el nombre que tenga tu entorno vitual)
*/__pycache__/
*.py[cod]

# Base de datos local
*.sqlite3

# Configuración sensible
.env

# Archivos del sistema
.DS_Store
Thumbs.db

# Configuración del IDE
.idea/
.vscode/

# Archivos de migraciones (opcional)
*/migrations/__pycache__/

# BASE DE DATOS-- 
 Instalar el conector de PostgreSQL en tu entorno virtual

Abrí la terminal de PyCharm (asegurate de tener activado tu entorno virtual) y ejecutá:

pip install psycopg2-binary


Este paquete es el driver que Django usa para conectarse con PostgreSQL. 

Configurar la base de datos en sttings.py 
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'gestor_estudiantes_db',  # nombre de la base que creaste
        'USER': 'postgres',               # tu usuario de PostgreSQL
        'PASSWORD': 'contraseña',      # la contraseña que usás en pgAdmin
        'HOST': 'localhost',              # servidor local
        'PORT': '5432',                   # puerto por defecto de PostgreSQL
    }
}
para mandar la info se hace python manage.py migrate
 # PARA GUARDAR LOS REQUERIMIENTOS 
 pip freeze
y cuando clonamos hacemos pip install -r requirements.txt
# DESACOPLAR LAS VARIABLES
pip install python-decouple 
agregar a los requerimientos
 en settings.py importar: from decouple import config
Y HACER LAS CONEXIONES ENTRE EL ENV Y EL SETTINGS.PY 
# correr el servidor 
python manage.py runserver

# CREAR UNA APP
Ejecutar: python manage.py startapp nombre_app

 
 
