<h1 align="center">ANÁLISIS DE DATOS ABIERTOS DE FÚTBOL APLICANDO LA METODOLOGÍA CRISP-DM</h1>

<p align="center">
<img src="resources/CRISP-DM.png" alt="CRISP-DM" width="" height="400">
</p>

## Requerimientos ‼️
* Python 3.6
* Scikit-learn
* Seaborn
* Matplotlib
* Pandas
* XGBoost
* Numpy
* Time
* Missingno
* Joblib
* Plotly
* Glob
* Requests
* Kaggle

## CRISP-DM 📝
| Fase                             | Descripción                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fase 1: Comprensión del negocio  | • Definición de la situación actual<br>• Establecimiento de los objetivos<br>• Selección de criterios de éxito<br>• Definición de restricciones y supuestos |
| Fase 2: Comprensión de los datos | • Búsqueda de fuentes<br>• Descripción de los datos<br>• Verificación de calidad<br>• Exploración de datos                                                  |
| Fase 3: Preparación de los datos | • Limpieza<br>• Estructuración<br>• Integración                                                                                                             |
| Fase 4: Modelado                 | • Selección de técnicas de modelado<br>• Generación plan de prueba<br>• Construcción de modelos                                                             |
| Fase 5: Evaluación               | • Evaluación de resultados                                                                                                                                  |
| Fase 6: Implantación             | • Definición de plan de monitorización e implementación<br>• Revisión del proceso y líneas futuras                                                          |

## Resultados 📊
### Fase 1: Comprensión del negocio
- Objetivo
- Criterios de éxito
- Requisitos, supuestos y limitantes

### Fase 2: Comprensión de los datos 💿
| Fuente                                                                                                                                                                              | Naturaleza            | Descripción                                                | Estructura                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [StatsBomb](https://statsbomb.com/es/)                                                                                                                                              | Base de datos abierta | Datos de partidos nacionales e internacionales             | **competitions.json**: Archivo con las competiciones y temporadas.<br>**matches**: Carpeta que contiene los partidos organizados por subcarpetas de competiciones y cada archivo contiene los partidos de una temporada.<br>**events**: Carpeta que contiene eventos de todos los partidos.<br>**lineups**: Carpeta que contiene alineaciones de todos los partidos. |
| [SOFIFA](https://sofifa.com)                                                                                                                                                        | Web scrapping         | Características de los jugadores videojuego FIFA 2023      | **male_players.csv**: Archivo con el detalle de los jugadores.<br>**male_teams.csv**: Archivo con el detalle de los equipos.                                                                                                                                                                                                                                         |
| [International Football](https://www.kaggle.com/datasets/martj42/international-football-results-from-1872-to-2017)                                                                  | Base de datos abierta | Partidos de fútbol internacional desde 1872 hasta 2023     | **matches**: Carpeta que contiene los partidos.<br>**results.csv**: Archivo con el resultado de los partidos.                                                                                                                                                                                                                                                        |
| [Transfers](https://es.wikipedia.org/wiki/Anexo:Fichajes_más_caros_de_la_historia_del_fútbol#:~:text=Neymar%2C%20el%20fichaje%20más%20caro,del%20Paris%20Saint%2DGermain%20F.%20C.) | Web scrapping         | Datos de los traspasos más caros de la historia del fútbol | **football_players.csv**: Archivo que contiene los fichajes más caros de la historia del fútbol.                                                                                                                                                                                                                                                                     |
| [Football Manager](https://www.kaggle.com/datasets/platinum22/foot-ball-manager-2023-dataset)                                                                                       | Base de datos abierta | Características de los jugadores Videojuego FM 2023        | **FM 2023.csv**: Archivo que almacena el detalle de los juadores de la temporada 2022-2023.                                                                                                                                                                                                                                                                          |

### Fase 3: Preparación de los datos ⚒️
Los datos se han:
- Seleccionado
- Limpiado
- Estructurados
- Integrados
- Formateados

### Fase 4: Modelado 🗂️
| Dataset                    | Descripción                                             | Modelo                                                                                                                                   |
|----------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| **StatsBomb**              | Búsqueda de la probabilidad de victoria de cada jugador | Clasificación multiclase<br>• Características del jugador (nombre, frecuencia de partidos, equipo, nacionalidad)<br>• resultado_partido  |
| **SOFIFA**                 | Búsqueda del jugador con mayor rendimiento              | Regresión<br>• 47 Características del jugador (físicas, rendimiento, evaluación, económicas)<br>• potencial_jugador                      |
| **International Football** | Búsqueda de la probabilidad de goles de cada jugador    | Regresión<br>• Características del partido (torneo, minuto, penalty, equipo)<br>• goles_anotados                                         |
| **Football Manager**       | Búsqueda del jugador con mayor rendimiento              | Regresión<br>• 70 Características del jugador (físicas, rendimiento, evaluación, económicas)<br>• habilidad_actual y habilidad_potencial |

### Fase 5: Evaluación 📊
| Dataset                    | Resultado |
|----------------------------|-----------|
| **StatsBomb**              | 66 %      |
| **SOFIFA**                 | 99 %      |
| **International Football** | 50 %      |
| **Football Manager**       | 100 %     |

### Fase 6: Implantación ☑️
- Monitorización
- Conclusiones
- Líneas futuras

