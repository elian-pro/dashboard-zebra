# Dashboard Zebra - Guía de Implementación en EasyPanel (Hostinger)

## 📋 Archivos incluidos

1. **index.html** - Aplicación principal del dashboard
2. **logo-zebra.png** - Tu logo (deberás subirlo manualmente)
3. Este README con instrucciones

## 🚀 Pasos para implementar en EasyPanel

### 1. Acceder a EasyPanel
- Ingresa a tu panel de control de Hostinger
- Abre EasyPanel desde el menú

### 2. Crear nuevo proyecto
- En EasyPanel, ve a **"Apps"** o **"Projects"**
- Haz clic en **"Create New App"** o **"+ New"**
- Selecciona **"Static Site"** o **"HTML"**

### 3. Configuración del proyecto
- **Nombre del proyecto**: `dashboard-zebra` (o el que prefieras)
- **Tipo**: Static HTML Site
- **Puerto**: Usar el puerto por defecto (usualmente 80 o 3000)

### 4. Subir archivos

#### Opción A: Via File Manager
1. En EasyPanel, busca el **File Manager** o **Gestor de Archivos**
2. Navega a la carpeta raíz de tu proyecto (usualmente `public_html` o similar)
3. Sube el archivo `index.html`
4. Sube tu logo como `logo-zebra.png` en la misma carpeta

#### Opción B: Via FTP
1. Conecta via FTP usando las credenciales de Hostinger
2. Navega a la carpeta de tu dominio
3. Sube `index.html` y `logo-zebra.png`

#### Opción C: Via Git (Recomendado)
1. Crea un repositorio en GitHub/GitLab
2. Sube estos archivos al repositorio
3. En EasyPanel, conecta el repositorio
4. EasyPanel desplegará automáticamente

### 5. Configurar dominio (Opcional)
- En EasyPanel, ve a **"Domains"**
- Agrega tu dominio o subdominio
- Apunta el DNS al servidor de EasyPanel
- Espera a que la propagación DNS se complete (puede tardar hasta 24h)

### 6. Habilitar HTTPS (Recomendado)
- En EasyPanel, busca la opción **"SSL/TLS"**
- Habilita **"Let's Encrypt"** para SSL gratuito
- EasyPanel generará automáticamente el certificado

## 🔑 Credenciales de acceso

### Panel de Administración
- **URL**: Tu dominio + /index.html
- **Contraseña por defecto**: `admin123`

⚠️ **IMPORTANTE**: Cambia la contraseña después de la primera implementación

### Cómo cambiar la contraseña
1. Abre el archivo `index.html` en un editor de texto
2. Busca la línea (aproximadamente línea 180):
   ```javascript
   if (password === 'admin123') {
   ```
3. Cambia `'admin123'` por tu nueva contraseña
4. Guarda y vuelve a subir el archivo

## 📊 Características implementadas

✅ **Estatus de Plataformas**
- Filtros por fecha (desde/hasta)
- Visualización de fallas activas y resueltas
- Contador de usuarios afectados

✅ **Cambios Realizados**
- Filtros por fecha (desde/hasta)
- Filtro por cliente
- Visualización de prompts largos con scroll

✅ **Panel Administrativo**
- Agregar nuevas fallas
- Agregar cambios realizados
- Editar registros existentes
- Eliminar registros
- Protección con contraseña

✅ **Persistencia de Datos**
- Los datos se guardan en localStorage del navegador
- No requiere base de datos
- Los datos persisten entre sesiones

## 🎨 Personalización adicional

### Cambiar colores
En el archivo `index.html`, busca la sección `<style>` y modifica:
```css
.logo-container {
    background: linear-gradient(135deg, #1a1a1a 0%, #2d2d2d 100%);
}
```

### Agregar más campos
Edifica los objetos `statusForm` y `changeForm` en el código JavaScript.

## 🐛 Solución de problemas

### El logo no aparece
- Verifica que el archivo se llame exactamente `logo-zebra.png`
- Asegúrate de que esté en la misma carpeta que `index.html`
- Limpia el caché del navegador (Ctrl + F5)

### Los datos no se guardan
- Verifica que localStorage esté habilitado en el navegador
- Prueba en modo incógnito para descartar extensiones

### No puedo acceder al panel admin
- Verifica la contraseña (por defecto: admin123)
- Abre la consola del navegador (F12) para ver errores

## 📱 Compatibilidad

- ✅ Chrome/Edge (últimas versiones)
- ✅ Firefox (últimas versiones)
- ✅ Safari (últimas versiones)
- ✅ Móviles (responsive design)

## 🔄 Actualizar el dashboard

1. Modifica el archivo `index.html` localmente
2. Sube el archivo actualizado via FTP/File Manager/Git
3. Limpia el caché del navegador para ver los cambios

## 📞 Soporte

Si tienes problemas con:
- **EasyPanel/Hostinger**: Contacta el soporte de Hostinger
- **Funcionalidad del dashboard**: Revisa la consola del navegador (F12)

## 🔐 Mejoras de seguridad recomendadas

Para producción, considera:
1. Implementar autenticación backend real (no solo JavaScript)
2. Usar base de datos en lugar de localStorage
3. Agregar validación de entrada
4. Implementar límites de intentos de login
5. Usar variables de entorno para credenciales

## 📝 Notas adicionales

- El dashboard usa React (cargado via CDN)
- No requiere Node.js ni instalación de dependencias
- Funciona completamente en el cliente (frontend)
- Los datos se almacenan localmente en cada navegador

---

**Versión**: 1.0
**Última actualización**: Octubre 2025
