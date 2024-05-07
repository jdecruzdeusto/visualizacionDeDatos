
# Reto: Visualización de Datos

Introducción a Kibana y Elastic Search

## Descripción:

Este reto tiene como objetivo crear una plataforma con el stack de elastic.

Mínimos:

- Crear 1 nodos de elastic y 1 nodo con kibana. Versión elastic mínima→8

- Insertar datos en un índice

- Crear 1 dashboard con varios gráficos adecuados a los datos introducidos

- Extra: Seguridad mediante certificados

## Estructura 🏗️

![image](https://github.com/jdecruzdeusto/visualizacionDeDatos/assets/125390240/e218bb8b-8777-4940-8553-bcb9e57fc2cd)


## Ejecución 🚀

0. REQUERIMIENTOS

- Tener docker instalado en tu sistema

1. Ejecutar el comando para iniciar levantar los conetenedores, generar los certificados y la contraseña:
```bash
sudo docker-compose up
```

2. Abrir el navegador y entrar en Elastic Search:
```bash
http://localhost:5061
```
3. Introducir la contraseña y el usuario:

- Usuario: elastic

- Contraseña: *DEFINIDA EN .env*

4. Una vez dentro, se accede a:

- Management -> Kibana -> Saved objects -> Import el ‘.ndjson’

- Analytics -> Machine Learning -> Data visualizer -> File e importar el ‘.csv’

- Analytics -> Dashboard or Recently viewed

- Cambiar el índice al nuevo que incorpora los datos del ‘.csv’

## Pasos seguidos para realizar el reto 🚶

1. Leer y entender qué es y cómo funciona Elastic Search con Kibana
   
2. Crear el archivo docker-compose.yml definiendo las partes iniciales de ES y Kibana

3. Al intentar entrar en el servicio de Kibana pide un código, el cual se consigue ejecutando el fichero indicado

4. Incluir usuario y contraseña (contraseña autogenerada al instalar Elastic)

5. Una vez dentro de Kibana, seleccionar la opción de "Machine Learning" y en el apartado de "Data Visualizer"/"Visualize data from a file" seleccionar el botón "Select file". Seleccionar "Select or drag and drop a file" y añade el fichero csv que hemos utilizado para este proyecto (turbinas.csv)

6. Seleccionar el botón "Import", incluye como Index name "turbinas" y vuelve a seleccionar "Import"

7. Clickar el botón "Create dashboard", seleccionar la opción "Add panel"/"Lens" y crear las distintas agregaciones

## Posibles vías de mejora 📈
- Mejorar la calidad y variedad de los datos

- Insertar datos desde distintas fuentes

- Implementar ML para hacer análisis y predicciones sobre los datos

- Implementar librerías para mejorar la variedad y complejidad del dashboard

## Alternativas posibles 🔜
- Grafana

- InfluxDB

- MongoDB


## Problemas / Retos encontrados ❗
- Comprensión del reto

- Crear y exportar dashboard

- Contraseña Elastic Search/Kibana

- Certificados
