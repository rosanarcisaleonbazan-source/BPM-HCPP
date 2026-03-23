# 🎨 Guía: Agregar Imágenes en el Menú + Cambiar Colores

Te muestro exactamente **cómo agregar imágenes profesionales** en las tarjetas de tu menú principal y personalizar los colores.

---

## 🌈 NUEVA PALETA DE COLORES (Incluida)

El archivo `index-NUEVOS-COLORES.html` ya tiene estos colores **únicos para Ecuador/alimentos:**

```css
--azul-marino:      #0f4c75   (Profesionalidad)
--naranja-tierra:   #d4651c   (Productos locales)
--verde-bosque:     #1b5e3f   (Agricultura)
--rojo-critico:     #c02929   (Urgencia en auditoría)
--gris-oscuro:      #2c3e50   (Texto principal)
```

**NO es una copia del proyecto verde** — Es un esquema completamente nuevo que representa mejor:
- 🌾 Agricultura ecuatoriana
- 🏭 Plantas de alimentos
- 🔒 Profesionalidad en auditoría

---

## 🖼️ OPCIÓN 1: Agregar Imágenes desde URL (Lo más fácil)

### Paso 1: Busca imágenes GRATIS en estos sitios

| Sitio | Búsqueda recomendada | Tipo |
|-------|----------------------|------|
| **Unsplash** | "food processing plant", "manufacturing", "quality control" | Fotos reales |
| **Pixabay** | "food production", "hygiene factory", "audit checklist" | Fotos + ilustraciones |
| **Pexels** | "industrial food", "plant inspection" | Fotos gratis |
| **Freepik** | "BPM", "HACCP", "food safety" | Ilustraciones |

### Paso 2: Copia la URL de la imagen

Ej: `https://images.unsplash.com/photo-xxx?w=500`

### Paso 3: Reemplaza en el código

En `index-NUEVOS-COLORES.html`, busca esta sección:

```html
<div class="card-image card-image-1">
  <svg viewBox="0 0 200 200" ...><!-- SVG aquí --></svg>
</div>
```

**Reemplázalo por:**

```html
<div class="card-image card-image-1" style="background: url('TU_URL_AQUI') center/cover no-repeat; background-blend-mode: overlay;">
</div>
```

**Ejemplo real:**

```html
<div class="card-image card-image-1" style="background: url('https://images.unsplash.com/photo-1576775076996-b0c7e8d8e3a5?w=500') center/cover no-repeat; background-blend-mode: overlay;">
</div>
```

---

## 🖼️ OPCIÓN 2: Subir Imágenes a tu Repositorio (Lo mejor)

### Paso 1: Crea una carpeta `images/` en tu proyecto

```
auditoria-bpm-haccp/
├── images/
│   ├── guia-infografica.jpg
│   ├── cuestionario-evalua.jpg
│   └── auditoria-checklist.jpg
├── index.html
├── vercel.json
└── ...
```

### Paso 2: Sube las imágenes a GitHub

Junto con tus otros archivos HTML.

### Paso 3: Usa las rutas en HTML

```html
<div class="card-image card-image-1" style="background: url('/images/guia-infografica.jpg') center/cover no-repeat;">
</div>
```

---

## 📸 IMÁGENES RECOMENDADAS ESPECÍFICAS

Aquí te digo **exactamente qué buscar** en cada sitio:

### **Tarjeta 1: Guía Visual (Infografía)**
- Busca: `"infographic clipboard audit" OR "flowchart diagram"`
- Colores: Azul, blanco, diagramas
- Ejemplo: Un clipboard con gráficos o un diagrama de flujo
- **URL Unsplash:** `https://images.unsplash.com/photo-1552664730-d307ca884978?w=500`

### **Tarjeta 2: Autoevaluación (Cuestionario)**
- Busca: `"quality checklist" OR "inspection clipboard" OR "quality control"`
- Colores: Verde, blanco, checkmarks
- Ejemplo: Un checklist con marcas verdes o una inspección
- **URL Unsplash:** `https://images.unsplash.com/photo-1611632736579-6b16e2b50449?w=500`

### **Tarjeta 3: Auditoría (Checklist)**
- Busca: `"food manufacturing" OR "food processing plant" OR "production line"`
- Colores: Naranja, industrial, profesional
- Ejemplo: Una planta de alimentos, línea de producción o inspección
- **URL Unsplash:** `https://images.unsplash.com/photo-1581092162562-40038e57c5d5?w=500`

---

## 🎨 CÓMO PERSONALIZAR LOS COLORES

### Método 1: Cambiar TODOS los colores

Abre `index-NUEVOS-COLORES.html` y busca la sección `:root`:

```css
:root {
  --azul-marino: #0f4c75;    /* ← Cambia este */
  --naranja-tierra: #d4651c; /* ← Cambia este */
  --verde-bosque: #1b5e3f;   /* ← Cambia este */
  --rojo-critico: #c02929;   /* ← Cambia este */
}
```

**Opciones de colores por tema:**

#### **Opción A: Rojo-Oro (Premium para alimentos)**
```css
--azul-marino: #8b0000;      /* Bordo oscuro */
--naranja-tierra: #d4af37;   /* Oro */
--verde-bosque: #2d5016;     /* Verde oscuro */
--rojo-critico: #c02929;     /* Rojo (igual) */
```

#### **Opción B: Azul-Verde (Fresco y natural)**
```css
--azul-marino: #1e5a8e;      /* Azul profundo */
--naranja-tierra: #27ae60;   /* Verde vibrante */
--verde-bosque: #0b7285;     /* Teal oscuro */
--rojo-critico: #c02929;     /* Rojo (igual) */
```

#### **Opción C: Gris-Naranja (Moderno y corporativo)**
```css
--azul-marino: #34495e;      /* Gris azulado */
--naranja-tierra: #e67e22;   /* Naranja vibrante */
--verde-bosque: #16a085;     /* Verde medio */
--rojo-critico: #e74c3c;     /* Rojo moderno */
```

### Método 2: Usa una herramienta visual

1. Ve a **https://coolors.co**
2. Genera una paleta que te guste
3. Copia los códigos HEX
4. Pégalos en `:root`

---

## 📝 CÓDIGO COMPLETO: Tarjeta con Imagen + Colores Personalizados

Aquí está **la estructura lista para copiar y pegar:**

```html
<!-- TARJETA 1: INFOGRAFÍA CON IMAGEN REAL -->
<a class="tool-card" href="infografia.html">
  <div class="card-image card-image-1" style="background: url('https://images.unsplash.com/photo-1552664730-d307ca884978?w=500') center/cover no-repeat; background-blend-mode: multiply;">
  </div>
  <div class="tc-body">
    <div class="tc-num">Herramienta 01</div>
    <h2>Guía Visual de BPM/HACCP</h2>
    <p style="color: var(--gris-medio); font-size: 13px; margin-bottom: 16px;">
      Infografía completa con principios, requisitos legales y flujos de auditoría.
    </p>
    <ul class="tc-features">
      <li>10 principios de BPM ilustrados</li>
      <li>7 pasos HACCP visuales</li>
      <li>Normativa ARCSA y Código de Salud</li>
      <li>Matriz de criterios por área</li>
      <li>Preguntas clave del auditor</li>
    </ul>
    <div class="tc-meta">
      <span class="tc-tag">📥 Descargable PDF</span>
      <span class="tc-tag">🎨 Visual</span>
      <span class="tc-tag">📚 Capacitación</span>
    </div>
    <div class="tc-cta tc-cta-1">
      <span>Abrir Guía</span>
      <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round"><path d="M5 12h14M12 5l7 7-7 7"/></svg>
    </div>
  </div>
</a>
```

---

## 🎯 PASO A PASO: Agregar TUS imágenes

### 1️⃣ Elige una imagen en Unsplash

Por ejemplo: `https://images.unsplash.com/photo-1581092162562-40038e57c5d5?w=500`

### 2️⃣ Busca esta línea en el HTML:

```html
<div class="card-image card-image-1">
  <svg viewBox="0 0 200 200" ...
```

### 3️⃣ Reemplaza por:

```html
<div class="card-image card-image-1" style="background: url('https://images.unsplash.com/photo-1581092162562-40038e57c5d5?w=500') center/cover no-repeat; background-blend-mode: multiply;">
</div>
```

### 4️⃣ Guarda y abre en navegador

¡Listo! La imagen aparecerá en la tarjeta.

---

## ⚙️ OPCIONES DE MEZCLA (background-blend-mode)

Si la imagen se ve muy oscura o muy brillante, prueba estas opciones:

```html
<!-- Oscurece la imagen (recomendado) -->
style="background-blend-mode: multiply;"

<!-- Aclara la imagen -->
style="background-blend-mode: screen;"

<!-- Contraste suave -->
style="background-blend-mode: overlay;"

<!-- Normal (sin efecto) -->
style="background: url('...') center/cover no-repeat;"
```

---

## 🚀 IMÁGENES ESPECÍFICAS QUE YO RECOMIENDO

### **Para Herramienta 1 (Infografía):**
Busca en Unsplash: `audit flowchart`
- https://images.unsplash.com/photo-1552664730-d307ca884978?w=500

### **Para Herramienta 2 (Cuestionario):**
Busca en Unsplash: `quality control checklist`
- https://images.unsplash.com/photo-1611632736579-6b16e2b50449?w=500

### **Para Herramienta 3 (Auditoría):**
Busca en Unsplash: `food processing plant`
- https://images.unsplash.com/photo-1581092162562-40038e57c5d5?w=500

---

## 📌 CHECKLIST FINAL

- [ ] Descargué `index-NUEVOS-COLORES.html`
- [ ] Cambié los colores (o me gustaron los que vienen)
- [ ] Busqué 3 imágenes en Unsplash
- [ ] Agregué las URLs en las tarjetas
- [ ] Probé en navegador (se ven bien)
- [ ] Subí a GitHub
- [ ] Deployé en Vercel
- [ ] ✅ ¡Sitio en vivo con mis colores e imágenes!

---

## 💡 BONUS: Hacer las imágenes más oscuras/claras

Si las imágenes se ven muy claras con el texto, añade una capa semitransparente:

```html
<div class="card-image card-image-1" 
     style="background: url('...') center/cover no-repeat, linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4));">
</div>
```

Cambia `0.4` por:
- `0.2` = más claro
- `0.5` = más oscuro
- `0.7` = muy oscuro

---

## 🆘 ¿Las imágenes se ven pixeladas?

Añade `?w=800` a la URL para mejor resolución:

```html
https://images.unsplash.com/photo-xxx?w=800
```

Cambios disponibles:
- `?w=400` = pequeño
- `?w=600` = medio
- `?w=800` = grande
- `?w=1200` = muy grande

---

## ✅ LISTO!

Ya tienes:
1. ✅ Nuevos colores (NO es copia)
2. ✅ Imágenes profesionales en tarjetas
3. ✅ Instrucciones paso a paso para personalizarlas

**Próximo paso:** Usa `index-NUEVOS-COLORES.html` como tu nuevo index principal y sube a GitHub. 🚀

---

**¿Necesitas ayuda con algo específico?** Pregunta. 😊
