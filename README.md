# 🔥 Wings of Fire - Frontend

Aplicación web interactiva con sorteos y minijuegos de casino. Diseño medieval/fantástico con efectos visuales épicos.

## 🌐 Deployment

**URL de Producción:** https://dainty-haupia-0a725d.netlify.app  
**Plataforma:** Netlify  
**Backend API:** https://wingsoffirebackend.onrender.com

## 🎮 Componentes del Sistema

### 1. **Sorteo (index.html)** - Página Principal
- Sistema de ruleta tipo slot machine para sortear ganadores
- Gestión de alianzas/miembros con backend API
- Panel de administración protegido por contraseña (0p2026Win5)
- Alas de dragón animadas y transiciones con fuego
- Acceso directo a los 2 minijuegos (Slot y Blackjack)

### 2. **Alliance Slot (slot.html)** - Minijuego 100% Cliente
- Sistema de 5 niveles progresivos
- 3 símbolos: 🐉 Dragon (paga x5), 🐝 Bee (devuelve apuesta con 🦓), 🦓 Zoo (sin premio)
- Sistema de combos: 3 Dragons, 2 Dragons + 1 ROS, Dragon + ROS
- Auto-Roll desbloqueado tras 50 spins por nivel
- Probabilidades dinámicas por nivel (Dragon rate disminuye, ROS aumenta)
- Persistencia total en localStorage
- Sin conexión al backend

### 3. **Alliance Blackjack (blackjack.html)** - Minijuego con Backend
- Sistema de 4 niveles de progresión (0→499, 500→999, 1000→1499, 1500→2000)
- Reglas: Dealer stands on 17, Push = House wins, Blackjack pays 1.5x
- Sistema de puntos: Ganancia +50, Pérdida penaliza según nivel (-25/-50/-100/-200)
- Lógica de caída entre niveles con puntos protegidos
- 4-deck shoe con reshuffle al 25% de penetración
- Conectado a backend Flask para lógica segura del juego

## 🌟 Características Principales

- ✨ **Diseño unificado** medieval/fantástico en todas las páginas
- 🎰 **3 experiencias de juego** diferentes (sorteo + 2 minijuegos)
- 🔊 **Sistema de audio** con Web Audio API
- 📱 **100% Responsive** - optimizado para móvil, tablet y desktop
- 🔙 **Botón Atrás inteligente** - cierra modales antes de navegar
- 💾 **Persistencia local** con localStorage
- 🎨 **UI escalada al 90%** para mejor viewport fit
- 🔐 **Sistema de sesiones** con backend Flask

## 🎮 Flujo de Usuario

1. **Página de Inicio (index.html)**
   - Cargar lista de alianzas desde backend
   - Realizar sorteos con animación de ruleta
   - Acceder a panel admin para gestionar miembros
   - Navegar a minijuegos desde botones dedicados

2. **Minijuego Slot**
   - Progresar a través de 5 niveles
   - Desbloquear Auto-Roll tras 50 spins
   - Alcanzar 1000 créditos por nivel para avanzar
   - Riesgo de caer niveles al perder todos los créditos

3. **Minijuego Blackjack**
   - Conectar con backend para lógica del juego
   - Progresar hasta 2000 puntos en nivel 4
   - Penalizaciones crecientes por nivel
   - Sistema de victoria final al alcanzar 2000 pts

## 🌐 Despliegue Gratuito

Puedes alojar este sitio **100% gratis** en cualquiera de estas plataformas:

### Opción 1: GitHub Pages (Recomendado)

**Ventajas:** Gratis para siempre, fácil de actualizar, dominio personalizado gratis

1. Crea una cuenta en [GitHub](https://github.com) (si no tienes)
2. Crea un nuevo repositorio llamado `wingsoffire` (o el nombre que quieras)
3. Sube el archivo `index.html` al repositorio
4. Ve a **Settings** → **Pages**
5. En **Source** selecciona la rama `main` y carpeta `/ (root)`
6. Guarda y espera unos minutos
7. Tu sitio estará disponible en: `https://tu-usuario.github.io/wingsoffire`

**Instrucciones detalladas:**
```bash
# Desde la terminal/PowerShell en la carpeta website:
git init
git add index.html
git commit -m "Initial commit - Wings of Fire"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/wingsoffire.git
git push -u origin main
```

### Opción 2: Netlify (ACTUAL)

**Estado:** ✅ Desplegado en https://dainty-haupia-0a725d.netlify.app

**Para actualizar el deployment:**
1. Ve a [Netlify Dashboard](https://app.netlify.com/sites/dainty-haupia-0a725d)
2. Arrastra toda la carpeta `website/` en **Deploy → Drag & Drop**
3. Netlify desplegará automáticamente los cambios
4. Verifica que todos los archivos HTML funcionen correctamente
5. Prueba la conexión con el backend en blackjack

**Archivos a desplegar:**
- `index.html` (sorteo + admin)
- `slot.html` (minijuego slot)
- `blackjack.html` (minijuego blackjack)

### Opción 3: Vercel

**Ventajas:** Muy rápido, integraciones con Git, dominio personalizado gratis

1. Ve a [Vercel.com](https://vercel.com)
2. Crea una cuenta gratis
3. Haz clic en **"Add New Project"**
4. Si usas Git: conecta tu repositorio de GitHub
5. Si no: arrastra la carpeta `website`
6. Deploy automático
7. Tu sitio estará en `https://tu-proyecto.vercel.app`

### Opción 4: Cloudflare Pages

**Ventajas:** Red CDN global súper rápida, ilimitado, gratis

1. Ve a [Cloudflare Pages](https://pages.cloudflare.com)
2. Crea una cuenta gratis
3. Conecta tu repositorio de Git o sube directamente
4. Deploy automático
5. Tu sitio estará disponible en `https://tu-proyecto.pages.dev`

## 📂 Estructura del Proyecto

```
website/
├── index.html          # Sorteo principal + gestión de alianzas
├── slot.html           # Minijuego slot (100% cliente)
├── blackjack.html      # Minijuego blackjack (con backend)
├── slot-api.html       # [Deprecated] Versión antigua con backend
└── blackjack-old.html  # [Deprecated] Versión antigua
```

## 🔧 Configuración API

**API URL configurada en blackjack.html:**
```javascript
const API = 'https://wingsoffirebackend.onrender.com';
```

**API URL configurada en index.html:**
```javascript
const API_URL = 'https://wingsoffirebackend.onrender.com';
```

## 🎨 Personalización

### Colores Principales
- `#d4af37` - Color dorado principal (bordes, textos)
- `#ffd700` - Dorado brillante (títulos, highlights)
- `#3a1c52` - Morado oscuro del fondo
- `#1a0b2e` - Morado muy oscuro (gradientes)
- `#8a6e2f` - Dorado oscuro (bordes secundarios)

### Escalado de UI
Todas las páginas usan `transform: scale(0.9)` en el body para mejor ajuste en pantallas pequeñas.

### Modales
Los modales de información y contraseña se cierran con el botón "atrás" del navegador mediante `history.pushState()` y listeners de `popstate`.

2. **Textos:** 
   - Cambia `"WINGS OF FIRE"` por tu nombre
   - Modifica `"⚜ ROLL MEMBERS ⚜"` por tu título

3. **Emojis:** 
   - Busca el array `fantasyEmojis` en el JavaScript
   - Agrega o quita los emojis que quieras

## 🛠️ Tecnologías

- **HTML5** - Estructura
- **CSS3** - Estilos y animaciones
- **JavaScript** - Lógica y Web Audio API
- **Google Fonts** - Cinzel & Playfair Display

## 📱 Compatibilidad

✅ Chrome/Edge (Recomendado)  
✅ Firefox  
✅ Safari (iOS/macOS)  
✅ Opera  
✅ Navegadores móviles (Android/iOS)

## 🔒 Privacidad

- **Sin tracking:** No recopila datos de usuarios
- **Sin cookies:** No usa cookies
- **Sin analytics:** No envía información a terceros
- **100% local:** Todo funciona en el navegador del usuario

## � Desarrollo Local

### Ejecutar sin servidor
Los archivos HTML pueden abrirse directamente en el navegador para slot e index. Para blackjack necesitas el backend corriendo:

```bash
# En carpeta backend
cd ../backend
python app.py
```

Luego edita blackjack.html temporalmente para apuntar a localhost:
```javascript
const API = 'http://localhost:5000';
```

### Testing

**Slot (100% cliente):**
- Abrir `slot.html` directamente en navegador
- Todos los datos se guardan en localStorage

**Blackjack (requiere backend):**
1. Levantar backend local en puerto 5000
2. Cambiar API URL a localhost
3. Abrir `blackjack.html` en navegador

**Sorteo (requiere backend):**
1. Levantar backend local
2. Cambiar API_URL a localhost en index.html
3. Abrir `index.html` en navegador

## 📚 Documentación Adicional

- **DOCUMENTATION.md** - Documentación técnica completa (90+ secciones)
- **backend/README.md** - Documentación del backend API
- **DEPLOY_GUIDE.md** - Guía de deployment paso a paso

## 📝 Changelog Reciente

### v2.1.0 (Enero 2026)
- ✅ Botón atrás cierra modales en lugar de navegar
- ✅ UI escalada al 90% para mejor viewport fit
- ✅ Auto-Roll requiere 50 spins (antes 20)
- ✅ Nivel 2→1 cae a 475 pts (antes 25)
- ✅ Modal de info persiste en recarga
- ✅ Mensaje "PLAYING" sincronizado con animación

### v2.0.0 (Diciembre 2025)
- ✅ Sistema de 3 juegos completo
- ✅ Backend deployado en Render
- ✅ Frontend deployado en Netlify
- ✅ Documentación completa
- ✅ Sistema de niveles sin nombres (Level 1/2/3/4)

## 🤝 Soporte

### Problemas Comunes

1. **Audio no funciona:** 
   - Algunos navegadores requieren interacción antes de reproducir audio
   - Solución: Hacer clic en la página primero

2. **Blackjack no conecta:**
   - Verificar que backend esté activo (puede tardar 30s en despertar)
   - Revisar URL del API en blackjack.html

3. **Modal no se cierra con botón atrás:**
   - Limpiar cache del navegador
   - Verificar que estés en la última versión del código

4. **localStorage no persiste:**
   - No usar modo incógnito
   - Revisar configuración de cookies del navegador

## 🚀 Próximos Pasos Recomendados

1. ✅ **Ya desplegado** - Proyecto en producción
2. 🎨 Personalizar colores y textos según preferencias
3. 🎵 Agregar más efectos de sonido
4. 📊 Considerar agregar analytics (Google Analytics, Plausible)
5. 🗄️ Migrar de memoria a base de datos (si se requiere persistencia)

---

**Última actualización:** Enero 2026  
**Status:** ✅ Producción  
**Frontend:** https://dainty-haupia-0a725d.netlify.app  
**Backend:** https://wingsoffirebackend.onrender.com

**¡Disfruta Wings of Fire! 🔥🐉**
