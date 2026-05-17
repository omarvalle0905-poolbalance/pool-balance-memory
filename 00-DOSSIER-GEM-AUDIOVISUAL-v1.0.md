# Dossier de Salida — Gem Audiovisual Pool Balance
## Sala Claude Opus — Mayo 2026

> **Versión:** 1.0 (sala de origen, lista para migrar)
> **Fecha:** 2026-05-17
> **Mantenedor:** Omar Valle
> **Propósito:** Memoria persistente para retomar el proyecto Gem Audiovisual en sala nueva sin arrastrar contexto contaminado.

---

## 1. Qué es este proyecto (y qué NO es)

**Es:** Construir una Gem de Gemini que funcione como consultor técnico audiovisual de nivel profesional (DOP, sonidista, colorista) para generar contenido de marketing de Pool Balance con calidad cinematográfica real. La Gem debe razonar sobre física de la imagen y del sonido, no solo autocompletar.

**Salidas concretas que la Gem debe poder producir:**
- Prompts cinematográficamente correctos para Nano Banana Pro (generación de imagen).
- Especificaciones técnicas para sesiones de video reales (cámara, lente, luz, sonido).
- Prompts para herramientas de generación de video (Veo, Runway, Kling, Sora cuando aplique).
- Guiones técnicos para podcasts y piezas de audio.
- Recomendaciones de post-producción (color, mezcla, entrega).

**No es:**
- Una Gem genérica de marketing.
- Un agente de código 3D web (esa rama se pausó hoy, 2026-05-17).
- Un asistente conversacional sin base técnica documentada.

---

## 2. Decisión clave del 2026-05-17

Se pausa la integración de Three.js / R3F / capa 3D real en la PWA Pool Balance. Se resolverá el "wow visual" con CSS moderno, microinteracciones, parallax ligero y detalles en botones/carrusel sin motor 3D. Pendiente: Omar comparte el listado técnico de detalles CSS que sí se van a implementar (lo tiene en una nota).

**Consecuencia para este proyecto:** se retoma el plan original de cuatro investigaciones audiovisuales Deep Research. El Brief 5 (puente físico cine → Three.js) queda en pausa hasta que se reactive la rama 3D. Los briefs 3D-1 a 3D-4 que se habían diseñado quedan archivados, no descartados, para uso futuro.

---

## 3. Las cuatro investigaciones Deep Research del proyecto

| # | Tema | Estado |
|---|------|--------|
| AV-1 | Cámaras de cine y video profesional | Investigación V1.2 ejecutada, auditada, con errores conocidos pendientes |
| AV-2 | Ópticas: cine, foto-cine, anamórficos, filtros | Brief redactado y blindado, pendiente lanzar Deep Research |
| AV-3 | Iluminación profesional | Brief redactado y blindado, pendiente lanzar Deep Research |
| AV-4 | Sonido producción y postproducción | Brief redactado y blindado, pendiente lanzar Deep Research |
| AV-5 | Postproducción de imagen (NLEs, color, VFX, entregas) | Brief redactado y blindado, pendiente lanzar Deep Research |

> Nota: originalmente eran 4 investigaciones. Al desarrollarlas se separó "sonido" de "postproducción de imagen" porque son dominios distintos. Quedan 5 briefs audiovisuales pero el espíritu sigue siendo el plan de cuatro frentes (cámaras + ópticas + luz + post).

---

## 4. Estado del Brief AV-1 (Cámaras)

### Versiones
- **V1.0:** generada por Deep Research, contiene ~173 imágenes rotas donde deberían ir números. Inutilizable.
- **V1.1:** intento intermedio (HTML dashboard generado por Gemini "create page"). Visualmente impactante pero técnicamente superficial y con errores graves (consumos eléctricos absurdos como 800W o 1kW para cámaras, pesos inflados, V-Raptor confundido). Descartada.
- **V1.2:** corregida, números en línea como texto plano, errores críticos resueltos. **Archivo en repo:**
  `Investigación Técnica Audiovisual Profesional V1.2(1).md`
  Link raw confirmado funcionando en repo `pool-balance-memory`.

### Errores conocidos en V1.2 (a corregir en V1.3 antes de cargar a la Gem)

1. **Rango dinámico Alexa 35** reporta 15.1 stops SNR=2 y 16.3 stops SNR=1; CineD mide aproximadamente 13.1 stops SNR=2 y 15+ stops SNR=1. Verificar fuente y metodología.
2. **Rolling shutter Canon C400** reporta ~4.5 ms; CineD reporta ~14.7 ms en modo 6K full-frame. Posible confusión con modo recortado / Super 35.
3. **Archivo truncado** en mitad de sección Canon ("fungen como puentes entre fotografía de..." frase sin completar). Faltan secciones Blackmagic, Panasonic, Z-Cam, Sigma fp.
4. **ARRI Amira sensor:** dato en 16:9 (26.40 × 14.85 mm) correcto, pero falta dimensión Open Gate completa (28.17 × 18.13 mm).
5. **Verificar consistencia metodológica:** todas las cifras DR deben citar si son declaración de fabricante, CineD lab test, o estimación propia. Hoy hay mezcla sin etiquetar.

### Aciertos confirmados en V1.2
- Dimensiones sensor Alexa 35 correctas (27.99 × 19.22 mm).
- Rolling shutter Alexa 35 correcto (7.9 ms).
- Peso Alexa 35 corregido (2.9 kg cuerpo desnudo).
- Consumo Alexa 35 corregido (~85W).
- Distinción correcta V-Raptor [X] / XL [X] (global shutter, 0 ms) vs V-Raptor 8K VV original (rolling shutter).
- Sony Venice 2: 8.6K a 30p Open Gate, 4K a 120 fps, rolling shutter 3.0 ms, peso 4.3 kg, todo correcto.
- Sony Burano: detalle crítico capturado (procesamiento IBIS+ND eleva rolling shutter a ~10 ms).
- Canon C400: triple base ISO (800/3200/12800) correcto.

---

## 5. Briefs AV-2 a AV-5 (redactados, listos para lanzar)

### AV-2 — Ópticas

Cobertura requerida: lentes cine prime y zoom (ARRI Signature, Cooke S4/S7/S8, Zeiss Supreme, Leitz, Angénieux Optimo, Tokina Vista, Sigma Cine, Laowa, Atlas, DZOFilm, Sirui), foto-cine (Sony GM, Canon RF L, Nikon Z S-Line, Sigma Art DG DN), anamórficos con factor de squeeze (1.33×, 1.5×, 1.65×, 1.8×, 2×) y filtros (ND/IRND, polarizadores, Black Pro-Mist, Glimmerglass, difusión). Para cada lente: focal, T-stop, círculo de imagen mm, distancia mínima de foco, peso, montura, características ópticas (breathing, flare, bokeh, sharpness), precio. Diferencia T-stop vs f-stop, breathing, mumps, sensor cover, compatibilidad PL vs LPL.

Fuentes obligatorias: cookeoptics.com, zeiss.com, arri.com, angenieux.com, sharegrid.com, ymcinema.com, cined.com, bhphotovideo.com, lensprotogo.com.

Cierre del brief con instrucción anti-divergencia: "No amplíes a cámaras, iluminación, sonido ni post-producción."

### AV-3 — Iluminación

Cobertura requerida: fixtures LED modernos (ARRI SkyPanel X21/X23, Orbiter, L/M Series, Aputure LS 1200d Pro/600d/x/Nova/Electro Storm/Amaran, Litepanels Gemini, Astera Titan Tubes/Hyperion/PlutoFresnel, Quasar Rainbow 2, Kino Flo MIMIK 120, Creamsource Vortex 8/24, Nanlux Evoke 2400B, DMG Lumière Maxi/Mini MIX), HMI clásico (ARRI M-Series M18/M40/M90), tungsteno. Para cada fixture: potencia W, output en lux a 1m / 3m / 5m, CRI/TLCI/SSI, rango CCT, RGBWW o RGBACL, control DMX/sACN/Art-Net/CRMX, IP rating, peso, precio. Modificadores (softboxes, lanterns, china balls, banderas, sedas), gels (Lee/Rosco con códigos CTB/CTO/Plus Green/Minus Green), esquemas (3 puntos, Rembrandt, Split, motivada, negative fill, day-for-night).

Fuentes obligatorias: arri.com, aputure.com, astera-led.com, quasarscience.com, kinoflo.com, creamsource.com.au, nanlux.com, dmglumiere.com, le.rosco.com.

Cierre: "No amplíes a cámaras, ópticas, sonido ni post-producción."

### AV-4 — Sonido

Cobertura requerida: micrófonos boom (Sennheiser MKH 416/8060/50, Schoeps CMIT 5 U, DPA 4017/4018, Neumann KMR 81/82, Sanken CS-3e, Audio-Technica BP4071, Rode NTG5), lavalier y wireless (DPA 6060/6061, Sanken COS-11D, Countryman B6, Sennheiser MKE 2, Lectrosonics DCHT/DCR, Wisycom MTP60, Deity Theos, Rode Wireless Pro), recorders y mixers (Sound Devices MixPre/833/888/Scorpio, Zoom F8n Pro/F6, Tascam DR-701D, Aaton Cantar X3). Por cada uno: polar pattern, frequency response, sensitivity, self-noise, max SPL, alimentación, conectores, bandas RF, latencia, tracks, formatos, timecode, peso, autonomía. Conceptos: dBFS, LUFS de entrega por plataforma, sample rate, bit depth, timecode SMPTE, métodos de sincronía. Post: Pro Tools, DaVinci Resolve Fairlight, Logic Pro, Reaper, Nuendo; plugins (iZotope RX, FabFilter, Waves, Soundtoys, Sonnox); flujo ADR, foley, premix, mezcla final hasta Dolby Atmos.

Fuentes obligatorias: sennheiser.com, schoeps.de, dpamicrophones.com, sounddevices.com, zoom-na.com, lectrosonics.com, wisycom.com, izotope.com, avid.com, blackmagicdesign.com (Fairlight), dolby.com (Atmos).

Cierre: "No amplíes a cámaras, ópticas, iluminación ni post-producción de imagen."

### AV-5 — Postproducción de imagen

Cobertura requerida: NLEs comparados (DaVinci Resolve Studio, Premiere Pro, Final Cut Pro, Avid Media Composer) con criterios objetivos (colaboración, codecs, proxies, multicam, integración). DaVinci Resolve a fondo (nodos, ACES, color spaces, HDR, scopes, LUTs, calibración de monitor). VFX (Nuke, After Effects, Fusion, Blender, Houdini) y opciones tracking/roto/keying. Motion graphics esencial. Specs de entrega: DCP (JPEG 2000, XYZ, DCI), IMF, ProRes 4444 XQ y 422 HQ, requisitos Netflix, Amazon, Disney+, Apple TV+, HBO Max, BBC, YouTube, Vimeo (resolución, codec, bitrate, loudness LUFS, captions). QC tools.

Fuentes obligatorias: blackmagicdesign.com/products/davinciresolve, helpx.adobe.com/premiere-pro, support.apple.com/final-cut-pro, avid.com/media-composer, partnerhelp.netflixstudios.com, acescentral.com, mixinglight.com, fxguide.com, smpte.org.

Cierre: "No amplíes a cámaras, ópticas, iluminación ni sonido."

### Instrucción común para los cuatro briefs

Al final de cada uno, agregar literalmente:
> *"Formato de entrega obligatorio: Markdown puro. No uses LaTeX, no uses imágenes, no uses placeholders. Todos los valores numéricos (mm, ms, lux, K, USD, kg, W, dB) deben aparecer en línea como texto plano. Tablas comparativas en Markdown estándar. Citas numeradas con URL completa al final."*

Esto evita el problema de imágenes rotas que sufrió V1.0 de AV-1.

---

## 6. Sistema de la Gem — Cinco Capas Operativas

Diseñadas, pendientes de redacción final cuando los 5 reportes estén auditados y cargados.

| Capa | Función |
|------|---------|
| 1 | System prompt maestro como árbol de decisión: la Gem recopila variables (objetivo emocional, audiencia, plataforma, presupuesto, referencias, restricciones) antes de responder, y pregunta máximo dos cosas si falta info crítica. |
| 2 | Plantillas de prompt parametrizadas: 8-12 formularios reutilizables que Omar pega y rellena (briefing de plano, recomendación de cámara+lente+luz, prompt Nano Banana Pro, prompt Veo/Runway, brief de podcast, etc.). |
| 3 | Principio "muestra tu trabajo": cada recomendación técnica debe incluir opción principal + justificación citando KB + alternativa económica + alternativa premium + párrafo de tradeoffs. |
| 4 | Memoria persistente vía NotebookLM espejo: protocolo de cierre que genera bloque NOTA_PERSISTENTE al final de sesiones productivas, copiable manualmente al cuaderno vinculado. Template completo abajo. |
| 5 | Bucle de feedback explícito: al cierre, la Gem autoevalúa qué del KB usó, qué le faltó, qué supuesto hizo. Detecta huecos del KB y obliga a hacer supuestos explícitos. |

### Template NOTA_PERSISTENTE (para system prompt)
Al cierre de sesión productiva, o cuando el usuario diga "cierra sesión", "guarda esto", "archiva" o "memoriza", genera este bloque:

NOTA_PERSISTENTE
Fecha: AAAA-MM-DD
ID Proyecto/Cliente: [nombre]
Tipo de Decisión: Cámara | Lente | Iluminación | Sonido | Post | Workflow | Prompt
Contexto y Objetivo: máximo 3 líneas
Configuración Técnica Final: parámetros físicos completos
Justificación: cita al documento del KB con referencia
Resultado: Aceptado | Rechazado | Pendiente | Modificado
Alternativas Consideradas: económica + premium + tradeoffs
Etiquetas: #proyecto #tipo #tecnologia #año
Entrega listo para copiar manualmente al NotebookLM vinculado.

---

## 7. Plan de acción al abrir sala nueva

Pasos en orden:

1. La sala nueva lee este dossier completo y confirma versión leída.
2. Resume en 5 bullets el estado del proyecto.
3. Pregunta a Omar por qué frente quiere arrancar: corregir V1.2 de cámaras a V1.3, o lanzar el siguiente brief Deep Research (AV-2 ópticas es el orden natural).
4. Si Omar trae nuevo material (reportes Deep Research nuevos, correcciones), la sala lo audita igual que se hizo aquí con V1.2: errores numéricos, dependencias de firmware, consistencia metodológica entre fuentes (declaración fabricante vs lab medido).
5. Cuando los 5 reportes estén limpios y cargados a la Gem, se procede a redactar el system prompt maestro integrando las 5 capas operativas.

---

## 8. Glosario mínimo

- **DOP:** Director of Photography.
- **DR:** Dynamic Range (rango dinámico, stops).
- **SNR:** Signal-to-Noise Ratio. SNR=2 es métrica conservadora, SNR=1 es permisiva.
- **Rolling shutter:** lectura progresiva del sensor en ms; menor es mejor.
- **Global shutter:** lectura simultánea de todo el sensor (0 ms efectivo).
- **CRI/TLCI/SSI:** índices de calidad de color de fuentes de luz. Mayor es mejor.
- **CCT:** Correlated Color Temperature (Kelvin).
- **LUFS:** Loudness Units relative to Full Scale, unidad de medición de loudness.
- **dBFS:** decibelios relativos a fondo de escala digital.
- **ACES:** Academy Color Encoding System, estándar de gestión de color.
- **DCP/IMF:** formatos profesionales de entrega cine y streaming.
- **NLE:** Non-Linear Editor (editor de video).

---

## 9. Lo que NO está en este dossier (a propósito)

- Detalles del repo de código de la PWA Pool Balance (otra sala lo tiene, y la rama 3D se pausó).
- Detalles de Firebase, Vercel, despliegue de la app.
- Briefs 3D-1 a 3D-5 (archivados, no descartados, para reactivación futura).
- Conversaciones operativas día a día sobre marketing.

---

## 10. Changelog

- **2026-05-17 v1.0:** Dossier creado al cierre de la sala original Claude Opus, antes de migrar a sala limpia. Refleja decisión de pausar 3D y retomar foco audiovisual puro.

