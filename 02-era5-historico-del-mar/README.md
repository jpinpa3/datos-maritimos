# 02 · ERA5: el histórico del mar

## La idea en una frase

ERA5, el reanálisis del programa europeo Copernicus, da estimaciones hora a hora de viento, oleaje, presión o temperatura en todo el planeta desde 1940. Es abierto y gratuito.

## Qué es un reanálisis

Es una reconstrucción del tiempo pasado:

1. Se ejecuta un modelo meteorológico, del mismo tipo que los de previsión, hacia atrás en el tiempo.
2. En cada paso se corrige con todas las observaciones disponibles: boyas, buques, estaciones, globos sonda y satélites.
3. El resultado es la mejor estimación posible en cualquier punto, incluso donde nunca hubo un instrumento midiendo.

## Características principales

| Aspecto | Valor |
|---|---|
| Periodo | Desde 1940 hasta la actualidad (actualización diaria) |
| Resolución temporal | Horaria |
| Malla de variables atmosféricas | 0,25° × 0,25° |
| Malla de variables de oleaje | 0,5° × 0,5° (unas 30 millas de norte a sur) |
| Acceso | Climate Data Store de Copernicus, con cuenta gratuita |

## Usos en el sector marítimo

**Planificar**
- Navieras: estimar cuántos días al año un ferry no podrá operar en una ruta por estado de la mar.
- Aseguradoras: ajustar la prima al riesgo meteorológico real de una ruta o zona.
- Astilleros: decidir para qué estado de la mar se diseña un buque.

**Evaluar decisiones**
- Comprobar si un cambio de derrota para esquivar un temporal ahorró combustible o tiempo.
- Verificar, en una reclamación, si el temporal alegado por un buque existió.

## Límites

- **No es una medición directa:** es un modelo corregido con observaciones, y suaviza los extremos locales.
- **La malla de oleaje es gruesa:** sirve para mar abierto, no para el interior de un puerto ni para zonas costeras muy abrigadas.
- **Si se pide un punto concreto, se devuelve el nodo de malla más cercano.**
- **La calidad depende de las observaciones disponibles:** es mayor en las últimas décadas y en zonas con mucho tráfico e instrumentación.

## Notebook: días de mala mar en un punto

[`era5_dias_mala_mar.ipynb`](era5_dias_mala_mar.ipynb) descarga la serie horaria de altura significativa de ola en un punto de mar abierto frente a la costa de Cartagena y calcula, para cada año, cuántos días se superaron 2, 3 y 4 metros, además de la estacionalidad mensual.

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jpinpa3/datos-maritimos/blob/main/02-era5-historico-del-mar/era5_dias_mala_mar.ipynb)

Requisitos: cuenta gratuita en el [Climate Data Store](https://cds.climate.copernicus.eu), aceptar la licencia de ERA5 y la clave personal de la API. El notebook explica cada paso.

## Fuentes

- Copernicus Climate Change Service (C3S) / ECMWF. *ERA5 hourly data on single levels from 1940 to present*. https://doi.org/10.24381/cds.adbb2d47
- Copernicus Climate Change Service (C3S) / ECMWF. *ERA5 hourly time-series data on single levels from 1940 to present*.

Contiene información modificada del Copernicus Climate Change Service.
