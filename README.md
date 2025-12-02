# 🛒 Análisis de Patrones de Compra y Comportamiento del Cliente en Instacart

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?logo=python" />
  <img src="https://img.shields.io/badge/Pandas-Limpieza%20%26%20EDA-150458?logo=pandas" />
  <img src="https://img.shields.io/badge/Matplotlib-Visualización-11557c?logo=plotly" />
  <img src="https://img.shields.io/badge/Seaborn-Estadística-9cf?logo=python" />
  <img src="https://img.shields.io/badge/Status-Proyecto%20Completo-success" />
</p>

---

## 📌 Descripción del Proyecto  

Este proyecto analiza el **comportamiento de compra de los usuarios de Instacart**, descubriendo patrones en:

- Frecuencia de pedidos  
- Artículos más comprados  
- Horas y días con mayor actividad  
- Productos más reordenados  
- Tiempos de reposición  
- Hábitos de compra por usuario  

El conjunto de datos fue previamente **reducido y modificado** (se añadieron valores ausentes y duplicados) para simular escenarios reales de análisis y limpieza.

El objetivo es desarrollar un **análisis exploratorio completo (EDA)** y un **preprocesamiento profesional**, justificando cada decisión tomada.

## 🧰 Herramientas Utilizadas

- 🐍 **Python**
- 📚 **Pandas** — integración, limpieza y manipulación  
- 📊 **Matplotlib y Seaborn** — gráficos y visualización  
- 🗂️ **CSV datasets** simulados de Instacart  

## 📁 Estructura de los Datos

- `instacart_orders.csv` — historial de pedidos  
- `products.csv` — catálogo de productos  
- `aisles.csv` — pasillos  
- `departments.csv` — departamentos  
- `order_products.csv` — productos agregados a cada pedido  

El análisis utiliza **unión de tablas**, detección y manejo de:

✔️ duplicados  
✔️ valores ausentes  
✔️ tipos incorrectos  
✔️ relaciones entre claves (order_id, product_id, aisle_id, etc.)  

## 🧪 Etapas Principales del Análisis

### 🔧 1. Preprocesamiento  
- Corrección de tipos de datos  
- Eliminación de duplicados (especialmente en orders)  
- Relleno responsable de nulos (ej. *Unknown* en productos sin nombre)  
- Conservación de NaN cuando tienen significado (primer pedido del cliente)  
- Reemplazo de valores desconocidos en orden de carrito (`999`)

### 📊 2. Análisis Exploratorio de Datos (EDA)

#### 🕒 Comportamiento temporal  
- Los pedidos se concentran **entre 9 a.m. y 5 p.m.**  
- **Domingo y lunes** son los días con más compras  
- La mayoría retorna entre **1 y 9 días**, con ciclos semanales/mensuales

#### 🛍️ Comportamiento del cliente  
- La mayoría hace **entre 5 y 10 productos por pedido**  
- La distribución es sesgada: pocos usuarios compran en grandes cantidades  
- Los usuarios frecuentes generan un patrón estable de consumo

#### 🍌 Productos más comprados  
Los TOP 20 incluyen principalmente:  
Bananas, fresas, leche, aguacates, espinaca, cítricos, productos orgánicos.

#### 🔁 Productos más reordenados  
Alta concentración en productos frescos y básicos:  
Bananas, leche orgánica, limón, frambuesas, etc.

#### 🛒 Primeros artículos del carrito  
El análisis revela que los primeros productos agregados suelen ser:  
Bananas, leche, fresas, aguacates — *productos esenciales*.

## 📈 Análisis avanzado

### ✔️ Tasa de repetición por producto  
- Varios productos tienen **reorder_rate = 1.0**, indicando lealtad total.  

### ✔️ Tasa de repetición por usuario  
- La mayoría de los usuarios repiten productos frecuentemente.  
- Algunos usuarios nunca repiten → muestra perfiles exploradores.

## 🧾 Conclusión General

El análisis revela patrones consistentes de compra:

- Los usuarios realizan **compras regulares**, con reposición semanal/mensual.  
- Los productos frescos y orgánicos dominan las compras y reórdenes.  
- Las rutinas de compra son predecibles según **hora**, **día** y **frecuencia**.  
- La limpieza de datos fue esencial debido a valores ausentes, duplicados y categorías desconocidas.  
- La plataforma Instacart puede aprovechar estos hallazgos para:  
  - Optimizar inventario  
  - Diseñar promociones  
  - Personalizar recomendaciones  
  - Predecir demanda  
