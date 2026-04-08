[![English](https://img.shields.io/badge/English-Switch-blue)](README.md) [![简体中文](https://img.shields.io/badge/简体中文-切换-blue)](README_zh.md) [![日本語](https://img.shields.io/badge/日本語-切替-blue)](README_ja.md) [![한국어](https://img.shields.io/badge/한국어-전환-blue)](README_ko.md)

<div align="center">
  <img src="assets/logo.png" alt="HappyHorse Logo" width="200">

  # 🐴 HappyHorse Prompts

  **Colección comunitaria de prompts de generación de video para [HappyHorse](https://happyhorses.io)**

  [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
  [![GitHub stars](https://img.shields.io/github/stars/Ericgood/happyhorse-prompt?style=social)](https://github.com/Ericgood/happyhorse-prompt)
  [![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
  [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/Ericgood/happyhorse-prompt/pulls)

</div>

---

> **Nota:** Este es un proyecto impulsado por la comunidad. Si encuentras contenido que infrinja derechos de autor, por favor [abre un issue](https://github.com/Ericgood/happyhorse-prompt/issues).

## 🐴 ¿Qué es HappyHorse?

**HappyHorse-1.0** es un modelo Transformer unificado de 15 mil millones de parámetros que genera video y audio simultáneamente a partir de texto, sin necesidad de doblaje en postproducción. Apareció a principios de abril de 2026 como una entrada anónima en el ranking Video Arena de [Artificial Analysis](https://artificialanalysis.ai/), conquistando rápidamente el **puesto #1** y superando a modelos establecidos como Seedance 2.0, Kling 3.0 y PixVerse V6.

### Características Principales

- 🏆 **#1 en AI Video Arena** — Elo 1333 (Texto a Video), Elo 1392 (Imagen a Video)
- 🧠 **15B Parámetros** — Transformer de flujo único con 40 capas, sin atención cruzada
- 🎬 **Video + Audio Conjunto** — Diálogos, sonido ambiental y Foley generados junto con los fotogramas
- 🗣️ **Lip-Sync Multilingüe** — Chino, inglés, japonés, coreano, alemán, francés, cantonés
- ⚡ **8 Pasos de Denoising** — Inferencia rápida mediante destilación DMD-2, sin CFG
- 📖 **Código Abierto** — Modelo base, modelo destilado, módulo de super-resolución y código de inferencia (con derechos de uso comercial)

### Arquitectura

El modelo utiliza un **Transformer de auto-atención de flujo único** donde los tokens de texto, los latentes de imagen de referencia y los tokens de video/audio con ruido se denoisan conjuntamente en una secuencia. Las primeras y últimas 4 capas usan proyecciones específicas por modalidad; las 32 capas intermedias comparten parámetros entre todas las modalidades.

> *"Nadie en la comunidad de código abierto había realizado antes un pre-entrenamiento conjunto real de audio-video desde cero."*
>
> — [Informe de 36Kr sobre HappyHorse](https://eu.36kr.com/en/p/3757826958635781)

### Rankings del Leaderboard

| Categoría | Puntuación Elo | Posición |
|:---|:---:|:---:|
| Texto a Video (sin audio) | **1333** | 🥇 #1 |
| Imagen a Video (sin audio) | **1392** | 🥇 #1 |
| Texto a Video (con audio) | 1205 | 🥈 #2 |
| Imagen a Video (con audio) | 1161 | 🥈 #2 |

*Datos de [Artificial Analysis Video Arena](https://artificialanalysis.ai/), abril de 2026.*

### Comparativa

| Modelo | T2V Elo | Notas |
|:---|:---:|:---|
| **HappyHorse-1.0** | **1333** | Código abierto, audio-video conjunto |
| Seedance 2.0 (720p) | 1273 | ByteDance, líder en sincronización de audio |
| SkyReels V4 | 1244 | $7.20/min |
| Kling 3.0 1080p Pro | 1241 | $13.44/min |
| PixVerse V6 | 1239 | $5.40/min |

### El Misterio

Nadie ha confirmado públicamente quién construyó HappyHorse-1.0. Artificial Analysis lo describió como un **modelo "seudónimo"**. La investigación comunitaria sugiere que podría ser una optimización iterativa basada en el modelo de código abierto [daVinci-MagiHuman](https://github.com/BrightXiaoHan/MagiHuman), potencialmente vinculado a Sand.ai y el laboratorio GAIR de Shanghái. El nombre coincide con que 2026 es el **Año del Caballo** en el zodíaco chino.

> *Fuentes: [36Kr](https://eu.36kr.com/en/p/3757826958635781) · [WaveSpeed AI](https://wavespeed.ai/blog/posts/what-is-happyhorse-1-0-ai-video-model/) · [Análisis Apiyi](https://help.apiyi.com/en/happyhorse-model-mystery-ai-video-lmarena-analysis-en.html)*

---

## 📊 Estadísticas

| Total de Prompts | Destacados | Última Actualización |
|:---:|:---:|:---:|
| 18 | 7 | Abril 2026 |

---

## 🏆 Demos Oficiales — Generadas por HappyHorse

Estos prompts son demostraciones oficiales de las capacidades de HappyHorse: movimiento con percepción física, dinámica de fluidos, animación de personajes, consistencia temporal y generación de audio sincronizado.

---

### 1. 🎯 Niño con Hula Hoop

![Destacado](https://img.shields.io/badge/⭐_Destacado-Demo_Oficial-FF4D00)

> Movimiento con percepción física — el aro sube, baja y cae con peso y momento realistas.

#### 📝 Prompt

```
A hula hoop spinning on a kid's waist, gradually climbing to their chest, then dropping
to knees, then clattering to the floor. They pick it up to try again.
```

<div align="center">
  <a href="videos/hula-hoop-kid.mp4">
    <img src="assets/thumbnails/hula-hoop-kid.jpg" width="700" alt="Niño con Hula Hoop - Vista previa">
  </a>
  <br>
  <a href="videos/hula-hoop-kid.mp4">📥 Descargar Video</a> ・ <a href="https://x.com/i/status/2041591993386856448">🐦 Fuente</a>
</div>

---

### 2. ⛳ Putt de Golf

![Destacado](https://img.shields.io/badge/⭐_Destacado-Demo_Oficial-FF4D00)

> Emoción del personaje sincronizada con la física — el lenguaje corporal del golfista cambia con cada rotación de la pelota.

#### 📝 Prompt

```
A golf ball in a cup rolling around the rim three times before finally dropping in.
The golfer's body language matches each rotation. Audio: Ball rattle, exhale, plop.
```

<div align="center">
  <a href="videos/golf-ball-putt.mp4">
    <img src="assets/thumbnails/golf-ball-putt.jpg" width="700" alt="Putt de Golf - Vista previa">
  </a>
  <br>
  <a href="videos/golf-ball-putt.mp4">📥 Descargar Video</a> ・ <a href="https://x.com/i/status/2041591995106521352">🐦 Fuente</a>
</div>

---

### 3. 🐱 Gato y Reflejo en Tostadora

![Destacado](https://img.shields.io/badge/⭐_Destacado-Demo_Oficial-FF4D00)

> Renderizado de reflejos + animación animal — un gato toca la superficie cromada de una tostadora y el reflejo distorsionado responde.

#### 📝 Prompt

```
A cat staring at its own reflection in a toaster, paw tapping the chrome surface.
The distorted cat reflection taps back. Audio: Paw taps, confused meow.
```

<div align="center">
  <a href="videos/cat-toaster-reflection.mp4">
    <img src="assets/thumbnails/cat-toaster-reflection.jpg" width="700" alt="Gato y Tostadora - Vista previa">
  </a>
  <br>
  <a href="videos/cat-toaster-reflection.mp4">📥 Descargar Video</a> ・ <a href="https://x.com/i/status/2041591996754903188">🐦 Fuente</a>
</div>

---

### 4. ☕ Arte Latte del Barista

![Destacado](https://img.shields.io/badge/⭐_Destacado-Demo_Oficial-FF4D00)

> Obra maestra de dinámica de fluidos — la leche se sumerge bajo la crema, emerge y forma un patrón de roseta con movimientos precisos de muñeca.

#### 📝 Prompt

```
A barista creating latte art by pouring steamed milk into espresso. The white milk
submerges beneath the brown crema initially, then breaks through the surface as the
cup fills. The barista's wrist makes precise oscillating movements, creating a rosetta
pattern. The milk and espresso maintain their distinct colors while interacting at
the boundary. Audio: The gentle pour of liquid, the hiss of the steam wand in the
background.
```

<div align="center">
  <a href="videos/barista-latte-art.mp4">
    <img src="assets/thumbnails/barista-latte-art.jpg" width="700" alt="Arte Latte - Vista previa">
  </a>
  <br>
  <a href="videos/barista-latte-art.mp4">📥 Descargar Video</a> ・ <a href="https://x.com/i/status/2041591999061758171">🐦 Fuente</a>
</div>

---

### 5. 🌸 Timelapse de Flor Floreciendo y Marchitándose

![Destacado](https://img.shields.io/badge/⭐_Destacado-Demo_Oficial-FF4D00)

> Consistencia temporal a lo largo de dos semanas simuladas — mismo jarrón, misma ventana, mismo ángulo. La luz cambia naturalmente con el clima.

#### 📝 Prompt

```
A flower blooming and wilting over two weeks, one photo per day. Same vase, same window,
same angle. Light changes with weather. Audio: Quiet domestic.
```

<div align="center">
  <a href="videos/flower-bloom-timelapse.mp4">
    <img src="assets/thumbnails/flower-bloom-timelapse.jpg" width="700" alt="Timelapse de Flor - Vista previa">
  </a>
  <br>
  <a href="videos/flower-bloom-timelapse.mp4">📥 Descargar Video</a> ・ <a href="https://x.com/i/status/2039462980715524457">🐦 Fuente</a>
</div>

---

## 🤝 Cómo Contribuir

¡Damos la bienvenida a contribuciones de prompts!

### Enviar mediante Pull Request

1. Haz **Fork** de este repositorio
2. **Añade tu prompt** — crea un archivo Markdown en la carpeta `prompts/<categoría>/` correspondiente
3. **Envía un PR** — ¡lo revisaremos y fusionaremos!

### Enviar mediante Issue

¿No quieres hacer un PR? Solo [abre un issue](https://github.com/Ericgood/happyhorse-prompt/issues/new) con tu prompt y lo añadiremos por ti.

### Directrices

- ✅ Prompts originales o con permiso para compartir
- ✅ Indicar el modelo utilizado (ej: HappyHorse)
- ✅ Añadir descripción del resultado esperado
- ✅ Se recomienda encarecidamente incluir vista previa de video/imagen
- ❌ Sin contenido NSFW
- ❌ Sin reproducción de personajes con copyright

## 📜 Licencia

Este proyecto está licenciado bajo [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Puedes compartir y adaptar los prompts libremente, siempre que des el crédito apropiado.

## 🌐 Enlaces

- 🐴 [Sitio Web Oficial de HappyHorse](https://happyhorses.io)
- 📰 [36Kr: Análisis Profundo de HappyHorse](https://eu.36kr.com/en/p/3757826958635781)
- 📊 [Artificial Analysis Video Arena](https://artificialanalysis.ai/)
- 💬 [Discusiones](https://github.com/Ericgood/happyhorse-prompt/discussions)
- 🐛 [Reportar Problemas](https://github.com/Ericgood/happyhorse-prompt/issues)

---

<div align="center">

**Si te resulta útil, ¡danos una ⭐!**

Hecho con ❤️ por la Comunidad HappyHorse

</div>
