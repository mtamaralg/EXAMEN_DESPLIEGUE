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






















