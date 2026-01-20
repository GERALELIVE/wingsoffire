# 🔥 Wings of Fire - Sorteo Web App

Aplicación web de sorteos gratuita con animaciones épicas y efectos de sonido.

## 🌟 Características

- ✨ **Interfaz elegante** con diseño medieval/fantástico
- 🎰 **Animación de ruleta** tipo slot machine
- 🔊 **Efectos de sonido** con Web Audio API
- 🐉 **Alas de dragón animadas** que se mueven
- 🔥 **Transiciones con fuego** entre pantallas
- 📱 **100% Responsive** - funciona en móvil, tablet y desktop
- 🚀 **Sin dependencias** - archivo HTML único y autónomo
- 💯 **Completamente offline** - funciona sin internet

## 🎮 Cómo usar

1. Abre el archivo `index.html` en tu navegador
2. Escribe o pega la lista de participantes (uno por línea)
3. Haz clic en **START**
4. Haz clic en **SUMMON** para realizar el sorteo
5. Puedes hacer sorteos ilimitados con **SUMMON AGAIN**

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

### Opción 2: Netlify

**Ventajas:** Despliegue con arrastrar y soltar, dominio personalizado gratis, HTTPS automático

1. Ve a [Netlify.com](https://www.netlify.com)
2. Crea una cuenta gratis (puedes usar GitHub/Google)
3. Haz clic en **"Add new site"** → **"Deploy manually"**
4. Arrastra la carpeta `website` (con el `index.html` dentro)
5. ¡Listo! Tu sitio estará en línea en segundos
6. Netlify te dará una URL como `https://random-name-12345.netlify.app`
7. Puedes cambiar el nombre en **Site settings** → **Change site name**

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
└── index.html      # Aplicación completa (archivo único)
```

## 🎨 Personalización

Puedes personalizar fácilmente:

1. **Colores:** Busca en el CSS las variables de color:
   - `#d4af37` - Color dorado principal
   - `#ffd700` - Dorado brillante
   - `#3a1c52` - Morado oscuro del fondo

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

## 📝 Licencia

Este proyecto es de código abierto. Puedes usarlo libremente para proyectos personales o comerciales.

## 🤝 Soporte

Si tienes problemas:

1. **Audio no funciona:** Algunos navegadores requieren interacción del usuario antes de reproducir audio. Haz clic en cualquier parte de la página primero.

2. **No se ve bien en móvil:** Asegúrate de que la etiqueta viewport esté presente (ya incluida).

3. **No funciona offline:** El archivo HTML debe estar guardado localmente. Las fuentes de Google requieren conexión inicial pero se cachean después.

## 🚀 Próximos pasos

Una vez desplegado:

1. Comparte tu URL con amigos
2. Personaliza el diseño a tu gusto
3. Considera agregar tu propio dominio personalizado (gratis en GitHub Pages, Netlify o Vercel)

---

**¡Disfruta tu aplicación Wings of Fire sin pagar nada! 🔥🐉**
