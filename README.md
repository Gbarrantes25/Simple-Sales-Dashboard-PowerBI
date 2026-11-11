# 📊 Simple Sales Dashboard

[![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-0078D4?style=flat&logo=microsoft&logoColor=white)](https://learn.microsoft.com/en-us/dax/)
[![Power Query](https://img.shields.io/badge/Power%20Query-0078D4?style=flat&logo=microsoft&logoColor=white)](https://learn.microsoft.com/en-us/power-query/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Version](https://img.shields.io/badge/Version-1.0-blue.svg)]()

---

## 📋 Tabla de Contenidos

- [Descripción General](#-descripción-general)
- [Características Principales](#-características-principales)
- [Contenido del Proyecto](#-contenido-del-proyecto)
- [Herramientas y Tecnologías](#️-herramientas-y-tecnologías-utilizadas)
- [Configuración del Entorno](#️-configuración-del-entorno)
- [Estructura del Repositorio](#-estructura-del-repositorio)
- [Medidas DAX Implementadas](#-medidas-dax-implementadas)
- [Vistas Previas](#️-vistas-previas-del-proyecto)
- [Autor](#-autor)
- [Licencia](#-licencia)

---

## 📃 Descripción General

Dashboard de **Ventas Simplificado** desarrollado en Power BI, diseñado para analizar unidades y productos vendidos por representante de ventas de manera clara y directa. Este proyecto transforma datos de transacciones comerciales en información visual interactiva mediante:

- 📊 **Vista Única:** Resumen de ventas por vendedor con KPIs principales.
- 👥 **Fotos de Vendedores:** Imágenes personalizadas para cada representante de ventas.
- 🎨 **Diseño Personalizado:** Lienzo con fondo personalizado (Boxy sections) y diseño adaptable (Desktop y Mobile).
- 📈 **KPIs de Ventas:** 3 medidas DAX esenciales (unidades vendidas, productos distintos, porcentajes de participación).
- 🖱️ **Navegación Interactiva:** Segmentación de datos y botones con imágenes para una experiencia de usuario fluida.

---

## ✨ Características Principales

### 🔄 Transformaciones en Power Query
- Procesos de limpieza y modelado de datos para optimizar el rendimiento.
- Unificación de fuentes de datos CSV en un modelo relacional coherente.

### 📐 Modelo de Datos
- **Tablas Principales:** `Ventas`, `Productos` y `Vendedores`.
- Relaciones optimizadas entre las tablas para permitir un análisis multidimensional eficiente de las métricas de ventas.

### 🎨 Diseño Interactivo
- Navegación intuitiva con botón de borrado de filtros.
- Segmentación de datos dinámica por representante.
- Uso de segmentación de botones (Button Slicer) para mostrar imágenes de los vendedores.
- Diseño responsivo con vistas específicas optimizadas para Desktop y Mobile.

---

## 📊 Contenido del Proyecto

| Página | Descripción | Contenido Principal |
|--------|-------------|---------------------|
| **Resumen** | Vista consolidada ejecutiva | KPIs globales de ventas, fotos de vendedores, unidades vendidas y porcentaje de participación por representante. |

---

## 🛠️ Herramientas y Tecnologías Utilizadas

### Software Requerido
- **Power BI Desktop** (versión más reciente)

### Fuente de Datos
- 📄 Archivos CSV en la carpeta `Fuente de Datos/`:
  - `Productos.csv`
  - `Vendedores.csv`
  - `Ventas.csv`

### Lenguajes y Tecnologías
- **DAX** - Cálculo de medidas y KPIs de ventas.
- **Power Query (Lenguaje M)** - Transformación, limpieza y estructuración de los datos CSV.

---

## ⚙️ Configuración del Entorno

### Prerequisitos
1. Descargar e instalar [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

### Paso 1: Obtener el Proyecto
1. Clonar o descargar el repositorio completo.
2. Ubicar el archivo `Simple Sales.pbix`.

### Paso 2: Cargar y Actualizar Datos
1. Abrir el archivo en Power BI Desktop.
2. Navegar a la pestaña **Inicio** en la cinta de opciones.
3. Hacer clic en el botón **Actualizar** (Refresh) para cargar los datos desde los archivos CSV configurados en la carpeta `Fuente de Datos`.
4. Si las rutas de los archivos cambian, ir a **Transformar datos** > **Configuración de origen de datos** y actualizar las rutas locales.

---

## 📂 Estructura del Repositorio

```text
.
├── Fuente de Datos/                  # Contiene los archivos de datos de ejemplo (.CSV)
│   ├── Productos.csv
│   ├── Vendedores.csv
│   └── Ventas.csv
├── Fotos/                            # Contiene las fotos de los vendedores
├── Dashboard (Boxy con foto).svg     # Archivo de fondo personalizado para el lienzo del reporte
├── Simple Sales.pbix                 # Archivo ejecutable de Power BI
├── Demo.gif                          # Demostración animada del funcionamiento del dashboard
├── .gitignore                        # Archivo de configuración Git
└── README.md                         # Este archivo de documentación
```

## 🧮 Medidas DAX Implementadas
El proyecto utiliza medidas DAX fundamentales para el análisis de ventas, enfocadas en totales, conteos distintos y porcentajes de participación.

<details>
<summary>Ver medidas DAX del proyecto</summary>

#### 📈 Métricas de Ventas
Unidades Vendidas
Calcula la suma total de unidades vendidas en el contexto filtrado.

```dax
Unidades Vendidas = SUM(Ventas[Unidades])
```

Productos Distintos
Cuenta la cantidad única de productos vendidos basándose en su código.
```dax
Productos Distintos = DISTINCTCOUNT(Ventas[CódigoProducto])
```

Porcentaje de Ventas
Calcula el porcentaje de participación de las unidades vendidas por un representante en relación con el total general de la organización.

```dax
Porcentaje de Ventas = 
DIVIDE(
    [Unidades Vendidas],
    CALCULATE([Unidades Vendidas], ALL(Vendedores[Representante]))
)
```

</details>

## 🖼️ Vistas Previas del Proyecto
<details>
<summary>📸 Ver Capturas de Pantalla</summary>

<img width="1777" alt="Vista de Escritorio" src="https://github.com/user-attachments/assets/73e82d59-e64d-4c56-8c8a-3e1232fdb825" />
<img width="538" alt="Vista Mobile 1" src="https://github.com/user-attachments/assets/e60adaf3-ddf0-4acf-af04-f10324ac0c70" />
<img width="541" alt="Vista Mobile 2" src="https://github.com/user-attachments/assets/f585bc48-3841-4113-8d1b-f1e0090fbb82" />
</details>

<details>
<summary>🎥 Ver Video Demostrativo</summary>

   
   Ver en YouTube: -
</details>

## 👤 Autor
Giancarlo Barrantes

Business Intelligence Developer | Power BI Specialist


<a href="https://www.linkedin.com/in/gb25"><img width="70" height="20" alt="image" src="https://github.com/user-attachments/assets/e0d69586-c6f9-4f66-9a3d-bc8dfa146463" /></a>
<a href="https://www.instagram.com/gbarrantes25"><img width="70" height="20" alt="image" src="https://github.com/user-attachments/assets/68773029-5e0f-49da-92e9-fb93a223dd09" />
</a>
<a href="https://www.tiktok.com/@gbarrantes25"><img width="65" height="20" alt="image" src="https://github.com/user-attachments/assets/349c87c0-1f3a-4368-8517-64a6012565c0" /></a>
<a href="https://www.youtube.com/@gbarrantes25"><img width="70" height="20" alt="image" src="https://github.com/user-attachments/assets/d9e2cb69-29ec-47fc-93ae-30896a7b533d" />
</a>

## 📝 Licencia
Este proyecto está bajo la Licencia MIT - ver el archivo <a href="https://mit-license.org/">LICENSE</a> para más detalles.

## ⭐ Agradecimientos
Si este proyecto te resultó útil, considera darle una ⭐ en GitHub y compartirlo con otros profesionales de Business Intelligence.

<div align="center">
   Hecho por <a href="https://gbarrantes25.github.io/">Giancarlo Barrantes</a>
</div>