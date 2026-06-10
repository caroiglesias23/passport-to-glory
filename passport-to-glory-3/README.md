# 🏕️ Passport to Glory – Summercamp 2026
## Guía de edición y publicación

---

## 📁 Archivos incluidos

| Archivo | ¿Qué es? |
|---------|----------|
| `index.html` | La app completa (HTML + CSS + JavaScript) |
| `manifest.json` | Configuración de app instalable (PWA) |
| `sw.js` | Service worker (permite usar offline) |
| `README.md` | Esta guía |

> **Nota:** Necesitas agregar íconos: `icon-192.png` y `icon-512.png`
> Pueden ser imágenes cuadradas del logo del campamento.

---

## ✏️ Cómo editar el estilo (colores, fuentes)

Abre `index.html` con cualquier editor de texto y busca la sección `:root {}`.
Está al inicio del archivo, dentro de `<style>`. Ahí están todas las variables de color:

```css
:root {
  --navy:  #0a1628;  /* fondo principal — cámbialo por cualquier color */
  --gold:  #F5C518;  /* color del título y acentos */
  --text:  #ffffff;  /* color de texto principal */
  /* ... etc */
}
```

**Para cambiar el título "Passport to Glory":**
Busca `.header-title` y edita `color: var(--gold)` por el color que quieras.

---

## 🔐 Cambiar la contraseña de admin

Busca en `index.html`:
```javascript
const ADMIN_PASSWORD = 'gloria2026';
```
Y cámbiala por tu propia contraseña.

---

## ⭐ Cambiar puntos de actividades

Busca en `index.html`:
```javascript
const ACT_POS = [
  {id:'manualidad', label:'Manualidad terminada a tiempo', pts:15, ...},
  ...
];
const ACT_NEG = [
  {id:'virtud_no', label:'Actuó contra la virtud...', pts:-20, ...},
  ...
];
```
Edita el valor de `pts` de cada actividad.

---

## 🚀 Publicar en Cloudflare Pages (GRATIS)

### Paso 1 — Crear cuenta
Ve a https://pages.cloudflare.com y crea una cuenta gratis.

### Paso 2 — Nuevo proyecto
- Click en **"Create a project"**
- Elige **"Direct Upload"** (no necesitas GitHub)

### Paso 3 — Subir archivos
- Arrastra la carpeta `passport-to-glory` completa
- O sube los 3 archivos: `index.html`, `manifest.json`, `sw.js`

### Paso 4 — Publicar
- Click en **"Deploy site"**
- Cloudflare te da un link tipo: `passport-to-glory.pages.dev`

### Paso 5 — Listo 🎉
Comparte el link con tus instructoras. Se puede instalar como app en el celular.

---

## 📲 Instalar como app en celular

**Android (Chrome):**
1. Abre el link en Chrome
2. Toca el menú (⋮) → "Agregar a pantalla de inicio"

**iPhone (Safari):**
1. Abre el link en Safari
2. Toca el botón compartir → "Agregar a pantalla de inicio"

---

## 💾 Datos y almacenamiento

Los puntos se guardan en el **localStorage** del navegador del dispositivo.
Esto significa:
- ✅ Funciona sin internet después de la primera carga
- ✅ Gratuito, sin base de datos externa
- ⚠️ Los datos son por dispositivo (si usas otro celular, empiezan en 0)

**Recomendación:** Usa siempre el mismo dispositivo para registrar puntos,
o usa el Panel Admin para hacer ajustes manuales si es necesario.

---

## 🌐 Dominio personalizado (opcional)

Si tienes un dominio propio, en Cloudflare Pages puedes configurarlo en:
**Settings → Custom domains**

---

¡Que disfruten el Summercamp! 🏆
