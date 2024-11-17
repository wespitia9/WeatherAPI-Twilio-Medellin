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
- Documentación oficial [Python 3.11](https://docs.python.org/3.11/)
- Librerías utilizadas
    - pandas==2.0.3
    - requests==2.31.0
    - tqdm==4.64.1
    - python-dotenv==1.0.0
    - beautifulsoup4==4.12.2
    - twilio==7.18.0

## WeatherAPI:
- Una API RESTful que proporciona datos climáticos en tiempo real, pronósticos y alertas.
- Permite configurar parámetros como la ciudad, días de pronóstico y calidad del aire, lo que la hace versátil para aplicaciones meteorológicas.
- Documentación oficial [WeatherAPI](https://www.weatherapi.com/docs/)

## Twilio:
- Un servicio de comunicación en la nube utilizado para el envío de mensajes SMS.
- Proporciona herramientas para configurar credenciales, manejar números de teléfono y personalizar mensajes.
- Documentación oficial [Twilio](https://www.twilio.com/docs)

## Jupyter Notebook:
- Herramienta clave para el desarrollo iterativo, organización de código y visualización de resultados.
- Documentación oficial [Jupyter Notebook](https://jupyter-notebook.readthedocs.io/en/stable/)

Nota: Este proyecto no solo tiene fines educativos, sino que también puede adaptarse fácilmente a escenarios reales, como servicios personalizados para empresas, aplicaciones móviles, o sistemas de monitoreo climático.