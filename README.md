# 📌 Predicción de Obesidad con Machine Learning

Este proyecto utiliza Machine Learning para predecir el nivel de obesidad de una persona en función de diversos factores como hábitos alimenticios, actividad física y antecedentes familiares. El modelo ha sido entrenado con un conjunto de datos que clasifica a los individuos en diferentes categorías de peso.

---

## 📂 Contenido del Proyecto

- **Google Colab Notebook**: Contiene el código de preprocesamiento, entrenamiento del modelo y predicción.
- **Dataset**: Incluye información sobre hábitos y características de los individuos.
- **Modelo Entrenado**: Se ha utilizado un algoritmo de Random Forest para la predicción.
- **README.md**: Guía para comprender y ejecutar el proyecto.

---

## 📊 Datos Utilizados

El dataset contiene diversas características relevantes, entre ellas:

- `Gender` (Género)
- `Age` (Edad)
- `family_history_with_overweight` (Historial familiar de sobrepeso)
- `FAVC` (Consumo frecuente de comida rápida)
- `FCVC` (Consumo de verduras)
- `NCP` (Número de comidas al día)
- `CAEC` (Consumo de snacks)
- `SMOKE` (Fuma o no)
- `CH2O` (Consumo de agua)
- `FAF` (Frecuencia de actividad física)
- `TUE` (Tiempo usando dispositivos electrónicos)
- `CALC` (Frecuencia de consumo de alcohol)
- `MTRANS` (Modo de transporte)
- `IMC` (Índice de Masa Corporal calculado)
- `NObeyesdad` (Nivel de obesidad - variable objetivo)

---

## 🛠️ Instalación y Uso

1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/tu-usuario/tu-repo.git
   ```
2. **Abrir el notebook en Google Colab**
   - Subir el archivo `.ipynb` a Google Drive
   - Abrir Google Colab y cargar el notebook
3. **Instalar dependencias necesarias**
   ```python
   !pip install numpy pandas scikit-learn
   ```
4. **Ejecutar el notebook paso a paso**
   - Cargar el dataset
   - Aplicar preprocesamiento y normalización
   - Entrenar el modelo
   - Hacer predicciones

---

## 🤖 Modelo Utilizado

Se ha utilizado un **Random Forest Classifier**, un algoritmo de aprendizaje supervisado que ofrece buenos resultados en problemas de clasificación multiclase. Se realizaron las siguientes etapas:

1. **Preprocesamiento**: Se codificaron variables categóricas con `LabelEncoder` y se normalizaron los datos numéricos.
2. **Entrenamiento**: Se entrenó el modelo con un 80% de los datos y se validó con el 20% restante.
3. **Evaluación**: Se utilizó la matriz de confusión para analizar el rendimiento del modelo.
4. **Predicción**: Se ingresan nuevos datos y se obtiene la categoría de obesidad.

---

## 📈 Interpretación de Predicciones

La predicción del modelo devuelve un número que representa un nivel de obesidad, mapeado a las siguientes categorías:

| Código | Clasificación de Obesidad | Traducción |
|--------|----------------------------|------------|
| 0      | Insufficient_Weight        | Peso insuficiente |
| 1      | Normal_Weight              | Peso normal |
| 2      | Obesity_Type_I             | Obesidad Tipo I |
| 3      | Obesity_Type_II            | Obesidad Tipo II |
| 4      | Obesity_Type_III           | Obesidad Tipo III |
| 5      | Overweight_Level_I         | Sobrepeso Nivel I |
| 6      | Overweight_Level_II        | Sobrepeso Nivel II |

Ejemplo de salida:
```python
Predicción para el nuevo dato: ['Normal_Weight']
```

---

## 📌 Resultados y Métricas

El modelo se evaluó utilizando la **matriz de confusión** y la **precisión**:
```python
from sklearn.metrics import accuracy_score

# Calcular precisión
accuracy = accuracy_score(y_test, y_pred)
print(f"Precisión del modelo: {accuracy * 100:.2f}%")
```

La matriz de confusión nos ayuda a analizar los verdaderos positivos (TP), falsos positivos (FP), verdaderos negativos (TN) y falsos negativos (FN) en cada categoría de obesidad.

---

## 📌 Contribuciones y Contacto

Si deseas contribuir o tienes dudas, puedes contactarme en:
📧 Correo: [ingdres.rodriguez@gmail.com]
📌 GitHub: [Andres-Nicolas]

¡Espero que este proyecto sea útil para entender cómo predecir niveles de obesidad con Machine Learning! 🚀

