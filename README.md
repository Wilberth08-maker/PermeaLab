# 🧪 PermeaLab — Simulador Interactivo de Permeabilidad (Carga Constante)

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?style=flat&logo=javascript&logoColor=black)
![SVG](https://img.shields.io/badge/Gráficos-SVG_Dinámico-0284C7?style=flat)
![Ingeniería Civil](https://img.shields.io/badge/Ingeniería_Civil-Geotecnia-059669?style=flat)
![Licencia](https://img.shields.io/badge/Licencia-CC_BY--NC_4.0-lightgrey?style=flat)

Aplicación web interactiva autocontenida para la simulación visual y el cálculo experimental del **coeficiente de permeabilidad (K)** en suelos granulares mediante un **permeámetro de carga constante**, basada en la **Ley de Darcy** y los lineamientos de la norma **ASTM D2434**.

> **Proyecto desarrollado para la enseñanza y demostración experimental en Mecánica de Suelos e Hidráulica Subterránea.**

---

## ✨ Características Principales

- **Lienzo Vectorial Interactivo (SVG):**
  - Manipulación directa en tiempo real: arrastra verticalmente el recipiente de **Suelo (h₁)** o el tanque de **Agua (h₂)** para modificar las cargas hidráulicas.
  - **Cinta métrica central** con líneas guía proyectadas desde los niveles libres (∇) y acotación dinámica de la pérdida de carga (ΔH).
  - **Inversión automática de flujo:** las flechas internas en la muestra, el sentido de circulación en la manguera en "U" y la ubicación del caudalímetro de descarga (`Q salida`) cambian automáticamente entre **flujo ascendente (h₂ > h₁)**, **flujo descendente (h₁ > h₂)** y **equilibrio hidrostático (ΔH = 0)**.
- **Doble Modo de Operación Física:**
  1. **Ensayo de Laboratorio (Calcular K):** Permite ingresar mediciones reales de caudal directo (Q) o mediante volumen recolectado y tiempo (V / t) para despejar K.
  2. **Demostración Física (K constante):** Fija la conductividad hidráulica de la muestra y recalcula en vivo el caudal resultante (`Q = K · i · A`) al variar la altura de los recipientes.
- **Herramientas de Diagnóstico Geotécnico:**
  - **Clasificación automática del suelo** según órdenes de magnitud clásicos (Casagrande / Terzaghi–Peck).
  - **Alerta de gradiente hidráulico crítico (i_c ≈ 1.0):** detecta condiciones de ebullición o sifonamiento (*quick condition*) en flujo ascendente.
  - **Estandarización por temperatura (K₂₀):** corrige el efecto de la viscosidad dinámica del agua a 20 °C.
  - **Conversión de unidades:** soporte instantáneo entre sistema de laboratorio (`cm`, `cm³/s`, `cm/s`) y Sistema Internacional (`m`, `m³/s`, `m/s`), además de desglose matemático paso a paso.

---

## 📐 Fundamento Matemático

El simulador resuelve en tiempo real las ecuaciones fundamentales del flujo laminar unidimensional en medios porosos saturados:

```text
Área transversal de la muestra:
A = (π · D²) / 4

Gradiente hidráulico:
i = ΔH / L = |h₂ − h₁| / L

Conductividad hidráulica (Ley de Darcy):
K = (Q · L) / (A · ΔH)

Corrección por temperatura a 20 °C (ASTM D2434):
K₂₀ = K_T · (μ_T / μ₂₀)
```

---

## 🚀 Ejecución Local

El proyecto no requiere dependencias externas, servidores ni compilación; toda la aplicación reside en un único archivo `index.html`.

1. Clona este repositorio:
   ```bash
   git clone [https://github.com/Wilberth08-maker/PermeaLab.git](https://github.com/Wilberth08-maker/PermeaLab.git)
   ```
2. Abre la carpeta del proyecto y haz doble clic sobre `index.html` para ejecutarlo en cualquier navegador moderno.

---

## 👨‍💻 Autoría y Licencia

Diseñado y desarrollado por **Wilberth Adair Martínez Puc** · **IngeTerra** (2026).

Este proyecto se distribuye bajo la licencia **[Creative Commons Atribución-NoComercial 4.0 Internacional (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/deed.es)**:
- ✅ **Libre uso educativo y académico:** puedes usarlo, compartirlo y adaptarlo citando al autor original.
- ❌ **Uso no comercial:** queda prohibida su venta o explotación con fines de lucro.
