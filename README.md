# Análisis de Tenis mediante Computer Vision

Este proyecto implementa un sistema de análisis de partidos de tenis utilizando técnicas de computer vision. El sistema detecta jugadores, la pelota, y genera estadísticas de juego en tiempo real.

## Características

- Detección y seguimiento de jugadores
- Detección y seguimiento de la pelota
- Detección de líneas de la cancha
- Visualización de mini-cancha con posiciones en tiempo real
- Cálculo de estadísticas:
  - Velocidad de los tiros
  - Velocidad de movimiento de los jugadores
  - Velocidades promedio
  - Posiciones en la cancha


## Modelos Pre-entrenados

El proyecto utiliza los siguientes modelos:

- **YOLO para detección de jugadores**: Modelo entrenado para detectar y seguir a los jugadores en la cancha.
- **YOLO para detección de pelota**: Modelo especializado en detectar la pelota de tenis, aunque presenta algunos desafíos:
 - El entrenamiento fue complejo debido al pequeño tamaño de la pelota
 - La alta velocidad de la pelota causó dificultades en la detección
 - Se requirió un extenso conjunto de datos de entrenamiento para mejorar la precisión
- **Modelo personalizado para detección de líneas de la cancha**: Detector de puntos clave para identificar las líneas y dimensiones de la cancha.

### Desafíos Técnicos

#### Detección de la Pelota
- La pelota de tenis es muy pequeña en el frame del video
- El movimiento rápido causa motion blur
- Las sombras y cambios de iluminación afectan la detección
- Se necesitó entrenar durante dias el modelo y hacer mucho post processing.

#### Visualización en Mini-Court
- El seguimiento de la pelota en la vista miniatura presenta inconsistencias
- La conversión de coordenadas entre la cancha real y la miniatura requirió ajustes de perspectiva
- El movimiento de la pelota puede aparecer errático debido a:
 - Errores en la detección original
 - Imprecisiones en la transformación de coordenadas
 - Desafíos en el manejo de la perspectiva de la cancha


https://drive.google.com/drive/folders/1kXu_O8Yg2R90vxw_ddSkUSCTt5j_bmA6?usp=sharing
