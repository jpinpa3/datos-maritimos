# 01 · Buques oscuros: lo que el AIS no ve

## La idea en una frase

Entre el 72 % y el 76 % de los pesqueros industriales del mundo no aparecen en los sistemas públicos de seguimiento de buques. Lo demostró un estudio publicado en *Nature* en 2024 cruzando imágenes de satélite, posiciones AIS y aprendizaje profundo.

## Qué es el AIS y por qué tiene huecos

El Sistema de Identificación Automática (AIS) es un transpondedor que emite la identidad, posición, rumbo y velocidad del buque. La Organización Marítima Internacional lo exige (SOLAS, capítulo V, regla 19) a:

- buques de 300 GT o más en viajes internacionales,
- buques de carga de 500 GT o más en viajes nacionales,
- todos los buques de pasaje, sea cual sea su tamaño.

Fuera de esos casos no es obligatorio, y un equipo obligatorio puede estar apagado, averiado o fuera de la cobertura de los receptores. Por eso un mapa construido solo con AIS muestra una parte del tráfico, no todo.

## Qué hizo el estudio

El equipo de Global Fishing Watch y varias universidades (Paolo et al., 2024):

1. Analizó unos 2 petabytes de imágenes de satélite de 2017 a 2021, principalmente radar de apertura sintética de Sentinel-1 (programa Copernicus), que detecta barcos aunque no emitan.
2. Entrenó modelos de aprendizaje profundo para detectar buques e infraestructuras en el mar y clasificar su actividad.
3. Comparó cada detección con las posiciones AIS públicas: lo que el satélite veía y el AIS no, quedó marcado como «no rastreado públicamente».

## Resultados principales

| Actividad | Proporción no rastreada públicamente |
|---|---|
| Pesca industrial | 72-76 % |
| Transporte y energía | 21-30 % |

La mayor parte de la pesca no rastreada se concentra en el sur y sudeste de Asia y en África. El estudio también detectó actividad no rastreada dentro de áreas marinas protegidas.

## Lecciones para el análisis de datos

- **Ninguna fuente aislada es completa.** El patrón aparece al fusionar fuentes independientes.
- **El satélite no sustituye al AIS: lo valida.** Cada fuente tiene sus límites (cobertura, resolución, frecuencia de paso).
- **La ausencia de datos también es un dato.** Antes de analizar un conjunto de datos conviene preguntarse quién no aparece en él y por qué.
- **«No rastreado» no significa «ilegal».** El estudio mide visibilidad pública, no legalidad: muchos buques no están obligados a llevar AIS.

## Para explorar

- Mapa público de Global Fishing Watch: https://globalfishingwatch.org/map
- Datos y código del estudio: enlazados desde el artículo de *Nature*.

## Fuentes

- Paolo, F. S., Kroodsma, D. et al. (2024). *Satellite mapping reveals extensive industrial activity at sea*. Nature, 625, 85-91. https://doi.org/10.1038/s41586-023-06825-8
- Organización Marítima Internacional. *AIS transponders* (SOLAS V/19). https://www.imo.org/en/OurWork/Safety/Pages/AIS.aspx
- Agencia Espacial Europea (2024). *Sentinel-1 and AI reveal 75% of fishing vessels not tracked*.
