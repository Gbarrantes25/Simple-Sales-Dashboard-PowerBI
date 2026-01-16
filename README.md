# Simple Sales Dashboard

## 📃 Descripción General
Diseñado para analizar las unidades y productos vendidos por vendedor.

## 📊 Contenido del proyecto
- Página de resumen: Ofrece una vista consolidada de toda la infortación relevante de los vendedores de la organización.
- Botón de borrado de filtro.
- Fotos del vendededor.



## 🛠️ Herramientas y Tecnologías Utilizadas
- Visualización: Power BI Desktop.
- Fuente de Datos:
  - [Productos.csv](https://raw.githubusercontent.com/Gbarrantes25/Simple-Sales-Dashboard-PowerBI/refs/heads/main/Fuentes%20de%20datos/Productos.csv)
  - [Vendedores.csv](https://raw.githubusercontent.com/Gbarrantes25/Simple-Sales-Dashboard-PowerBI/refs/heads/main/Fuentes%20de%20datos/Vendedores.csv)
  - [Ventas.csv](https://raw.githubusercontent.com/Gbarrantes25/Simple-Sales-Dashboard-PowerBI/refs/heads/main/Fuentes%20de%20datos/Ventas.csv)
 
    
- Lenguajes: DAX para las medidas calculadas y Power Query (Lenguaje M) para la transformación de datos.


## ⚙️ Configuración del Entorno
- Software Necesario: Power BI Desktop.
- Instalación:
  - Descargar [Ventas.pbix](https://github.com/Gbarrantes25/Simple-Sales-Dashboard-PowerBI/raw/refs/heads/main/Ventas.pbix) con Power BI Desktop.
  - Entrar a Inicio y darle click a "Actualizar".


## 📂 Estructura del Repositorio
<code>.
  ├── Fuente de Datos/                  # Contiene los archivos de datos de ejemplo (.CSV)
  |── Fotos/                            # Contiene las fotos de los vendedores.
  ├── Dashboard (Boxy con foto).svg     # Es el archivo de fondo del lienzo del proyecto.
  ├── Ventas.pbix                       # Archivo que será ejecutado con Power BI Desktop.
  |—— Demo.gif                          # Demo del proyecto.
  └── README.md                         # Este archivo
</code>


## ✅ Características Principales
- Transformaciones en Power Query: Se realizaron procesos de limpieza y modelado de datos para optimizar el rendimiento.
- Medidas DAX:
  - <code>Unidades Vendidas = SUM(Ventas[Unidades])</code>
  - <code>Productos Distintos = DISTINCTCOUNT(Ventas[CódigoProducto])</code>
  - <code>Porcentaje de Ventas = DIVIDE([Unidades Vendidas],CALCULATE([Unidades Vendidas],ALL(Vendedores[Representante])))</code>
- Diseño Interactivo: Uso de segmentación de datos y segmentación de botones para agregar imagen.


## 🖼️ Vistas Previas del proyecto
<details>
  <summary>Escritorio</summary>
  <img width="1777" height="978" alt="image" src="https://github.com/user-attachments/assets/73e82d59-e64d-4c56-8c8a-3e1232fdb825" />

  
  ![Animation3](https://github.com/user-attachments/assets/fd509d4a-eeef-4206-959d-5f0a31f5e1ab)
</details>
<details>
  <summary>Mobile</summary>
  <img width="538" height="886" alt="image" src="https://github.com/user-attachments/assets/e60adaf3-ddf0-4acf-af04-f10324ac0c70" />
  <img width="541" height="916" alt="image" src="https://github.com/user-attachments/assets/f585bc48-3841-4113-8d1b-f1e0090fbb82" />
</details>


## 👤 Autor
- Giancarlo Barrantes
- Lima, Perú
- [Linkedin](https://www.linkedin.com/in/gb25/)

