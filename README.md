# Supermercado - Proyecto Final

## Descripción del Proyecto
Sitio web de ecommerce para supermercado con listado de productos por categorías. Diseño simple, limpio y funcional.

## Estructura del Proyecto
```
supermercado-proyecto/
├── assets/
│   └── css/
│       ├── style.css              # Estilos globales y base
│       ├── product-categories.css # Contenedores y layouts
│       └── product-card.css       # Estilos de cards de productos
├── products/
│   └── aparatos-electronicos.html # Página de categoría
└── README.md
```

## Detalle de Archivos CSS

### 📄 **style.css** - Estilos Globales
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: "Poppins", sans-serif;
    font-weight: 400;
    background-color: white;
    color: #333;
    line-height: 1.6;
}

header {
    background-color: #f8f9fa;
    padding: 30px 20px;
    border-bottom: 1px solid #e5e5e5;
    margin-bottom: 40px;
}

header h1 {
    font-size: 28px;
    font-weight: 700;
    color: #333;
    text-align: center;
    max-width: 1200px;
    margin: 0 auto;
}

.main-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

button {
    background-color: #2563eb;
    color: white;
    border: none;
    padding: 12px 24px;
    border-radius: 8px;
    font-size: 14px;
    font-weight: 500;
    cursor: pointer;
    font-family: inherit;
}

button:hover {
    background-color: #1d4ed8;
}
```

### 📄 **product-categories.css** - Contenedores y Layouts
```css
/* Contenedores y layout de productos */
.products-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

.products-grid {
    display: grid;
    grid-template-columns: 1fr;
    gap: 30px;
}
```

### 📄 **product-card.css** - Estilos de Cards
```css
/* Card del producto */
.product-card {
    background: white;
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 20px;
    display: grid;
    grid-template-columns: 180px 1fr 140px;
    gap: 25px;
    align-items: center;
}

/* Imagen */
.product-card .img {
    background: #f5f5f5;
    padding: 15px;
    border-radius: 8px;
}

.product-card .img img {
    max-width: 150px;
    height: auto;
}

/* Información */
.product-info h3 {
    font-size: 22px;
    font-weight: 600;
    color: #333;
    margin-bottom: 10px;
}

.product-info .description {
    font-size: 16px;
    color: #666;
    line-height: 1.5;
}

/* Compra */
.product-buy {
    text-align: center;
}

.product-buy .price {
    font-size: 28px;
    font-weight: 700;
    color: #2563eb;
    margin-bottom: 15px;
}

.product-buy button {
    width: 100%;
    padding: 12px 20px;
    font-size: 16px;
    font-weight: 600;
}
```

## Guía de Estilos y Convenciones

### 🎨 **Principios de Diseño**
- **Simplicidad**: CSS simple y directo, sin variables complejas
- **Fondo blanco**: Toda la página debe mantener fondo blanco
- **Sin responsive**: Diseño horizontal fijo para todas las pantallas
- **Sin estados especiales**: No hay productos deshabilitados, agotados o destacados

### 📝 **Convenciones de CSS**

#### **Nomenclatura de Clases**
- **Contenedores**: Usar sufijo `-container` solo para elementos que realmente contengan otros elementos
  - ✅ `.products-container` - Contenedor principal de productos
  - ✅ `.main-container` - Contenedor principal de página
  - ❌ `.products-grid-container` → `.products-grid` - Es un grid, no un contenedor

#### **Organización de Archivos CSS**
1. **`style.css`**: Estilos globales, reset, tipografía, header, botones
2. **`product-categories.css`**: Contenedores y layouts de productos
3. **`product-card.css`**: Solo estilos de la card individual del producto

#### **Valores CSS**
- **Colores directos**: `#333`, `#666`, `#2563eb`, `white`, `#f5f5f5`
- **Espaciado directo**: `20px`, `15px`, `30px` (sin variables)
- **Sin media queries**: Diseño fijo sin responsive
- **Sin hover effects**: Mantener interacciones mínimas

### 🏗️ **Estructura HTML**

#### **Layout de Productos**
```html
<main class="products-container">
  <div class="products-grid">
    <div class="product-card">
      <div class="img">
        <img src="..." alt="..." />
      </div>
      <div class="product-info">
        <h3>Título del Producto</h3>
        <p class="description">Descripción...</p>
      </div>
      <div class="product-buy">
        <div class="price">Q0,000</div>
        <button type="button">Comprar</button>
      </div>
    </div>
  </div>
</main>
```

#### **Grid Layout Fijo**
- **3 columnas**: `180px 1fr 140px` (imagen + info + compra)
- **Gap**: `25px` entre columnas
- **Alineación**: `align-items: center`

### 🚫 **Qué NO Incluir**
- ❌ Variables CSS (`--variable`)
- ❌ Media queries (`@media`)
- ❌ Estados deshabilitados (`:disabled`, `.out-of-stock`)
- ❌ Hover effects complejos
- ❌ Animaciones o transiciones
- ❌ Productos destacados (`.featured`)
- ❌ Lazy loading (`loading="lazy"`)
- ❌ Comentarios HTML innecesarios

### ✅ **Qué SÍ Incluir**
- ✅ CSS simple y directo
- ✅ Tipografía Poppins
- ✅ Layout horizontal fijo
- ✅ Colores y espaciado consistentes
- ✅ Estructura HTML limpia
- ✅ Nomenclatura clara de clases

### 🎯 **Tipografía**
- **Fuente**: Poppins (Google Fonts)
- **Títulos**: 22px, font-weight: 600
- **Descripción**: 16px, color: #666
- **Precios**: 28px, font-weight: 700, color: #2563eb
- **Botones**: 16px, font-weight: 600

### 🎨 **Colores**
- **Fondo**: `white`
- **Texto principal**: `#333`
- **Texto secundario**: `#666`
- **Primario**: `#2563eb`
- **Bordes**: `#ddd`
- **Fondo de imagen**: `#f5f5f5`
- **Header**: `#f8f9fa`

## Prompt para IA

Cuando trabajes en este proyecto, sigue estas reglas estrictas:

1. **Mantén CSS simple**: Usa valores directos, sin variables complejas
2. **Fondo blanco siempre**: Toda la página debe tener fondo blanco
3. **Sin responsive**: Diseño horizontal fijo para todas las pantallas
4. **Sin estados especiales**: No agregues productos deshabilitados o destacados
5. **Nomenclatura clara**: Solo usa `-container` para verdaderos contenedores
6. **Organización**: Respeta la separación de responsabilidades entre archivos CSS
7. **HTML limpio**: Estructura simple sin divs innecesarios
8. **Sin hover effects**: Mantén interacciones mínimas

El objetivo es un código simple, mantenible y funcional para un ecommerce básico.
