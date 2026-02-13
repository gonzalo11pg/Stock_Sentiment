# Stock Sentiment Analysis - Versión Mejorada 📊

Análisis avanzado del sentimiento de noticias sobre **Take-Two Interactive** y su correlación con el precio de las acciones.

## 🚀 Nuevas Funcionalidades

### ✅ Implementadas

1. **📊 Análisis de Correlación Estadística**
   - Correlación entre sentimiento y precio de cierre
   - Correlación entre sentimiento y cambio porcentual
   - Análisis con lag temporal (día anterior)

2. **🤖 Predicción con Machine Learning**
   - Modelo de regresión lineal
   - Features: sentimiento, volumen, noticias
   - Métricas: MAE, RMSE, R²

4. **🌐 Análisis de Múltiples Fuentes**
   - Integración con NewsAPI
   - Análisis de keywords específicos
   - Agregación de sentimiento por día

6. **🎮 Detección de Eventos Específicos**
   - Detección automática de menciones de GTA 6
   - Análisis de impacto en sentimiento
   - Marcadores visuales en gráficos

8. **🛠️ Mejoras Técnicas**
   - Manejo robusto de errores
   - Funciones modulares y reutilizables
   - Comentarios detallados en cada sección
   - Configuración centralizada
   - Logging de progreso

## 📦 Instalación

```bash
pip install numpy pandas yfinance nltk vaderSentiment requests scikit-learn matplotlib seaborn
```

## 🎯 Uso

### Opción 1: Ejecutar el script Python

```bash
python Stock_sentiment_improved.py
```

### Opción 2: Usar en Jupyter Notebook

1. Copia cada sección (CELDA) del archivo `.py` en celdas separadas del notebook
2. Ejecuta las celdas en orden

## ⚙️ Configuración

Edita el diccionario `CONFIG` en la **CELDA 3**:

```python
CONFIG = {
    'stock_ticker': 'TTWO',  # Cambiar ticker aquí
    'start_date': '2025-02-05',  # Fecha de inicio
    'news_days': 28,  # Días de noticias
    'api_key': 'TU_API_KEY',  # Tu NewsAPI key
    'search_query': 'Take-Two Interactive',
    'gta_keywords': ['GTA 6', 'GTA VI', 'Grand Theft Auto 6'],
}
```

## 📊 Visualizaciones Generadas

El script genera 6 gráficos:

1. **Precio vs Sentimiento** - Gráfico principal con doble eje Y
2. **Predicciones del Modelo** - Scatter plot de predicciones vs valores reales
3. **Distribución de Sentimiento** - Histograma de scores
4. **Correlación** - Sentimiento vs cambio de precio
5. **Evolución Temporal** - Sentimiento promedio a lo largo del tiempo
6. **Eventos GTA** - Marcadores en fechas con menciones

## 📈 Métricas Calculadas

- **Correlación de Pearson** entre sentimiento y precio
- **MAE** (Mean Absolute Error) del modelo
- **RMSE** (Root Mean Squared Error)
- **R² Score** del modelo predictivo
- **Impacto de eventos** (GTA 6)

## 🔍 Estructura del Código

```
CELDA 1:  Instalación de dependencias
CELDA 2:  Imports y configuración
CELDA 3:  Parámetros configurables
CELDA 4:  Funciones de recopilación de datos
CELDA 5:  Procesamiento de texto y sentimiento
CELDA 6:  Preparación de datos combinados
CELDA 7:  Análisis de correlación
CELDA 8:  Modelo de predicción ML
CELDA 9:  Detección de eventos GTA
CELDA 10: Visualizaciones completas
CELDA 11: Resumen y conclusiones
```

## 💡 Interpretación de Resultados

### Correlación
- **|r| > 0.5**: Correlación fuerte
- **|r| > 0.3**: Correlación moderada
- **|r| < 0.3**: Correlación débil

### R² Score
- **R² > 0.7**: Modelo excelente
- **R² > 0.5**: Modelo bueno
- **R² < 0.5**: Modelo necesita mejoras

## 🎓 Próximas Mejoras Posibles

- [ ] Integración con Twitter/Reddit API
- [ ] Modelos ML más avanzados (Random Forest, LSTM)
- [ ] Dashboard interactivo con Streamlit
- [ ] Alertas automáticas por email
- [ ] Análisis de competidores
- [ ] Backtesting de estrategias de trading

## 📝 Notas

- **NewsAPI** tiene límite de 100 requests/día en plan gratuito
- Los datos de **yfinance** pueden tener delay de 15 minutos
- El análisis de sentimiento usa **VADER**, optimizado para redes sociales

## 🤝 Contribuciones

Este es un proyecto educativo. Siéntete libre de:
- Agregar nuevas fuentes de datos
- Mejorar el modelo de predicción
- Añadir más visualizaciones
- Optimizar el código

## ⚠️ Disclaimer

Este script es solo para fines educativos y de investigación. **No debe usarse como base única para decisiones de inversión**. El mercado de valores es impredecible y conlleva riesgos.

---

**Versión**: 2.0  
**Última actualización**: Febrero 2026  
**Autor**: Análisis de Sentimiento de Acciones
