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
    - **pandas==2.0.3**
    - **requests==2.31.0**
    - **tqdm==4.64.1**
    - **python-dotenv==1.0.0**
    - **beautifulsoup4==4.12.2**
    - **twilio==7.18.0**
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

Nota: Este proyecto no solo tiene fines educativos, sino que también puede adaptarse fácilmente a escenarios reales, como servicios personalizados para empresas, aplicaciones móviles, o sistemas de monitoreo climático.

# Descripción del Flujo de Trabajo

## Integración de APIs
- Se utilizó WeatherAPI para obtener pronósticos meteorológicos en formato JSON. Este proceso incluyó:
    - Construcción de URLs dinámicas: Incorporando parámetros como la ciudad, número de días y alertas.
    - Manejo de solicitudes HTTP: Usando la librería requests para enviar peticiones GET.
    - Procesamiento de datos JSON: Transformando los datos de la API en estructuras manejables como DataFrames.
    - Ejemplo de URL generada: http://api.weatherapi.com/v1/forecast.json?key=tu_api_key&q=Medellin&days=1&aqi=no&alerts=no

## Automatización de Tareas
- Se configuró un sistema de envío automatizado de notificaciones SMS mediante Twilio, que incluyó:
    - La gestión de credenciales sensibles (como el **account_sid** y **auth_token*) mediante un archivo **.env*.
    - La configuración de un número de teléfono desde Twilio como remitente.
    - El envío de mensajes personalizados, incluyendo los datos climáticos relevantes.