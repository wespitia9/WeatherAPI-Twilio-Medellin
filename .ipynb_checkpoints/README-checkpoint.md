# Automatización de notificaciones climáticas

Este proyecto fue desarrollado como parte de un proceso de aprendizaje enfocado en integrar servicios web y automatizar tareas utilizando Python como lenguaje principal. A lo largo del desarrollo, se exploraron conceptos clave relacionados con el uso de APIs RESTful, la gestión de credenciales y la comunicación mediante SMS. A continuación, se detalla cada uno de los aspectos que abarca este proyecto y cómo contribuye a dicho proceso de aprendizaje:

# Objetivos del proyecto
1. Aprender e implementar el manejo de datos provenientes de APIs públicas como WeatherAPI.
2. Automatizar procesos mediante el uso de herramientas como Twilio, permitiendo el envío de notificaciones SMS con pronósticos climáticos en tiempo real.
3. Comprender conceptos prácticos relacionados con la manipulación de datos, la interacción con servicios externos y la estructuración de proyectos Python.


# Tecnologías Utilizadas

## Python:
- El lenguaje base para la integración de servicios web, análisis de datos y automatización.
- La versión utilizada fue 3.11.10, seleccionada por su compatibilidad con las librerías más recientes.
- Librerías utilizadas para la creación del archivo ´requirements.txt´
    - `pandas==2.0.3`
    - `requests==2.31.0`
    - `tqdm==4.64.1`
    - `python-dotenv==1.0.0`
    - `beautifulsoup4==4.12.2`
    - `twilio==7.18.0`
- Documentación oficial de [Python 3.11](https://docs.python.org/3.11/)

## WeatherAPI:
- Una API RESTful que proporciona datos climáticos en tiempo real, pronósticos y alertas.
- Permite configurar parámetros como la ciudad, días de pronóstico y calidad del aire, lo que la hace versátil para aplicaciones meteorológicas.
- Documentación oficial de [WeatherAPI](https://www.weatherapi.com/docs/)

## Twilio:
- Un servicio de comunicación en la nube utilizado para el envío de mensajes SMS.
- Proporciona herramientas para configurar credenciales, manejar números de teléfono y personalizar mensajes.
- Documentación oficial de [Twilio](https://www.twilio.com/docs)

## Jupyter Notebook:
- Herramienta clave para el desarrollo iterativo, organización de código y visualización de resultados.
- Documentación oficial de [Jupyter Notebook](https://jupyter-notebook.readthedocs.io/en/stable/)


# Descripción del Flujo de Trabajo

## Integración de APIs
- Se utilizó WeatherAPI para obtener pronósticos meteorológicos en formato JSON. Este proceso incluyó:
    - Construcción de URLs dinámicas: Incorporando parámetros como la ciudad, número de días y alertas.
    - Manejo de solicitudes HTTP: Usando la librería requests para enviar peticiones GET.
    - Procesamiento de datos JSON: Transformando los datos de la API en estructuras manejables como DataFrames.
    - Ejemplo de URL generada: http://api.weatherapi.com/v1/forecast.json?key=tu_api_key&q=Medellin&days=1&aqi=no&alerts=no

## Automatización de Tareas
- Se configuró un sistema de envío automatizado de notificaciones SMS mediante Twilio, que incluyó:
    - La gestión de credenciales sensibles (como el `account_sid` y `auth_token`) mediante un archivo `.env`.
    - La configuración de un número de teléfono desde Twilio como remitente.
    - El envío de mensajes personalizados, incluyendo los datos climáticos relevantes.

## Análisis y Filtrado de Datos
- Se procesaron los datos climáticos para seleccionar únicamente la información relevante para el usuario:
    - Filtrado por rangos horarios de interés (por ejemplo, entre 12:00 PM y 6:00 PM).
    - Extracción de variables como:
        - Condición climática: Descripciones como "Partly Cloudy" o "Light Rain".
        - Probabilidad de lluvia: Indicado en porcentajes.
        - Temperatura: En grados Celsius.

# Envío de Notificaciones

El mensaje SMS enviado incluye un resumen compacto de los datos procesados.

# Pasos para usar este repositorio:

- Paso 1: Clonar repositorio:
    - git clone https://github.com/wespitia9/WeatherAPI-Twilio-Medellin.git

- Paso 2: Instalación en un entorno Conda
    - Crear un nuevo entorno Conda: `conda create --name weatherapi-twilio python=3.11.10 -y`
    - Activar el entorno: `conda activate weatherapi-twilio`
    - Instalar las dependencias desde el archivo requirements: `pip install -r requirements.txt`
    - Crea un archivo `.env` con las credenciales necesarias:
        - WEATHER_API_KEY=tu_clave_de_weatherapi
        - TWILIO_ACCOUNT_SID=tu_account_sid
        - TWILIO_AUTH_TOKEN=tu_auth_token
        - PHONE_NUMBER=+1234567890

Este repositorio refleja un proceso de aprendizaje personal y sirve como base para cualquier persona interesada en la automatización de notificaciones utilizando APIs y Python. No solo tiene fines educativos, sino que también puede adaptarse fácilmente a escenarios reales, como servicios personalizados para empresas, aplicaciones móviles o sistemas de monitoreo climático. Es un ejemplo claro de cómo integrar servicios en la nube con herramientas de análisis y procesamiento de datos.