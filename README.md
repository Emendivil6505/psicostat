# PsicoStat
Laboratorio de estadística descriptiva para estudiantes de segundo semestre de Psicología.

## Incluye
- Estrés y ansiedad percibidos (puntuaciones educativas de 0 a 10), horas de estudio y horas de ocio.
- Entre 2 y 1000 datos simulados o ingreso manual; exportación CSV.
- Frecuencias agrupadas, Sturges o clases configurables.
- Media, mediana, moda, varianza muestral, desviación, rango, RIC, cuartiles y percentiles. Deciles mediante P10, P20, etc.
- Histograma y caja con regla 1,5 RIC.
- Modo exploración y práctica; preguntas numéricas con retroalimentación y reflexión contextual.

## Ejecutar
Requiere Node.js 22 o posterior. Sin dependencias externas.

    npm test
    npm start

Abrir http://localhost:3000. También se puede abrir public/index.html directamente.

## Publicar con GitHub y Render
1. Crear un repositorio llamado psicostat en GitHub.
2. Subir el CONTENIDO de esta carpeta a la raíz del repositorio (package.json y render.yaml deben quedar en la raíz).
3. En Render, crear un Web Service y conectar ese repositorio desde GitHub.
4. Configurar entorno Node; Build Command: npm test; Start Command: npm start. Elegir un plan disponible en la cuenta.
5. Crear el servicio y esperar el despliegue. Render asignará la URL pública.
6. Abrir la URL y comprobar generación de datos, ingreso manual, tablas, medidas, gráficas y actividad.

render.yaml proporciona configuración de Blueprint como alternativa; si el plan free no está disponible, ajustar el plan antes de desplegar. Las opciones e interfaz del proveedor pueden cambiar.

Para GitHub Pages también puede publicarse únicamente el contenido de public/.

## Convenciones
Medidas exactas calculadas con datos originales, no aproximaciones de las marcas de clase. Varianza con divisor n−1. Cuantiles interpolados: h=(n−1)p, índices desde cero; puede diferir del método usado por un texto. Sturges redondeado al entero más cercano; clases limitadas a 30. Intervalos cerrados a la izquierda, abiertos a la derecha, último cerrado. Límites mostrados con tres decimales, cálculos sin ese redondeo. Empates y variables discretas requieren cuidado al interpretar percentiles. En los ejercicios de 0–10 se trata la puntuación como numérica con fines didácticos. No hay diagnóstico ni puntos de corte clínicos.

El generador usa una distribución acotada de ejemplo; no representa un instrumento validado ni una población real. No incorpora captura de respuestas de varias personas mediante enlace. El ingreso manual permite consolidar respuestas anónimas ya recogidas.

## Privacidad
La aplicación no envía ni guarda los datos en un servidor. Al recargar se pierde el ejercicio; descargar CSV para conservarlo. No ingresar información identificable.

## Validación
Pruebas de cálculos conocidos, cuantiles, atípicos, límites de intervalos, datos constantes y validación mínima. Sintaxis JavaScript verificada. Pendiente revisión visual en navegador y comprobación posterior al despliegue.
