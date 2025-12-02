# Ejercicio 3 - Tailwind CSS v4.1

Este proyecto es una conversión del **Ejercicio 2** (que usaba SCSS/SASS) a **Tailwind CSS v4.1**.

## Cambios Principales

### 1. Migración de SCSS a Tailwind CSS v4.1

- Se eliminaron todos los archivos SCSS (`_base.scss`, `_layout.scss`, `_module.scss`, `_theme.scss`, `_state.scss`)
- Se creó un archivo `src/input.css` que utiliza la nueva sintaxis de Tailwind CSS v4 con `@theme`
- Todas las clases personalizadas se convirtieron a utility classes de Tailwind

### 2. Configuración de Tailwind CSS v4

El archivo `src/input.css` utiliza las nuevas características de Tailwind CSS v4:

- **@theme**: Define variables CSS personalizadas para colores, fuentes y espaciado
- **@layer utilities**: Añade utilidades personalizadas como `text-shadow-sm`
- **@layer components**: Define componentes reutilizables como `container-custom`

### 3. Conversión de HTML

Todos los archivos HTML han sido actualizados para usar utility classes de Tailwind:

- `index.html` - Página principal con hero, galería de eventos, carousel y parallax
- `eventos.html` - Listado completo de eventos
- `evento-detalle.html` - Página de detalle de un evento específico

### 4. Modo Oscuro

El modo oscuro se mantiene funcional mediante:

- Clases CSS personalizadas en `src/input.css` para `body.dark-mode`
- El mismo JavaScript de `main.js` que alterna la clase `dark-mode`

## Estructura del Proyecto

```
ejercicio3/
├── assets/          # Imágenes (copiadas de ejercicio2)
├── css/
│   └── style.css    # CSS compilado por Tailwind
├── js/
│   └── main.js      # JavaScript (copiado de ejercicio2)
├── src/
│   └── input.css    # Archivo fuente de Tailwind CSS v4
├── index.html
├── eventos.html
├── evento-detalle.html
├── package.json
└── README.md
```

## Instalación y Uso

### Instalar dependencias

```bash
npm install
```

### Compilar CSS (producción)

```bash
npm run build
```

### Modo desarrollo (watch)

```bash
npm run dev
```

## Características de Tailwind CSS v4 Utilizadas

1. **@theme**: Configuración de tema personalizado con variables CSS
2. **Utility-first**: Todas las clases son utilities de Tailwind
3. **Responsive Design**: Breakpoints `md:` y `lg:` para diseño adaptable
4. **Custom Properties**: Variables CSS para colores, fuentes y espaciado
5. **Dark Mode**: Implementado con clases personalizadas

## Diferencias con Ejercicio 2

| Aspecto       | Ejercicio 2 (SCSS) | Ejercicio 3 (Tailwind v4)      |
| ------------- | ------------------ | ------------------------------ |
| Preprocesador | SCSS/SASS          | Tailwind CSS v4                |
| Clases        | BEM + Custom       | Utility-first                  |
| Variables     | SCSS variables     | CSS Custom Properties (@theme) |
| Compilación   | sass --watch       | tailwindcss CLI                |
| Tamaño CSS    | ~8KB               | ~18KB (con utilities)          |

## Ventajas de Tailwind CSS v4

- ✅ No necesita archivo `tailwind.config.js`
- ✅ Configuración más simple con `@theme`
- ✅ Mejor rendimiento en compilación
- ✅ Utility classes más consistentes
- ✅ Menor curva de aprendizaje para nuevos desarrolladores

## Notas Técnicas

- **Versión de Tailwind**: v4.1.17 (alpha)
- **Package usado**: `@tailwindcss/cli`
- **Compatibilidad**: Todos los navegadores modernos
- **JavaScript**: Sin cambios respecto a ejercicio2

---

**Autor**: Conversión realizada con Tailwind CSS v4.1  
**Fecha**: Diciembre 2025
