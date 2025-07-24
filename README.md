# predicting_stock_prices

# 📈 Stock Price Prediction with Machine Learning

Este proyecto utiliza técnicas de aprendizaje automático para predecir el precio futuro de acciones con base en datos históricos del mercado financiero. A través de un modelo de regresión lineal, se analizan variables como apertura, cierre, volumen y retornos diarios para estimar el comportamiento futuro del precio de una acción, apoyando así la toma de decisiones en inversiones.

---

## 📌 Objetivo

Construir un modelo de regresión capaz de predecir el precio de cierre del día siguiente y generar una proyección de precios para los próximos 10 días hábiles, utilizando Python y bibliotecas como `pandas`, `scikit-learn`, `matplotlib` y `yfinance`.

---

## 🧠 Metodología

1. **Obtención y preparación de datos**  
   Se utiliza la librería `yfinance` para descargar precios históricos de acciones (ej. Autodesk - ADSK).  
   Se calculan nuevas variables como retornos diarios y el precio del siguiente día.

2. **Visualización de datos**  
   El script `plot_stock_data` genera gráficos de:
   - Retornos diarios
   - Precios de apertura, máximo y mínimo
   - Volumen de transacciones

   <p align="center">
     <img src="/images/Plot1.png" alt="Gráficos del comportamiento histórico de la acción">
   </p>

3. **Entrenamiento del modelo de regresión**  
   `linear_regression_model` entrena un modelo con las variables relevantes y evalúa su desempeño usando:
   - **MSE (Mean Squared Error)**
   - **R² (Coeficiente de determinación)**

4. **Predicción futura**  
   `predict_future_prices` extrapola los datos más recientes usando cambios porcentuales promedio, generando predicciones para los próximos 10 días hábiles.

---

## 🧩 Funciones clave

### `plot_stock_data(data, colors)`
Genera una visualización completa del comportamiento histórico de la acción, incluyendo retornos, precios y volumen.

### `linear_regression_model(data, colors)`
Entrena y evalúa un modelo de regresión lineal para predecir el precio del día siguiente.  
Devuelve el modelo entrenado.

### `predict_future_prices(model, data, colors)`
Proyecta los precios futuros basándose en tendencias recientes y los predice usando el modelo entrenado.

---

## 📚 Requisitos

- Python 3.8+
- pandas
- numpy
- matplotlib
- scikit-learn
- yfinance
- pandas_market_calendars (opcional para días hábiles)
- `from pandas.tseries.offsets import BDay` (para fechas hábiles)

Instalación rápida:

```bash
pip install pandas numpy matplotlib scikit-learn yfinance
