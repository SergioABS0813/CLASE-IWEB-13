# CLASE-IWEB-13
Despliegue en nube con Google Cloud

## Creación de Máquina Virtual en GCP

-Ingresamos en el buscador a "google console"

-Creamos el proyecto y le damos a seleccionar proyecto:

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/f74ad273-17d4-4d91-88be-b0a5afaf63c5)

-Vamos a Compute Engine

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/30644c59-0345-4282-88b9-8b42f0ac8eee)

- Creamos una máquina virtual
  En la opción de Región (se escogerá pero tiene distintos costos y distintos performance) **En clase usamos: us-central(lowa)**

  En la zona de disponibilidad seleccionamos: **us-central1-a**
  
  ![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/4a5a5afb-0ea8-4b8e-8427-0bfa579caeda)
  
  En Configuración de la máquina seleccionamos la potencia de la máquina (según lo que deseemos)

  ![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/ee487219-74d2-4472-92f2-f34e675c8f3a)
  
  En Tipo de Máquina, seleccionamos sus núcleos (Dejamos en micro es más barato)

  ![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/6238a3e6-04ab-4974-8488-c17ae7bebaa1)
  
  Damos clic en configuración de modelo

  ![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/0eaf5c1f-cf53-4f9e-968c-4268abfc2237)

  Vemos Disco de Arranque y le damos a cambiar: (**cambiamos a Ubuntu**)

  ![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/46536522-822c-4c81-b9c1-1a9d7fcf7bbc)

  ![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/0ba87b7c-1246-407c-8e17-265f23473073)

  En Firewall podemos permitir HTTP y HTTPS. (Como JAVA emplea puerto 8080 y no 80 de HTTP ni 443 HTTPS) **no es necesario habilitarlos**

  ![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/3080d3be-cd68-4ec0-a4e7-93a7d90fec03)

  Si sale error en la máquina virtual creada simplemente la borramos y creamos otra
  
## Conexión a la VM con SSH:

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/1bad46c8-05de-4a50-8b41-d617a09df476)

Le damos a Authorize

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/da01d4e5-f0f4-4521-b4bf-fd01cef229ca)

## Mantener la IP Pública (Proyecto Investigación)

## Conexión a la VM con otro cliente

## Despliegue de proyecto sin Base de Datos

Cuando corro con Java un proyecto lo hace en .jar. Sin embargo, el proyecto ".war" no se corre. Todo mi proyecto en JAVA se comprime en un ".war"

Entonces cuando yo corro mi proyecto, la "flechita verde" empaqueta todo el proyecto en un war (.war) y levanta el Server Tomcat. **El problema es que ahora el Tomcat tiene que estar en Nube, no en la PC únicamente**

Entonces primero **generamos el archivo en .war**, segundo **levantamos el Tomcat** y tercero **manualmente colocamos el .war en el Tomcat**.

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/a56f0dcb-3d34-45dc-8bac-36184b8f119e)

Clic en Package y luego le damos a correr el Maeven: (OJO EL MAEVEN NO EL TOMCAT)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/6fb676dc-9648-4e42-80f2-7b5495e07078)

Luego cuando finalice, en Target veremos el .war

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/b3528a78-deff-4ad5-85e9-cf06010f075f)

**Instalamos Java en la máquina virtual pero en la versión de nuestro proyecto**

Nos fijamos la versión de nuestro JAVA en New Project:

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/4e02a49c-d63f-428b-8e8a-01101194e712)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/f1ed278d-5505-4061-94aa-4f77d6b83dcb)

**Instalamos Tomcat en la VM**

Vamos a la página de TOMCAT y vamos al TOMCAT 10:

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/d4ebc7b5-fcb3-4fa9-b5e4-53edec23bd8c)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/9d3c0288-6172-4afa-b8d5-10fe25f2187f)

Usamos el comando: wget <link para bajar de internet>

Ahora lo destareamos: (Usamoe el nombre del archivo en nuestra VM)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/93496be3-b7e5-4d54-846d-0e148fb7f825)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/7665f12a-7f5d-442c-971f-ea66e29827b9)

Creamos un Usuario TOMCAT para que corra:

  sudo useradd -M -d /usr/share/apache-tomcat/ tomcat

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/6aa79ba9-082f-4d40-858a-1b7ee83045a3)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/6bca04b6-1a8d-45d6-9cb0-c1c374cbd889)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/4e3e83f0-b50e-4c9a-bb63-9380a9559636)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/a7e05c66-d6b3-4c48-8f34-096940802126)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/7e71c661-097f-46f5-98f6-aa0a3369adec)

**Luego le damos ctrl X, Yes y ENTER**

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/63276f3c-c657-492d-b3ce-190b5cb4021f)

Colocamos en comentario:

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/624f22a8-dcb1-462d-823a-79861601b465)

**Luego le damos ctrl X, Yes y ENTER**

Ahora Tomcat tiene que correr el Servicio

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/361225b5-a5de-4d3c-87e1-92c3d84f1f51)

Y compiamos el código adentro para ejecutar el servicio de TOMCAT (**NOS DAMOS CUENTA QUE SI HAY UNA VERSION DIFERENTE LA CAMBIAMOS EN BASE A NUESTRA VERSION DE PROYECTO**)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/ed16b4bc-7f9c-4efd-a9bc-6457457ce3ed)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/09bd0505-262c-4570-bf70-1deaf6b79529)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/6d166c1c-82aa-4342-9f8c-a705cf63c4e9)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/f720aea4-9a0b-401a-9012-98d34d268757)

Ahora abrimos el puerto desde GCP:

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/8ecda752-b556-445b-a0fa-181b93b9c091)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/04203db1-40b3-44fa-b728-8929694b33ac)

Creamos regla en Firewall:

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/0f77e73b-bdfc-4258-adb4-b7043b267af6)

Ahora sí colocamos 0.0.0.0/0

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/e9370d61-1e05-4a39-a4c2-d53e28058136)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/fa422b6f-741e-422f-ab21-1cbed2cd194d)

Colocamos a la Instancia la regla creada al Firewall:

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/b6b2c003-32df-438b-a26e-fc3d92303e46)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/2fafd0b0-4550-4788-be61-1f2ed7b90e70)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/5c0f0e8b-21b3-4a1e-b8f4-bf717ae933fb)

Ingresamos a nuestra VM

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/f61836b3-3ece-45aa-a379-40203b205781)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/fafc9192-23f7-4753-8581-dd5d893fc20b)


## 1:56


## Levantamos Servidor de Base de datos
Levantamos Base de Datos en base a Servicio de levantamiento de Base de datos en GCP:

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/e9406924-8737-4589-8de1-bbc4d0e47e79)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/eb7b2aaa-5a67-47a2-86a5-b2a8546ccd11)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/8fc74cd9-d8f1-4d37-b50f-ffcdaf571590)

Ahora le asignamos configuraciones y vemos el costo:

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/99485b8f-745b-4ed4-ba0f-45dd1da1fa33)

Le damos a Enterprise:

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/0498858d-fd5e-4da5-9497-267a868a8a62)

Le asignamos una zona única:

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/37eece97-544e-4e18-a062-6cd0848229b5)

Le damos a 1 núcleo:

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/3ce9daa9-e045-4a35-9ee9-3cc47bec36b7)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/b0220b8d-b36f-489a-acaf-a1bcec3b7071)

Para conectarme desde redes autorizadas (Entre ellas el Workbench)

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/d8edddef-880a-4cef-879f-fec08171508f)

A manera de Prueba colocamos todo en redes autorizadas:

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/72c3e24a-457e-4ed5-9035-b5f924cfe61b)

Luego en Crear Instancia:

![image](https://github.com/SergioABS0813/CLASE-IWEB-13/assets/134556600/393a71b4-6a08-4949-ba0c-8d195b4a2ac2)

**HEMOS CREADO NUESTRO SERVIDOR DE BASE DE DATOS**






  





  

