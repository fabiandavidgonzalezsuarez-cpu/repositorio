# 🛜 Laboratorio: Optimalidad y Sink Tree (Johal, 2008)

Aplicación interactiva hecha con **Streamlit** que permite experimentar con el principio de optimalidad y el concepto de *Sink Tree* en redes de computadores, tomando como referencia el artículo de Johal (2008).

A partir de una red de routers (origen **H**, destino **B**), la app calcula la mejor ruta según el criterio elegido, la compara con las rutas estáticas del artículo (PSRC, SSRC y TSRC) y construye el Sink Tree hacia el destino.

## ✨ Funcionalidades

- **Tabla editable de enlaces**: modifica retardo (ms), ancho de banda (Mbps) y disponibilidad de cada enlace.
- **Tres criterios de optimización** (barra lateral):
  - **Johal: mínimo de saltos**: cada enlace cuesta 1.
  - **Mínimo retardo**: se minimiza la suma de retardos.
  - **Multicriterio**: combina saltos (α), retardo (β) y baja capacidad (γ) con pesos ajustables que se normalizan automáticamente.
- **Comparación de rutas**: saltos, retardo total y banda mínima de PSRC, SSRC, TSRC y la ruta óptima calculada con Dijkstra.
- **Sink Tree hacia B**: siguiente salto de cada router para llegar al destino.
- **Visualización de la red** con Plotly.
- **Exportación a CSV** de la tabla de resultados.

## 🗺️ Red de ejemplo

| Ruta | Camino | Saltos |
|------|--------|--------|
| PSRC | H → D → A → B | 3 |
| SSRC | H → E → J → C → B | 4 |
| TSRC | H → O → N → J → C → B | 5 |

## 🚀 Instalación y ejecución

1. Clona el repositorio:

   ```bash
   git clone https://github.com/<tu-usuario>/<tu-repositorio>.git
   cd <tu-repositorio>
   ```

2. (Recomendado) Crea y activa un entorno virtual:

   ```bash
   python -m venv venv
   # Windows
   venv\Scripts\activate
   # Linux / macOS
   source venv/bin/activate
   ```

3. Instala las dependencias:

   ```bash
   pip install -r requirements.txt
   ```

4. Ejecuta la aplicación:

   ```bash
   streamlit run app.py
   ```

   Se abrirá en el navegador, normalmente en `http://localhost:8501`.

## 🧰 Tecnologías

- [Streamlit](https://streamlit.io/): interfaz web
- [NetworkX](https://networkx.org/): grafos y algoritmo de Dijkstra
- [Pandas](https://pandas.pydata.org/): manejo de tablas
- [Plotly](https://plotly.com/python/): visualización de la red

## 📁 Estructura del proyecto

```
.
├── app.py             # Aplicación principal
├── requirements.txt   # Dependencias
└── README.md
```

## 📚 Referencia

Johal (2008), artículo sobre optimalidad de rutas y Sink Tree.

## 📄 Licencia

Proyecto con fines académicos. Añade aquí la licencia que prefieras (por ejemplo, MIT).
