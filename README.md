Instalación de Pip, Python y Virtualenv en un sistema Debian Wheezy recién instalado.
========================================================================

El desarrollo de este tutorial se va a dividir en tres partes, las cuales se clasifican en: 

 - **Parte 1:** Instalación de gestor de paquetes PIP.
 - **Parte 2:** Instalación de versiones de Python diferentes a las que viene por defecto 
 - **Parte3:** Instalación del Virtualenv.
 
 

Instalación del gestor de paquetes PIP
--------------------------------------

**Paso 1:** Ingresar a la terminal en modo root (de esta manera podremos ejecutar cualquier comando sin ningún inconveniente) para actualizar la lista de paquetes del repositorio y para instalar algunas librerías importantes para el entorno Python.

    sudo apt-get update 
    sudo apt-get install build-essential checkinstall
    sudo apt-get install libreadline-gplv2-dev libncursesw5-dev 
    sudo apt-get install libssl-dev libsqlite3-dev tk-dev libgdbm-dev 
    sudo apt-get install libc6-dev libbz2-dev zlib1g-dev

**Paso 2:** Ingresar a la siguiente dirección [https://pip.pypa.io/en/stable/installing/](https://pip.pypa.io/en/stable/installing/) y descargar el archivo get-pip.py; para hacer esto, dentro de la terminal cambiamos al directorio de descargas y utilizamos el comando wget link-archivo-get-pip.py

    cd /home/usuario/Descargas
    wget https://bootstrap.pypa.io/get-pip.py

**Paso 3:** Ejecutar el siguiente comando:

    python get-pip.py

**Paso 4:** Se comprueba que PIP se hayaa instalado correctamente con el siguiente comando:

    pip –V

[Ver video](https://www.youtube.com/watch?v=aGXpt34ZKgA&index=1&list=PLqDwl4H6rH9MLqHdoYe-vQg5F_f2aV8LT)


Instalación de versiones de Python diferentes a las que viene por defecto.
------------------------------------------------------------------------

Por defecto, Debian viene instalada con la versión 2.7 de Python. Si se requiere tener instalada una versión diferente, se debe seguir los siguientes pasos:

**Paso 1:** Ingresar a la página oficial de [Python](https://www.python.org/downloads/)  y buscar la versión que se desea. 

**Paso 2:** Una vez seleccionada la versión de Python, se procede a descargar con el comando wget link-version-python.

    wget https://www.python.org/ftp/python/3.4.7/Python-3.4.7.tgz

**Paso 3:** Descomprimir el archivo recién descargado con el siguiente comando: 

	

    tar xfz Python-3.4.7.tgz

**Paso 4:** Cambiar al directorio recién creado.

    cd  Python-3.4.7

**Paso 5:** Dentro del directorio se ejecuta el archivo configure

    ./configure

**Paso 6:** Una vez que el proceso de configuración ha terminado, se ejecuta el siguiente comando: 

    make altinstall

**Paso 7:** Para comprobar que se ha instalado correctamente la versión de Python, se ejecuta:

	

    /usr/local/bin/python3.4 –V

El resultado del anterior comando debe ser: Python 3.4.7 o la versión que se ha elegido.

[Ver video](https://www.youtube.com/watch?v=yifzdsPP2eI&list=PLqDwl4H6rH9MLqHdoYe-vQg5F_f2aV8LT&index=2)

Instalación del Virtualenv
--------------------------

Para instalar el virtualenv, simplemente hacemos uso del siguiente comando:

    pip install virtualenv

Si se quiere crear un nuevo entorno virtual con la versión de Python que se creó en la parte 2 de este tutorial, simplemente se debe especificar la ruta a esa versión:

	

  

     virtualenv –p /usr/local/bin/python3.4 nombre_entorno_virtual

Cuando el entorno se ha creado, lo activamos y comprobamos la versión de Python y de PIP

	

    cd nombre_entorno_virtual
    source bin/actívate
    python –V
    pip –V
	
De esta manera podemos instalar diferentes versiones de Python y crear varios entornos virtuales con esas versiones. 

[Ver video](https://www.youtube.com/watch?v=n8gHfw-IzUo&list=PLqDwl4H6rH9MLqHdoYe-vQg5F_f2aV8LT&index=3)









