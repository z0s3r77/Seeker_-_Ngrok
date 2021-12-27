# Seeker y Ngrok

En esta entrada, explicaré como obtener la ubicación de cualquier dispositivo mediante un enlace. Cual Hacker de Pelicula.

( ESTA GUÍA es con fines educativos, hecha para ver como funcionan  "de manera sencilla"  este tipo de practicas)

La herramienta que usaremos será Seeker y es de Thewhiteh4t (https://github.com/thewhiteh4t/seeker). También usaremos Ngrok, que es un ejecutable unico y sin dependencias, que con una simple instrucción nos permite exponer hacia el exterior cualquier servicio web local que tengamos en nuestro ordenador, en cualquier puerto.  Podemos usar tanto HTTP como HTTPS.

Seeker, la usaremos para cargar la plantilla y para recoger los datos. Es decir, será como una especie de Apache.

### Instalación de Seeker

Para instalar Seeker tan solo debemos hacer:

      git clone https://github.com/thewhiteh4t/seeker
      
En la misma página de Thewhiteh4t aparece la guía para instalarlo. 

       git clone https://github.com/thewhiteh4t/seeker.git
       cd seeker/
       apt update 
       apt install python3 python3-pip php
       pip3 install requests
       
Nos quedará lo siguiente:

![imagen](https://user-images.githubusercontent.com/80277545/147465928-acac511f-b1b3-481e-95f2-16abcb742ae9.png)

### Instalación Ngrok 

Para instalar Ngrok, nos iremos a su página principal (https://dashboard.ngrok.com/get-started/setup). Tendremos que crearnos unas cuenta. A continuación ejecutaremos el siguiente comando para descargar el programa:

( ESTO LO PODEMOS HACER DENTRO DEL DIRECTORIO DE SEEKER)

      wget https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-linux-amd64.zip
      
 ![imagen](https://user-images.githubusercontent.com/80277545/147466317-c15ffc13-1122-4869-bafb-4c2a5ee8b7c4.png)

Descomprimiremos el archivo y eliminaremos el zip:

       sudo unzip ngrol-stable-linux-amd64.zip
       sudo rm ngrok-stable-linux-amd64.zip
     
![imagen](https://user-images.githubusercontent.com/80277545/147466452-b043e321-6ffb-4510-9418-da2c1b3079ed.png)

Ahora, tendremos que conectar nuestra cuenta de Ngrok a la aplicación "ngrok" que se nos ha creado en el directorio Seeker. En la pagina de ngrok (https://dashboard.ngrok.com/get-started/setup) , debemos tomar nuestro token (identificador) de la cuenta. Ejecutaremos el comando que nos sale:

![imagen](https://user-images.githubusercontent.com/80277545/147466704-4ced354f-ab56-438f-a23f-cca99d30de63.png)

![imagen](https://user-images.githubusercontent.com/80277545/147466776-5ea65e5b-1809-4e5d-96f7-a3b554b5a11a.png)

# Iniciando "Ataque"

Lo primero que haremos es iniciar Seeker:

En el directorio de Seeker, ejecutaremos lo siguiente:

      sudo python3 seeker.py -t manual -p 80 

Seleccionaremos la primera opción, NearYou, para agilizar la practica:

       0
 
 ![imagen](https://user-images.githubusercontent.com/80277545/147467077-9722928d-398f-413a-8103-b0a660761379.png)

Ahora iniciaremos Ngrok, para publicar el puerto 80 que hemos levatado y que la victima se pueda conectar a nuestra página malisiosa. En el mismo directorio donde está el ejecutable "ngrok":

      sudo ./ngrok http 80

![imagen](https://user-images.githubusercontent.com/80277545/147467324-1b478df1-c279-4633-b504-4e213bb7cfaf.png)

Se nos abrirá la siguiente interfaz:

![imagen](https://user-images.githubusercontent.com/80277545/147467589-28774ab8-1bb7-4d52-a6df-bcee08ac0cf1.png)

      En caso de no salirnos el apartado "Account" con nuestro correo electronico, hay que volver a ejecutar el comando de autenticación de la cuenta. sudo ./ngrok TOKEN. 

Ahora, desde nuestro movil pondremos la URL que nos saldrá, en mi caso usaré:

      http://9e06-67-218-241-229.ngork.io

En el movil nos saldrá lo siguiente y tendremos que seguir los pasos que nos dice "COMO SI NO SUPIERAMOS NADA". 

Esto es lo que nos saldría:
Inicio:
![Inicio](https://user-images.githubusercontent.com/80277545/147468027-4c7474b4-5f35-4141-b14d-3583a2936b12.jpeg)
Autorización:
![Autorizacion-gps](https://user-images.githubusercontent.com/80277545/147468047-b00beac4-d7b0-49b6-be5a-17a21eb4d11e.jpeg)
Finalización:
![Finalizado](https://user-images.githubusercontent.com/80277545/147468064-74aa4c18-bd43-4437-91fc-3656f7f469bd.jpeg)

Una vez finalizado esto, por una parte,Ngrok nos irá mostrando lo que hace el usuario:

![imagen](https://user-images.githubusercontent.com/80277545/147468159-dd8d0b00-e4a1-4216-ad50-e2d75dcc8655.png)

Por otro lado, Seeker nos dará toda la información que ha recabado, inclusive una dirección de google Maps:

![imagen](https://user-images.githubusercontent.com/80277545/147468310-24d717c5-c123-4687-8902-f5a9c67b8599.png)

Este sería el resultado final:

![imagen](https://user-images.githubusercontent.com/80277545/147468374-7c4312bc-48d0-43ac-8c53-dda4065a6380.png)

# Conlusión

Como hemos visto, Seeker, nos ayuda a recoger toda esa información sensible de la victima con tan solo unos pasos. Por otro lado, Ngrok, es un exelente programa para hacer "experimentos" y compartir nuestros "VIRUS" (broma) con nuestros compañeros. Siempre en un entorno controlado. 

Con esto también espero que haya sido más "palpable" el hecho de ver como un atacante puede acceder a nuestros datos. De ahí la importancia de tener bloqueadores de restreo y Addwares de páginas Web. Yo recomiendo usar el complemento "Adguard" de firefox. 

Espero que haya sido de ayuda e interesante. 

#### Para cualquier consulta: z0s3r77@gmail.com






