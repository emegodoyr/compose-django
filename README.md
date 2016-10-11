**Compose para levantar django con mysql**

Recordar que la variable `DATABASES` debe quedar asi

``` 
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql', 
        'NAME': 'django',
        'USER': 'admin',
        'PASSWORD': 'mypass',
        'HOST': 'mysql',
        'PORT': '3306',
    }
}
```


primero debemos hacer un build de la imagen de django con:

`docker-compose build --no-cache`

una vez finalizado el build, debemos crear un proyecto en django con el siguiente comando:

`docker-compose run django django-admin.py startproject NombreProyecto .`


si ya tenemos el proyecto creado desde antes, copiarlo a la raiz de este repositorio, en una
carpeta que se llame `app`, esta es la carpeta que se mapea en el compose.


una vez creado o copiado el proeycto dentro de la carpeta `app` podremos ejecutar el siguiente
comando para ver en el puerto `8000` de nuestro servidor local la vista de que django esta corriendo

`docker-compose up -d`

