# 📸 INSTRUCCIONES PARA AGREGAR EL LOGO

## 🎯 Ubicación del Logo

Tu logo debe estar en la **misma carpeta** que estos archivos:

```
📁 tu-proyecto/
├── 📄 index.html
├── 📄 enterprise.html
├── 📄 white-label.html
├── 📄 vercel.json
├── 🖼️ logo-conecta2.png  ← ¡AQUÍ VA TU LOGO!
└── 📄 README.md
```

## ✅ Especificaciones del Logo

### Nombre del archivo:
```
logo-conecta2.png
```
⚠️ **IMPORTANTE**: El nombre debe ser EXACTAMENTE así (todo en minúsculas)

### Formato recomendado:
- **Tipo**: PNG con fondo transparente
- **Ancho**: 200-300px
- **Alto**: 60-80px
- **Resolución**: 72-150 DPI

### Ejemplos de tamaños:
- ✅ 300x80px (horizontal amplio)
- ✅ 250x70px (horizontal medio)
- ✅ 200x60px (horizontal compacto)
- ✅ 150x150px (cuadrado - si tu logo es cuadrado)

## 📍 Dónde Aparecerá el Logo

Tu logo se mostrará en:

1. **Landing Page (index.html)**:
   - Posición: Arriba, centrado
   - Tamaño: ~80px de alto
   - Con efecto de sombra verde

2. **Plan Enterprise (enterprise.html)**:
   - Posición: Arriba izquierda
   - Tamaño: ~60px de alto
   - Visible en pantalla y en PDF descargado

3. **Plan White Label (white-label.html)**:
   - Posición: Arriba izquierda
   - Tamaño: ~60px de alto
   - Visible en pantalla y en PDF descargado

## 🔄 Si Tu Logo Tiene Otro Nombre

Si tu logo se llama diferente (ej: `logo.png`, `conecta2-logo.png`), tienes 2 opciones:

### Opción 1: Renombrar el archivo (MÁS FÁCIL)
Simplemente renombra tu logo a: `logo-conecta2.png`

### Opción 2: Cambiar el código
Abre cada HTML y busca esta línea:
```html
<img src="logo-conecta2.png" alt="Conecta2.ai Logo">
```

Cámbiala por:
```html
<img src="tu-nombre-de-logo.png" alt="Conecta2.ai Logo">
```

Hazlo en los 3 archivos:
- `index.html` (línea ~138)
- `enterprise.html` (líneas ~158 y ~162)
- `white-label.html` (líneas ~177 y ~181)

## 🎨 Optimización del Logo

### Para mejor resultado:

1. **Fondo transparente**: Usa PNG, no JPG
2. **Sin bordes blancos**: Recorta el espacio extra
3. **Alta calidad**: No uses logos pixelados o borrosos
4. **Colores correctos**: Usa tu paleta oficial

### Herramientas recomendadas:

- **Quitar fondo**: https://remove.bg
- **Redimensionar**: https://imageresizer.com
- **Optimizar PNG**: https://tinypng.com

## ✅ Verificación

Después de agregar el logo, verifica:

1. **En navegador local**:
   - Abre `index.html` con doble click
   - ¿Se ve el logo? ✅

2. **En Vercel después del deploy**:
   - Abre tu URL: `https://tu-proyecto.vercel.app`
   - ¿Se ve el logo? ✅

3. **En PDF descargado**:
   - Click en "Descargar PDF"
   - Abre el PDF
   - ¿Se ve el logo en la primera página? ✅

## ⚠️ Problemas Comunes

### "El logo no se ve"

**Causa 1**: El archivo no está en la carpeta correcta
- ✅ **Solución**: Mueve `logo-conecta2.png` a la raíz del proyecto

**Causa 2**: El nombre no coincide
- ✅ **Solución**: Verifica que se llame EXACTAMENTE `logo-conecta2.png`

**Causa 3**: El formato es incorrecto
- ✅ **Solución**: Convierte a PNG si está en JPG, JPEG, SVG, etc.

### "El logo se ve muy grande o muy pequeño"

**Solución**: 
1. Redimensiona el logo a 200-300px de ancho
2. O edita el CSS en el HTML

En cada archivo HTML, busca:
```css
.logo-container img {
    max-height: 60px;  ← Cambia este número
}
```

Aumenta o disminuye el número según necesites.

### "El logo no sale en el PDF"

**Causa**: El navegador no puede cargar la imagen para el PDF

**Solución**:
1. Verifica que el logo esté en la carpeta correcta
2. Prueba con un logo más pequeño (<200KB)
3. Usa PNG en lugar de otros formatos

## 📱 Logo en Diferentes Dispositivos

El logo se adapta automáticamente:

- **Desktop**: Tamaño completo
- **Tablet**: Tamaño completo
- **Móvil**: Se ajusta al ancho disponible

## 🎯 Ejemplo de Estructura Final

Después de agregar todo:

```
📁 titanes-2025-conecta2/
│
├── 📄 index.html              (con logo)
├── 📄 enterprise.html         (con logo)
├── 📄 white-label.html        (con logo)
├── 📄 vercel.json
├── 📄 README.md
├── 📄 GUIA-DEPLOY-VSCODE.md
├── 📄 INSTRUCCIONES-LOGO.md   (este archivo)
└── 🖼️ logo-conecta2.png       ← ¡TU LOGO AQUÍ!
```

## 🚀 Después de Agregar el Logo

1. **Guarda todos los archivos**
2. **Abre VS Code**
3. **En la terminal, ejecuta**:
   ```bash
   vercel --prod
   ```
4. **Espera 30 segundos**
5. **¡Abre tu URL y verifica!**

## 💡 Tips Extra

1. **Logos oscuros**: Si tu logo es oscuro, agrega un resplandor claro
2. **Logos claros**: Si tu logo es claro, agrega un resplandor oscuro
3. **Test**: Siempre prueba en diferentes fondos

## 📞 ¿Necesitas Ayuda?

Si tienes problemas con el logo:
1. Revisa que el nombre sea correcto
2. Verifica que esté en la carpeta correcta
3. Prueba con un logo diferente para descartar problemas del archivo
4. Contacta al equipo técnico

---

**¡Listo! Con estas instrucciones tu logo quedará perfecto en todos los brochures! 🎨**
