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

## Mantener la IP Pública (Proyecto)

## Conexión a la VM con otro cliente





  





  

