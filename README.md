```markdown
# ITCSS Project Structure

Este proyecto utiliza la metodología **ITCSS (Inverted Triangle CSS)** para organizar y estructurar las hojas de estilo de manera escalable y manejable.

## ¿Qué es ITCSS?

**ITCSS** organiza el código CSS en niveles, desde lo más global y abstracto hasta lo más específico y particular. Esto se representa como un triángulo invertido, donde las capas superiores tienen un impacto amplio y las inferiores son más específicas.

---

## Estructura de Carpetas

El proyecto se organiza en las siguientes carpetas, cada una con un propósito específico:
```
### 1. **Settings**
**Descripción:** Variables globales y configuraciones del proyecto.  
**Ejemplo:**  
```scss
// _variables.scss
$primary-color: #3498db;
$font-stack: 'Roboto', sans-serif;
```

### 2. **Tools**
**Descripción:** Mixins y funciones para reutilizar código.  
**Ejemplo:**  
```scss
// _mixins.scss
@mixin center {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

### 3. **Generic**
**Descripción:** Estilos genéricos, como resets y normalizaciones.  
**Ejemplo:**  
```scss
// _reset.scss
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

### 4. **Elements**
**Descripción:** Estilos para elementos básicos de HTML (h1, p, ul, etc.).  
**Ejemplo:**  
```scss
// _typography.scss
h1 {
  font-size: 2rem;
  font-weight: bold;
}
```

### 5. **Objects**
**Descripción:** Clases que definen estructuras o layouts reutilizables.  
**Ejemplo:**  
```scss
// _grid.scss
.o-grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
}
```

### 6. **Components**
**Descripción:** Estilos específicos para componentes de la interfaz, como botones o modales.  
**Ejemplo:**  
```scss
// _button.scss
.c-button {
  background-color: $primary-color;
  color: #fff;
  padding: 1rem;
  border: none;
  border-radius: 5px;
}
```

### 7. **Utilities**
**Descripción:** Clases de utilidad con estilos específicos, generalmente con `!important`.  
**Ejemplo:**  
```scss
// _utilities.scss
.u-hidden {
  display: none !important;
}
```

---

## Cómo Usar Esta Arquitectura

1. Crea una carpeta `scss` en tu proyecto y organiza los archivos en subcarpetas siguiendo esta estructura.
2. Incluye todos los archivos en un archivo principal, como `main.scss`:
   ```scss
   @import 'settings/variables';
   @import 'tools/mixins';
   @import 'generic/reset';
   @import 'elements/typography';
   @import 'objects/grid';
   @import 'components/button';
   @import 'utilities/utilities';
   ```
3. Compila el archivo `main.scss` a CSS utilizando un preprocesador como Sass.

---

## Beneficios de ITCSS

- **Escalabilidad:** Fácil de manejar en proyectos grandes.
- **Mantenibilidad:** Estructura clara y organizada.
- **Reducción de Especificidad:** Mejora la cascada y evita conflictos de estilos.

---

```
