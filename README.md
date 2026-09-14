# BahiaCash

App de gestión de caja para hotel (arqueo, propinas, equipo e historial).

Funciona en el móvil directamente desde el navegador, sin instalación. Optimizada para iPhone (Safari) y Android.

## Características

- **Arqueo de caja**: varios rangos de efectivo y datáfonos (Visa). Añade importes a mano o **escanea varios tickets con una sola foto** (OCR).
- **Propina**: reparto semanal (efectivo) y mensual (Visa) según días trabajados / bajas.
- **Equipo**: plantilla de empleados que se reutiliza en Propina (guardar/cargar .json).
- **Historial**: guarda arqueos y repartos en el dispositivo (localStorage).
- **Hojas limpias**: ver y compartir resumen por texto (o copiar).
- **PWA**: se puede añadir a la pantalla de inicio con icono propio.

## Publicar en GitHub Pages

1. Crea un repositorio en GitHub (público o privado).
2. Sube **todos** estos archivos a la **raíz** del repo (o a la carpeta `/docs`):
   - `index.html`
   - `manifest.json`
   - `apple-touch-icon.png`
   - `icon-192.png`
   - `icon-512.png`
   - `favicon-32.png`
   - `README.md` (opcional)
3. En GitHub: **Settings → Pages**.
4. En **Source** elige la rama (`main` o `master`) y la carpeta (`/ (root)` o `/docs`).
5. Guarda. En 1–2 minutos tendrás una URL del tipo:
   `https://TU-USUARIO.github.io/NOMBRE-REPO/`
6. Ábrela en el **iPhone con Safari** (debe ser `https://`). Así la cámara y el escaneo de tickets funcionan correctamente.

## Añadir a la pantalla de inicio (iPhone)

1. Abre la URL de GitHub Pages en Safari.
2. Toca **Compartir → Añadir a pantalla de inicio**.
3. Se instalará con el icono de BahiaCash y se abrirá a pantalla completa como una app.

## Escaneo de tickets (importante)

- El botón **Escanear** abre la **cámara en vivo**.
- Pasa cada ticket por la zona marcada de la pantalla: la app va **leyendo los importes sola** (sin hacer foto), como un lector.
- Los importes detectados aparecen abajo; puedes desmarcar los incorrectos y pulsar **Añadir**.
- Si el mismo ticket se queda quieto, no lo duplica (espera unos segundos entre lecturas del mismo importe).
- Si la cámara no está disponible, usa el modo foto como alternativa.
- La **primera vez** necesita internet para descargar el motor OCR (Tesseract). Después se reutiliza en la sesión.
- Consejos: buena luz, ticket nítido y bien encuadrado en la zona, no demasiado lejos.

## Actualizar la app

Cada vez que cambies algo, sustituye los archivos en el repo y haz commit + push. GitHub Pages se actualiza solo en unos minutos.

## Estructura del paquete

```
/
├── index.html          # App completa (HTML + CSS + JS)
├── manifest.json       # PWA / “Añadir a inicio”
├── apple-touch-icon.png
├── icon-192.png
├── icon-512.png
├── favicon-32.png
└── README.md
```

No hace falta servidor propio ni build: solo archivos estáticos en GitHub Pages.
