# 🐝 Invitación Digital — Alison cumple 2 años

Invitación digital interactiva lista para desplegar en **GitHub Pages**.

## Estructura del proyecto

```
invitacion-alison/
├── index.html          ← Página principal (todo en uno)
├── assets/
│   ├── sobre.mp4       ← Video apertura del sobre
│   ├── animacion.mp4   ← Video animación invitación
│   └── sobre-poster.jpg← Frame estático inicial
└── README.md
```

## Flujo de la experiencia

1. **Pantalla estática** → Se muestra el primer frame del sobre con un botón pulsante "Toca para abrir".
2. **Video sobre** → Al hacer clic, se reproduce la animación de apertura del sobre.
3. **Video invitación** → Al terminar el sobre, transiciona con fade al video principal de Alison.
4. **UI superpuesta** → Contador regresivo + botón de ubicación aparecen sobre el video.

## Datos del evento

- **Festejada:** Alison
- **Fecha:** 5 de julio de 2025
- **Hora:** 3:00 PM
- **Lugar:** Fraccionamiento Los Encinos
- **Ubicación:** https://share.google/217zwY3bvhmzM4k7h

## Despliegue en GitHub Pages

### Paso 1 — Crear repositorio local

```bash
cd invitacion-alison
git init
git add .
git commit -m "🐝 Invitación digital Alison — inicial"
```

### Paso 2 — Subir a GitHub

```bash
# Crear repositorio en github.com (puede ser privado o público)
git remote add origin https://github.com/TU_USUARIO/invitacion-alison.git
git branch -M main
git push -u origin main
```

### Paso 3 — Activar GitHub Pages

1. Ir a **Settings → Pages** en el repositorio.
2. En **Source** seleccionar `Deploy from a branch`.
3. En **Branch** seleccionar `main` y carpeta `/ (root)`.
4. Guardar. En ~2 minutos estará disponible en:
   `https://TU_USUARIO.github.io/invitacion-alison/`

## Notas técnicas

- Todos los videos están en `assets/` con rutas relativas → funciona sin servidor.
- El contador regresivo apunta a `2025-07-05T15:00:00-06:00` (zona horaria CDT México).
- El botón de ubicación abre Google Maps en una nueva pestaña.
- Compatible con iOS Safari (usa `playsinline` y `webkit-playsinline`).
- No requiere dependencias externas (solo Google Fonts vía CDN).
