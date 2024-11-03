# 🚀 KallmanSimulation: 3D Kalman Filter on Noisy LIDAR Data

<p align="center">
  <img src="https://raw.githubusercontent.com/GoldHood/IA-KallmanSimulation/refs/heads/main/Simulation.png" alt="Kalman Filter Simulation" width="44%">
</p>

🎉 **Bienvenido a KallmanSimulation** 🎉 – Una inmersión en el uso del **Filtro de Kalman** aplicado a datos ruidosos de LIDAR en 3D. En esta simulación, aprenderás cómo transformar datos de sensores con ruido en trayectorias precisas y claras, ofreciendo una herramienta educativa valiosa para la comunidad interesada en el procesamiento de señales, la inteligencia artificial, y la robótica.

## 🌟 Introducción
El objetivo de **KallmanSimulation** es demostrar cómo el filtro de Kalman puede mejorar la precisión en las mediciones de LIDAR, que comúnmente sufren de ruido debido a interferencias y limitaciones del hardware. A través de un modelo visual, mostramos cómo esta técnica es útil para aplicaciones en navegación y seguimiento de objetos en movimiento.

En esta simulación, generamos datos sintéticos de LIDAR a lo largo de una espiral tridimensional, introduciendo ruido gaussiano para simular inexactitudes de sensores. Con el filtro de Kalman, suavizamos los datos y estimamos la trayectoria verdadera, brindando una experiencia visual de cómo este método de filtrado puede ser aplicado en escenarios de la vida real.

## ✨ Características
- 📊 **Simulación Realista**: Generación de datos LIDAR en 3D con ruido, representando la incertidumbre en las mediciones.
- 🧠 **Filtro de Kalman Inteligente**: Filtrado efectivo de ruido para obtener una trayectoria precisa y continua.
- 📈 **Visualización Comparativa**: Comparación entre la trayectoria real, los datos con ruido y el camino estimado por el filtro de Kalman.

## 💡 Cómo Funciona el Filtro de Kalman
En este proyecto, implementamos un filtro de Kalman simplificado en 3D que solo considera la posición y no la velocidad o aceleración. Este proceso incluye:

1. **Generación de Datos**: Creamos una espiral en 3D de 50 puntos como la trayectoria verdadera. Introducimos ruido gaussiano aleatorio para simular inexactitudes de un sensor LIDAR.
2. **Inicialización**: La estimación inicial del estado se define a partir de la primera medición con ruido, y la covarianza del estado se inicializa como la matriz identidad.
3. **Predicción**: Sin un modelo de movimiento, se asume que la posición se mantiene constante, y la matriz de covarianza se ajusta con el valor de incertidumbre `Q`.
4. **Actualización de Medición**: Calculamos la ganancia de Kalman para cada punto de datos, ajustando la estimación filtrada y reduciendo el impacto del ruido.
5. **Corrección**: Iteramos este proceso para cada punto, mejorando gradualmente la precisión de la trayectoria.

## 🚀 Instalación y Ejecución
Para instalar y ejecutar la simulación:

1. Clona el repositorio:
   ```bash
   git clone https://github.com/GoldHood/IA-KallmanSimulation.git
   cd IA-KallmanSimulation
   ```

2. Instala las dependencias necesarias:
   ```bash
   pip install numpy matplotlib
   ```

3. Ejecuta el programa para visualizar la simulación:
   ```bash
   python kallman_simulation.py
   ```

## 🔍 Ejemplo de Salida
El programa generará un gráfico 3D con:
- **Trayectoria Verdadera** (línea discontinua) – La espiral original en el espacio 3D.
- **Mediciones con Ruido** (puntos rojos) – Datos sin procesar de LIDAR con ruido.
- **Trayectoria Filtrada con Kalman** (línea verde) – La trayectoria estimada luego de aplicar el filtro de Kalman.

Esta visualización permite ver cómo el filtro de Kalman limpia el ruido, generando una trayectoria que sigue de cerca el camino verdadero:

![Kalman Simulation Plot](https://raw.githubusercontent.com/GoldHood/IA-KallmanSimulation/refs/heads/main/Simulation.png)

## 📘 Implementación del Código
Aquí tienes un resumen de las funciones clave en el código:

- **generate_lidar_data**: Genera la espiral en 3D con ruido.
- **kalman_filter_3d**: Aplica el filtro de Kalman a los datos con ruido, ajustando cada punto según la ganancia de Kalman calculada.

El filtro de Kalman se usa para predecir y actualizar posiciones en función de la medición y la incertidumbre del sensor, permitiendo que la trayectoria filtrada sea mucho más precisa.

## 🎯 Aplicaciones y Audiencia
**KallmanSimulation** es ideal para:

- **Desarrolladores de IA y ML** que desean entender aplicaciones de filtrado en el mundo real.
- **Estudiantes y Profesores** que buscan un recurso práctico para enseñar procesamiento de señales.
- **Investigadores en robótica y vehículos autónomos** que requieren mejoras en la precisión de datos de sensores en ambientes ruidosos.

## 🤝 Contribuciones
Este proyecto es de código abierto y está diseñado para crecer con la comunidad. Si tienes ideas o mejoras, ¡no dudes en colaborar!

1. Haz un fork del repositorio.
2. Crea una rama para tu característica (`git checkout -b feature-branch`).
3. Realiza tus cambios y haz commit (`git commit -m "Add new feature"`).
4. Haz push a tu rama (`git push origin feature-branch`).
5. Abre un Pull Request para revisión.

## 📜 Licencia
Este proyecto está bajo la licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.

## 📢 Conclusión
**KallmanSimulation** demuestra cómo el filtro de Kalman puede reducir eficazmente el ruido en los datos de LIDAR, proporcionando una trayectoria más precisa de un objeto en movimiento. Esta simulación simplificada muestra el potencial de esta técnica en aplicaciones prácticas como la navegación de vehículos autónomos y el seguimiento de objetos. Con esta herramienta educativa, esperamos contribuir al aprendizaje y desarrollo en procesamiento de datos de sensores.

