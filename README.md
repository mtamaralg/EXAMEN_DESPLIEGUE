# EXAMEN_DESPLIEGUE

Capturas de Pantalla

Borrado de todas las instancias que habia:
<img width="1920" height="1080" alt="BorradoDeInstancias" src="https://github.com/user-attachments/assets/5f10b808-86e9-47f4-ac27-7fd5337aa3a0" />

Ip Publicas liberadas:
<img width="1920" height="1080" alt="IpPublicaLiberadas" src="https://github.com/user-attachments/assets/d866f9ba-fcb9-4f43-a5df-a916f59b4ce3" />

Ahora lanzamos una instancia nueva:

Primero escribimos el nombre y seleccionamos ubuntu:
<img width="1920" height="1080" alt="PrimeraCapInstancia" src="https://github.com/user-attachments/assets/b64e1432-910a-4be0-94ce-25c9df1f210b" />

Despues en tipo de instancia seloeccionamos t2.medium: 
<img width="1920" height="1080" alt="SegundaCapInstancia" src="https://github.com/user-attachments/assets/3df46fe9-7a5f-479a-b65e-2c9397dbac51" />

Despues en par de claves seleccionamos vockey:
<img width="1920" height="1080" alt="TerceraCapInstancia" src="https://github.com/user-attachments/assets/d0844744-53a9-4dcc-84f0-7190360675db" />

Por ultimo configuramos la red permitiendo todos los traficos y aumentando el almacenamiento a 20 GiB:
<img width="1920" height="1080" alt="CuartaCap Instancias" src="https://github.com/user-attachments/assets/de861e26-b6b7-486f-8236-a5741944c933" />

Y ya hemos lanzado la nueva instancia:
<img width="1920" height="1080" alt="QuintaCapInstancias" src="https://github.com/user-attachments/assets/2a05cce5-bed9-43b3-9733-b3920eecb9ae" />

Asi comprobamos que ya este inicializada o ejecutandose:
<img width="1920" height="1080" alt="SextaCapInstancias" src="https://github.com/user-attachments/assets/2916551e-a70a-471d-aeeb-08a1dcdc3ddb" />


Ahora vamos a asociarle una ip Elastica: 

Primero pinchamos donde pone "Direcciones ip Elasticas":
<img width="1920" height="1080" alt="PrimeraCapIPPublica" src="https://github.com/user-attachments/assets/6a93a82f-83d1-48ba-8e21-a3308ebb2e73" />

Ahora le damos a "asignar direccion ip elastica":
<img width="1920" height="1080" alt="SegundaCapIPPublica" src="https://github.com/user-attachments/assets/1bacab14-9c42-4fe2-bdf5-6c898c5983e1" />

Pulsamos el boton de asignar: 
<img width="1920" height="1080" alt="TerceraCapIPPublica" src="https://github.com/user-attachments/assets/e559d6bd-6041-40bf-9e3d-88cb2b200c63" />

Y nos arriba nos sale un mensajito en verde: 
<img width="1920" height="1080" alt="CuartaCapIPPublica" src="https://github.com/user-attachments/assets/80b50d70-d0f3-4b99-af0f-4b96ac02a30b" />

Lo pulsamos para asociar la ip elastica y a su vez señalamos la instancia que hemos creado:
<img width="1920" height="1080" alt="QuintaCapIPPublica" src="https://github.com/user-attachments/assets/5133f6bc-31b7-4315-8cae-a26225c92d93" />

Pulsamos el boton de asociar y ariiba nos saldra un mensajito en verde diciendo que se ha asociado correctamente:
<img width="1920" height="1080" alt="SextaCapIPPublica" src="https://github.com/user-attachments/assets/c362f851-7ccb-41b8-9425-a3f47f8c07e2" />


Ahora para poder abrir por conexion remota en el visual studio debemos hacer unos ajustes:

Empezamos volviendo a la pagina de lanzamiento del laboratorio y buscando el botoncito donde pone AWS details: 
<img width="1920" height="1080" alt="PrimeraCapAjustes" src="https://github.com/user-attachments/assets/9ba6920f-7a3a-4a4e-a6a4-f17f0f88ef81" />

Si pulsamos nos apareceran archivos para descargar y nosotros vamos a descargar el archivo .pem:
<img width="1920" height="1080" alt="SegundaCapAjustes" src="https://github.com/user-attachments/assets/e2bee74f-99d7-465c-9bd9-3d4b32526d80" />


Ahora vamos a pasar a usar el VS:

Primero para que podamos acceder de forma remota debemos tener esto escrito: 
<img width="1920" height="1080" alt="1VS" src="https://github.com/user-attachments/assets/741a033a-0133-455a-b72c-dfc3975e0d02" />

Ahora creamos una carpeta que por defecto nos saldra con estos archivos:
<img width="1920" height="1080" alt="2VS" src="https://github.com/user-attachments/assets/2b92c194-aa42-4bcb-abc7-91172a5f3aeb" />

Ahora vamos a nuestro git y copiamos este enlace https://github.com/mtamaralg/EXAMEN_DESPLIEGUE.git: 
<img width="1920" height="1080" alt="3VS" src="https://github.com/user-attachments/assets/7c72eb6f-d481-4624-83ce-92b3f7c2263f" />

Hacemos un git clone https://github.com/mtamaralg/EXAMEN_DESPLIEGUE.git y asi ya tenemos la carpeta en la que vamos a trabajar:
<img width="1920" height="1080" alt="4vs" src="https://github.com/user-attachments/assets/2eed6a80-1e85-4b88-9bef-384482889088" />

Lo primero que vamos a hacer es añadir estas carpetas ya que trabajaremos con ellas: conf/ thaccess/ php/ scripts/ 
<img width="1920" height="1080" alt="5VS" src="https://github.com/user-attachments/assets/0bba5b3a-58e3-4d2a-ad4c-6cb6ac637770" />

En la carpeta conf/ crearemos un archivo llamado 000-default.conf con este codigo de aqui 
 <VirtualHost *:80>
   # ServerName PUT_YOUR_CERTBOT_DOMAIN_HERE
    ServerAdmin webmaster@localhost
    DocumentRoot /var/www/html/

    DirectoryIndex index.php index.html
    <Directory /var/www/html>
        AllowOverride All
    </Directory>
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>

<img width="1920" height="1080" alt="6VS" src="https://github.com/user-attachments/assets/129a216a-93c0-4e70-a106-7d56b70a4d8d" />

Ahora en el archivo htaccess/ crearemos un archivo .htaccess en el que pondremos este codigo de aqui: 
<IfModule mod_rewrite.c>
RewriteEngine On
RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]
RewriteBase /
RewriteRule ^index\.php$ - [L]
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule . /index.php [L]
</IfModule>

<img width="1920" height="1080" alt="7VS" src="https://github.com/user-attachments/assets/1d8ba5df-5056-4321-aaff-2152f08a53b1" />

Ahora en la carpeta php/ creamos un archivo llamado index.php y escribimos este codigo de aqui:
<?php
phpinfo();
?>
<img width="1920" height="1080" alt="8VS" src="https://github.com/user-attachments/assets/88c64d31-a12e-43aa-aa00-3e9a4e092bd2" />

Segun lo que nos pide en el enunciado vamos a crear estas carpetas en la carpeta scripts/ :
<img width="1920" height="1080" alt="9VS" src="https://github.com/user-attachments/assets/140fd921-f963-40e7-9fdb-256144db7f3c" />

Ahora antes de seguir rellenando archivos es importante crear un dominio en no-ip por que lo usaremos mas adelante: 
<img width="1920" height="1080" alt="10VS" src="https://github.com/user-attachments/assets/cdbe12b7-a97b-41bd-9d06-5e5099900125" />

hacemos un cambio en el nombre por que no se pueden poner _
<img width="1920" height="1080" alt="11VS" src="https://github.com/user-attachments/assets/2940c3c7-e4cc-463e-b025-dfd4fd3b601a" />

Ahora en la carpeta scripts creamos el archivo .env y pegamos este codigo que ya he ajustado a lo que necesito: 
<img width="1920" height="1080" alt="12VS" src="https://github.com/user-attachments/assets/f45fcc7c-5542-4cc6-864b-7dca52580b0d" />

Ahora creamos el archivo deploy_backend.sh:
<img width="1920" height="1080" alt="13VS" src="https://github.com/user-attachments/assets/4337ec2d-430c-4719-b80c-672eed1d011d" />

Ahora el archivo deploy_frontend.sh:
<img width="1920" height="1080" alt="14VS" src="https://github.com/user-attachments/assets/8a4dee6c-04a0-4000-80c9-dc4ac00e0d7b" />

Ahora el archivo install_lamp_backend.sh:
<img width="1920" height="1080" alt="15VS" src="https://github.com/user-attachments/assets/a4217bdd-72ae-4dd0-a3d7-d9842e934ef4" />

Ahora el archivo install_lamp_frontend.sh:
<img width="1920" height="1080" alt="16VS" src="https://github.com/user-attachments/assets/12e22ddc-668b-479d-8758-0e212a228ef4" />

Y por ultimo el archivo setup_letencrypt_certificate.sh:
<img width="1920" height="1080" alt="17VS" src="https://github.com/user-attachments/assets/b0ceeafd-e9f8-49c3-bca1-0396e0772489" />


Finalmente hacemos comprobaciones para asegurarnos de que funciona:

<img width="1920" height="1080" alt="18VS" src="https://github.com/user-attachments/assets/66f3de63-d4e8-4426-a351-a950c265e715" />
<img width="1920" height="1080" alt="19VS" src="https://github.com/user-attachments/assets/53133360-db15-4fad-ac59-aefa8204418c" />
<img width="1920" height="1080" alt="20VS" src="https://github.com/user-attachments/assets/28743fd9-326a-4d18-a32d-cac06c847ef5" />
<img width="1920" height="1080" alt="21VS" src="https://github.com/user-attachments/assets/bf00ee10-f069-4a4a-819b-b574438a59a1" />
<img width="1920" height="1080" alt="22VS" src="https://github.com/user-attachments/assets/9b7aa935-837b-4f6b-a9ba-1d3eda9c39ec" />
<img width="1920" height="1080" alt="23VS" src="https://github.com/user-attachments/assets/7d4f68d3-9d00-4c50-96c2-9a00923ce640" />
















































