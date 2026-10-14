# Ice — Análisis de ventas de videojuegos

Proyecto integrado del Sprint 6 de Ciencia de Datos de TripleTen, desarrollado
como ejercicio formativo por Jesús Alejandro Gómez Pérez con acompañamiento.

## Problema

En el escenario de diciembre de 2016, la tienda Ice necesita identificar patrones
asociados con las ventas para orientar sus campañas de 2017. El análisis estudia
plataformas, géneros, reseñas y diferencias entre Norteamérica, Europa y Japón.

## Herramientas y competencias

Python, Pandas, NumPy, Matplotlib y SciPy: preparación de datos, ausentes,
análisis exploratorio, visualización, comparación de catálogos, perfiles
regionales y contrastes bilaterales de medias con Welch.

## Datos y metodología

- Archivo inicial: 16,715 registros y 11 columnas.
- Encabezados normalizados; años como enteros anulables; `tbd` de las notas de
  usuarios convertido a ausente, sin asignarle una calificación artificial.
- Ventas globales calculadas como suma de cuatro regiones.
- Ventana principal 2013–2016, elegida a partir de la evolución de plataformas.
- Ausencia de ESRB conservada como grupo explícito en los perfiles.
- Alfa 0.05 y pruebas de Welch para Xbox One/PC y Action/Sports, con controles
  descriptivos y análisis de sensibilidad por período y título.

## Hallazgos principales

- PS4 lidera las ventas registradas de 2013–2016 con 314.14 millones en la escala
  de ventas de la fuente. La evolución del catálogo favorece PS4 y Xbox One
  como candidatas para la planificación del escenario de 2017.
- Japón presenta un perfil distinto: 3DS concentra cerca del 48.2% de las ventas
  regionales del período y Role-Playing alrededor del 36.3%.
- Las notas de críticos de PS4 muestran una asociación lineal positiva con
  ventas; las notas de usuarios no muestran una relación lineal clara.
- Xbox One frente a PC: p≈0.1476, sin rechazo de igualdad de medias al 5%; esto
  no demuestra equivalencia. Action frente a Sports: p≈1.446×10⁻²⁰, con diferencia
  de medias bajo el análisis planteado.

Estas conclusiones describen el escenario histórico del ejercicio, no el mercado
actual. No se entrenó un modelo predictivo ni se calcularon beneficios.

## Limitaciones

2016 puede estar incompleto. Las ventas asociadas a lanzamientos no equivalen a
transacciones medidas por año calendario. Hay reseñas y clasificaciones ausentes;
las correlaciones no identifican causalidad. Sin costos no puede afirmarse
rentabilidad. El notebook conserva la descripción de unidades de la consigna,
cuya interpretación monetaria no se validó independientemente frente a la fuente.

## Ejecutar

Desde esta carpeta, crea un entorno propio e instala `requirements.txt`.
En Windows:

```powershell
py -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

Abre `ice_video_game_analysis.ipynb` en VS Code, selecciona `.venv` como kernel,
ejecuta todas las celdas y guarda. El notebook busca `games.csv` localmente;
también conserva la ruta del entorno educativo y un enlace de descarga como
alternativas. El CSV incluido permite ejecutar sin descargar datos al iniciar.

## Archivos y revisión

- `ice_video_game_analysis.ipynb`: notebook con salidas y comentarios originales
  de revisión conservados.
- `games.csv`: fuente del análisis.
- `requirements.txt`: dependencias.

La revisión contenida es favorable; no se presenta como certificación de dominio
autónomo ni se infiere una aprobación formal que no conste en esa revisión.

## Fuente

[Dataset games.csv — material de práctica de TripleTen](https://practicum-content.s3.us-west-1.amazonaws.com/datasets/games.csv).
El contexto comercial es un caso de formación, no un encargo de una empresa real.
