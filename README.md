# 🏆 Simulador Predictivo del Mundial 2026

Este repositorio contiene un modelo de Machine Learning y simulación estocástica diseñado para predecir los resultados de la Copa Mundial de la FIFA 2026. 

El sistema combina el aprendizaje automático para estimar el rendimiento esperado de los equipos y distribuciones probabilísticas para simular la naturaleza impredecible del fútbol en un entorno de torneo.

## 🧠 Arquitectura del Modelo

El proyecto se divide en tres fases fundamentales:
1. **Machine Learning (Random Forest Regressor):** Se entrenaron dos modelos independientes con datos históricos para predecir la cantidad de goles (xG o Esperanza Matemática) que marcará el equipo local y el visitante.
2. **Capa Estocástica (Distribución de Poisson):** Las predicciones fraccionales del modelo se utilizan como el parámetro $\lambda$ en una distribución de Poisson para generar resultados de goles discretos y realistas, permitiendo empates y resoluciones por penales.
3. **Simulación de Monte Carlo:** El motor del torneo se ejecuta 1,000 veces para calcular las probabilidades reales que tiene cada selección de coronarse campeona.

## 📂 Estructura de los Datos

Los datos históricos, estadísticas de rendimiento y valor de mercado no están incluidos directamente en el código fuente. 

Para ejecutar el modelo, debes contar con los siguientes archivos `.csv` y colocarlos dentro de la carpeta `/data/`:
* `datos_mundial.csv`
* `datos_historicos.csv`
* `partidos.csv`
* `Grupos_Mundial.csv`
* `ranking_fifa.csv`
* `transfermarkt.csv`

## ⚙️ Instalación y Requisitos

Para reproducir los resultados de este proyecto de manera local, asegúrate de tener Python 3.8 o superior instalado.

1. Clona este repositorio:
   ```bash
   git clone [https://github.com/TU_USUARIO/simulador-mundial-2026.git](https://github.com/TU_USUARIO/simulador-mundial-2026.git)
   cd simulador-mundial-2026
