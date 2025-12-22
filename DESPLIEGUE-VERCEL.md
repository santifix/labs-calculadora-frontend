# 🚀 INSTRUCCIONES DE DESPLIEGUE EN VERCEL

## 📋 PASOS PARA DESPLEGAR

### 1️⃣ Preparar el repositorio de GitHub

```bash
# Asegúrate de que los cambios estén guardados
git add .
git commit -m "Actualizar URL del backend para producción"
git push origin main
```

### 2️⃣ Conectar con Vercel

1. Ve a [Vercel.com](https://vercel.com)
2. Clic en **"Add New Project"**
3. Importa tu repositorio de GitHub
4. Selecciona la carpeta `frontend` como **Root Directory**

### 3️⃣ Configuración del proyecto

**Framework Preset:** Other (es solo HTML estático)

**Build Command:** (déjalo vacío)

**Output Directory:** (déjalo vacío o `.`)

**Install Command:** (déjalo vacío)

### 4️⃣ Deploy

Haz clic en **"Deploy"** y espera a que termine.

---

## 🔧 CONFIGURACIÓN DE LA URL DEL BACKEND

El archivo `index.html` ya está configurado para usar:

```javascript
const URL_BASE_API = 'https://labs-backend-calculadora.onrender.com';
```

Si necesitas cambiarla en el futuro:

1. Edita el archivo `index.html`
2. Busca la línea con `URL_BASE_API`
3. Cámbiala por la nueva URL
4. Haz commit y push
5. Vercel se redesplegar automáticamente

---

## 🔄 ACTUALIZAR EL DESPLIEGUE

Cada vez que hagas cambios en tu código:

```bash
git add .
git commit -m "Descripción de los cambios"
git push origin main
```

Vercel detectará los cambios automáticamente y redesplegar.

---

## ✅ VERIFICACIÓN

Después de desplegar:

1. Abre tu URL de Vercel: https://labs-calculadora-frontend.vercel.app
2. Intenta registrar un usuario
3. Intenta iniciar sesión
4. Intenta hacer una suma

Si todo funciona, ¡listo! 🎉

---

## 🐛 PROBLEMAS COMUNES

### Error: "Network error" o no carga
**Solución:** 
- Verifica que el backend en Render esté corriendo
- Abre la consola del navegador (F12) para ver errores

### Error: "CORS blocked"
**Solución:** 
- Verifica que tu dominio de Vercel esté en la lista de orígenes permitidos en `servidor.js`
- Actualiza el backend con el nuevo dominio

### Error: Los cambios no se reflejan
**Solución:**
- Limpia el caché del navegador (Ctrl + Shift + R)
- Verifica que el commit llegó a GitHub
- Revisa los logs de despliegue en Vercel

---

## 🌐 URLS DEL PROYECTO

- **Frontend (Vercel):** https://labs-calculadora-frontend.vercel.app
- **Backend (Render):** https://labs-backend-calculadora.onrender.com

---

## 📚 RECURSOS

- [Documentación de Vercel](https://vercel.com/docs)
- [Deploy estático en Vercel](https://vercel.com/docs/concepts/deployments/overview)

