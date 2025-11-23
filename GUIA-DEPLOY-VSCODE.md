# 🚀 GUÍA PASO A PASO: Deploy desde Visual Studio Code a Vercel

## 📋 Requisitos Previos

1. **Visual Studio Code** instalado
2. **Node.js** instalado (descargar de https://nodejs.org)
3. **Git** instalado (descargar de https://git-scm.com)
4. **Cuenta en Vercel** (crear gratis en https://vercel.com)
5. **Tu logo** guardado como `logo-conecta2.png`

---

## 🎯 MÉTODO 1: Deploy Directo desde VS Code (MÁS RÁPIDO)

### Paso 1: Preparar tu proyecto

1. **Abre VS Code**

2. **Abre la carpeta del proyecto**:
   - File → Open Folder
   - Selecciona la carpeta donde están tus archivos HTML

3. **Agregar tu logo**:
   - Copia tu logo en la carpeta del proyecto
   - Renómbralo como: `logo-conecta2.png`
   - Debe estar en la misma carpeta que `index.html`

### Paso 2: Instalar Vercel CLI

1. **Abre la Terminal en VS Code**:
   - Menú: Terminal → New Terminal
   - O presiona: `` Ctrl + ` `` (tecla grave)

2. **Instala Vercel globalmente**:
   ```bash
   npm install -g vercel
   ```
   
   Espera a que termine la instalación (puede tomar 1-2 minutos)

### Paso 3: Login en Vercel

1. **En la terminal de VS Code, escribe**:
   ```bash
   vercel login
   ```

2. **Selecciona tu método de login**:
   - Te preguntará: "Login with..." 
   - Opción recomendada: **GitHub** (presiona Enter)
   - También puedes usar: Email, GitLab, Bitbucket

3. **Autoriza en el navegador**:
   - Se abrirá una ventana del navegador
   - Click en "Authorize" o "Allow"
   - Verás: "Success! You are now logged in"
   - Vuelve a VS Code

### Paso 4: Deploy a Vercel

1. **En la terminal, escribe**:
   ```bash
   vercel
   ```

2. **Responde las preguntas**:

   **¿Set up and deploy?** 
   - Presiona `Y` y Enter

   **¿Which scope do you want to deploy to?**
   - Selecciona tu cuenta (presiona Enter)

   **¿Link to existing project?**
   - Presiona `N` y Enter (es un proyecto nuevo)

   **¿What's your project's name?**
   - Escribe: `titanes-2025-conecta2` y Enter
   - O el nombre que prefieras (sin espacios)

   **¿In which directory is your code located?**
   - Presiona Enter (usa la carpeta actual `.`)

   **¿Want to modify these settings?**
   - Presiona `N` y Enter

3. **¡Deploy en proceso!**:
   - Verás una barra de progreso
   - Toma 10-30 segundos

4. **¡LISTO!** Verás algo como:
   ```
   ✅  Production: https://titanes-2025-conecta2.vercel.app
   ```

### Paso 5: Probar tu sitio

1. **Copia la URL** que te dio Vercel
2. **Ábrela en tu navegador**
3. **Verifica**:
   - ✅ Logo se ve correctamente
   - ✅ Colores Conecta2 están bien
   - ✅ Navegación funciona
   - ✅ Descarga PDF funciona

---

## 🎯 MÉTODO 2: Deploy desde GitHub (Recomendado para actualizaciones)

### Paso 1: Crear repositorio local

1. **Abre Terminal en VS Code**

2. **Inicializa Git**:
   ```bash
   git init
   ```

3. **Agrega tus archivos**:
   ```bash
   git add .
   ```

4. **Haz tu primer commit**:
   ```bash
   git commit -m "Initial commit - Titanes 2025 Conecta2.ai"
   ```

### Paso 2: Crear repositorio en GitHub

1. **Ve a GitHub.com** e inicia sesión

2. **Click en "+" → New repository**

3. **Completa la información**:
   - Repository name: `titanes-2025-conecta2`
   - Description: "Brochures interactivos Titanes 2025"
   - Public o Private: Tu elección
   - **NO** selecciones "Initialize with README"

4. **Click en "Create repository"**

5. **Copia los comandos** que GitHub te muestra

### Paso 3: Conectar tu proyecto local con GitHub

1. **En VS Code Terminal, pega y ejecuta**:
   ```bash
   git remote add origin https://github.com/TU-USUARIO/titanes-2025-conecta2.git
   git branch -M main
   git push -u origin main
   ```
   
   (Reemplaza `TU-USUARIO` con tu usuario de GitHub)

2. **Si te pide credenciales**:
   - Username: tu usuario de GitHub
   - Password: usa un **Personal Access Token** (no tu contraseña)
   - [Crear token aquí](https://github.com/settings/tokens)

### Paso 4: Conectar GitHub con Vercel

1. **Ve a [vercel.com/new](https://vercel.com/new)**

2. **Click en "Import Git Repository"**

3. **Selecciona tu repositorio**:
   - Busca: `titanes-2025-conecta2`
   - Click en "Import"

4. **Configuración del proyecto**:
   - Project Name: `titanes-2025-conecta2`
   - Framework Preset: **Other** (dejar como está)
   - Root Directory: `./` (dejar como está)
   - Click en **"Deploy"**

5. **¡Deploy automático!**:
   - Espera 30-60 segundos
   - Verás confetti cuando termine 🎉

6. **URL de tu sitio**:
   - Ejemplo: `https://titanes-2025-conecta2.vercel.app`

---

## 📝 ACTUALIZACIONES FUTURAS

### Si usaste Método 1 (CLI):

Simplemente corre en VS Code Terminal:
```bash
vercel --prod
```

### Si usaste Método 2 (GitHub):

1. **Haz tus cambios en VS Code**

2. **Guarda y commit**:
   ```bash
   git add .
   git commit -m "Actualización de precios" 
   git push
   ```

3. **Vercel detectará el push** y hará deploy automático en 30 seg

---

## 🎨 CÓMO AGREGAR TU LOGO

### Paso 1: Preparar el logo

1. **Formato recomendado**: PNG con fondo transparente
2. **Tamaño recomendado**: 
   - Ancho: 200-300px
   - Alto: 60-80px
   - O mantener proporción similar

3. **Renombrar**: `logo-conecta2.png`

### Paso 2: Colocar el logo

1. **Copia el archivo** `logo-conecta2.png`
2. **Pégalo en la carpeta** donde está `index.html`
3. **Verifica** que esté al mismo nivel que los HTML

### Paso 3: Verificar en el código

El código ya está preparado con estas líneas:

```html
<img src="logo-conecta2.png" alt="Conecta2.ai Logo">
```

Si tu logo tiene **otro nombre**, cámbialo en:
- `index.html` (línea ~138)
- `enterprise.html` (líneas ~158 y ~162)
- `white-label.html` (líneas ~177 y ~181)

### Paso 4: Deploy nuevamente

```bash
vercel --prod
```

O si usas GitHub:
```bash
git add .
git commit -m "Agregado logo Conecta2"
git push
```

---

## ⚠️ SOLUCIÓN DE PROBLEMAS COMUNES

### "command not found: vercel"

**Solución**:
```bash
npm install -g vercel
```

Si no funciona, cierra y abre VS Code de nuevo.

### "permission denied" al instalar

**Solución en Mac/Linux**:
```bash
sudo npm install -g vercel
```

**Solución en Windows**:
- Abre VS Code como Administrador
- Ejecuta el comando de instalación

### El logo no se ve en el PDF

**Causa**: El archivo `logo-conecta2.png` no está en la carpeta correcta

**Solución**:
1. Verifica que esté en la raíz del proyecto
2. Verifica el nombre exacto (distingue mayúsculas)
3. Vuelve a hacer deploy

### Los cambios no se ven en el sitio

**Solución**:
1. Limpia caché del navegador: Ctrl+F5
2. Prueba en modo incógnito
3. Espera 1-2 minutos y recarga

### Error "Git is not installed"

**Solución**:
1. Descarga Git: https://git-scm.com/downloads
2. Instálalo
3. Reinicia VS Code
4. Intenta de nuevo

---

## 📞 URLs FINALES

Después del deploy, tendrás:

```
Landing Page:
https://tu-proyecto.vercel.app/

Plan Enterprise:
https://tu-proyecto.vercel.app/enterprise

Plan White Label:
https://tu-proyecto.vercel.app/white-label
```

---

## 🎯 CHECKLIST FINAL

Antes de ir a Titanes, verifica:

- [ ] Logo se ve en las 3 páginas
- [ ] Logo se ve en el PDF descargado
- [ ] Tipografía Montserrat cargada correctamente
- [ ] Colores Conecta2 (#10e15c, etc.) se ven bien
- [ ] Navegación funciona entre páginas
- [ ] Botón "Descargar PDF" funciona
- [ ] WhatsApp links funcionan
- [ ] Responsive en tablet/iPad
- [ ] Precio $355/mes Enterprise correcto
- [ ] Precio $783/mes White Label correcto
- [ ] Email info@conecta2.ai correcto
- [ ] Teléfono +57 300 885 3322 correcto

---

## 💡 TIPS PRO

1. **Custom Domain**: En Vercel → Settings → Domains → Add Domain
   - Ejemplo: `titanes.conecta2.ai`

2. **Analytics**: En Vercel → Analytics (gratis)
   - Ve cuántas visitas tienes en tiempo real

3. **Compartir en Titanes**:
   - Crea un QR al URL principal
   - Imprime el QR en el stand
   - La gente escanea y ve los brochures en su móvil

4. **Backup**: 
   - Siempre ten los archivos en tu computadora
   - El deploy no borra tus archivos locales

---

## 🚀 ¡LISTO PARA TITANES 2025!

Ahora tienes tus brochures en línea con:
- ✅ Logo de Conecta2
- ✅ Tipografía Montserrat
- ✅ PDF con logo incluido
- ✅ URL profesional
- ✅ Deploy automático

**¿Algún problema?** Contáctame y te ayudo de inmediato.

**¡Éxito en Titanes! 🎉**
