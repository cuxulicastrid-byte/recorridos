# Recorridos · Árboles y Grafos

Proyecto final del curso de **Matemática Discreta** — Universidad del Valle de Guatemala, Campus Altiplano.

Aplicación web que permite:

1. **Árboles:** simular una pequeña base de datos con un árbol binario de búsqueda (insertar, buscar y eliminar registros) y recorrerlo en **preorden, inorden y posorden** con animación paso a paso, pila de llamadas y pseudocódigo.
2. **Grafos:** dibujar un grafo ponderado y encontrar el **camino más corto con Dijkstra**. Los pesos pueden ser distancias o, como en **OSPF**, un costo calculado a partir del ancho de banda (`costo = referencia ÷ ancho de banda`).

## Cómo abrirlo

**Opción A (recomendada):** abrir la carpeta en VS Code, instalar la extensión *Live Server* (VS Code la sugiere automáticamente) y hacer clic derecho en `index.html` → **Open with Live Server**.

**Opción B:** hacer doble clic en `index.html`. No necesita servidor ni instalaciones.

## Estructura

```
arboles-grafos/
├── index.html               Página principal (3 pestañas)
├── css/
│   ├── base.css             Variables de color, tipografía y reset
│   ├── layout.css           Estructura de la página y diseño adaptable
│   └── componentes.css      Botones, tarjetas, tablas y estilos del SVG
└── js/
    ├── utils.js             Funciones de apoyo (SVG, avisos, archivos)
    ├── animador.js          Reproduce pasos con pausa y velocidad
    ├── app.js               Navegación entre pestañas
    ├── arbol/
    │   ├── arbol-bst.js     Modelo del árbol binario de búsqueda
    │   ├── arbol-vista.js   Dibujo del árbol en SVG
    │   └── arbol-app.js     Controlador del módulo de árboles
    └── grafo/
        ├── grafo.js         Modelo del grafo y algoritmo de Dijkstra
        ├── ejemplos.js      Grafos de ejemplo
        ├── grafo-vista.js   Dibujo del grafo en SVG
        └── grafo-app.js     Controlador del módulo de grafos
```

Cada módulo separa **modelo** (lógica pura), **vista** (dibujo) y **controlador** (eventos de la interfaz).

## Uso rápido

### Árboles
- Escriba una clave (y un dato opcional) y presione **Insertar**. También puede pegar una lista: `50, 30, 70, 20:Cable`.
- Elija **Preorden / Inorden / Posorden** y presione **Reproducir** o **Paso**.
- La tabla de registros siempre aparece ordenada por clave, que es exactamente el recorrido inorden.

### Grafos
| Herramienta | Tecla | Acción |
|---|---|---|
| Mover | `V` | Arrastrar nodos, clic en un peso para editarlo, doble clic en un nodo para renombrarlo |
| Nodo | `N` | Clic en el lienzo para crear un nodo |
| Arista | `C` | Clic en dos nodos para unirlos |
| Borrar | `D` | Clic en un nodo o arista para eliminarlo |

Elija origen y destino y presione **Reproducir** para ver el algoritmo paso a paso con su tabla y bitácora, o **Resultado** para ver la respuesta directa.

El trabajo se guarda automáticamente en el navegador y se puede **exportar/importar como JSON**.

## Tecnologías
HTML, CSS y JavaScript puro (sin librerías). Los diagramas se dibujan con SVG.
