Aquí tienes el dossier maestro actualizado, Omar. Refleja el estado real de los cinco briefs AV cerrados, las versiones finales, y el siguiente paso (Deep Research de los briefs 3D). Todo en el mismo formato que ya tenías.

```markdown
# DOSSIER MAESTRO — GEM AUDIOVISUAL POOL BALANCE (V1.1)

**Fecha:** 17 de mayo de 2026
**Proyecto:** Pool Balance — Agencia de gestión hídrica, Veracruz, México
**Objetivo del dossier:** Memoria técnica central del ecosistema de investigación audiovisual y 3D para la Gema de Google AI Studio.

---

## 1. ARQUITECTURA DEL PROYECTO

La Gema Audiovisual de Pool Balance se alimenta de dos grandes bloques de investigación:

| Bloque | Propósito | Estado |
|--------|-----------|--------|
| **Serie AV (Audiovisual)** | Dotar a la Gema de conocimiento cinematográfico real (cámaras, ópticas, iluminación, sonido, postproducción) para generar contenido de redes y web con calidad de cine. | ✅ CERRADO |
| **Serie 3D (Web 3D)** | Dotar a la Gema de conocimiento sobre renderizado 3D web, animación, assets, WebXR y el puente físico cine→web. | ⏳ PENDIENTE LANZAR DEEP RESEARCH |

---

## 2. SERIE AV — INVESTIGACIONES CINEMATOGRÁFICAS (CERRADA)

### 2.1 Briefs y versiones finales

| Brief | Archivo en repositorio | Versión | Estado | Observaciones |
|-------|----------------------|--------|--------|---------------|
| **AV-1 Cámaras** | `AV-1-camaras-v1.3.md` | V1.3 | ✅ Cerrado | 15 observaciones corregidas (errores de rolling shutter, DR verificado con CineD, añadidas Alexa Mini LF, Nikon Z9/Z8, RED Komodo-X). Nota metodológica incluida. |
| **AV-2 Ópticas y Filtros** | `AV-2-opticas-y-filtros-v1.2.md` | V1.2 | ✅ Cerrado | 16 observaciones corregidas (fórmula f/D, pesos, coberturas de sensor, filtros, referencias). |
| **AV-3 Iluminación** | `AV-3-iluminacion-v1.3.md` | V1.3 | ✅ Cerrado | 31 observaciones corregidas (errores de equivalencias HMI/LED, añadidas Astera, Aputure 600c Pro, ratios Rembrandt/Paramount corregidos, tabla flicker-free ampliada con Godox). |
| **AV-4 Sonido** | `AV-4-sonido-v1.2.md` | V1.2 | ✅ Cerrado | 16 observaciones corregidas (añadidos fundamentos de acústica y psicoacústica, patrones polares completos, grabadoras, sistemas inalámbricos, diseño sonoro, Foley). |
| **AV-5 Postproducción** | `AV-5-postproduccion-v1.2.md` | V1.2 | ✅ Cerrado | 21 observaciones corregidas (flujo de trabajo completo, ACES, Dolby Vision, codecs de entrega, IMF, automatización con Python/Lua, QC, archivo LTO). |

### 2.2 Estadísticas de la serie AV
- **Total de briefs:** 5/5 cerrados.
- **Total de observaciones corregidas:** 109 (15+16+31+16+21+10 omitidas en V1.0 de AV-5).
- **Formato:** Markdown (.md) en repositorio GitHub `pool-balance-memory`.
- **Carga a la Gem:** Los 5 archivos .md están listos para ser cargados como Knowledge Base en Google AI Studio.

---

## 3. SERIE 3D — INVESTIGACIONES WEB 3D (PENDIENTE)

### 3.1 Briefs definidos (sin lanzar Deep Research)

| Brief | Tema | Alcance |
|-------|------|---------|
| **Brief 1** | Renderizado 3D (Three.js + R3F) | Cámaras, luces, materiales PBR, post-procesado |
| **Brief 2** | Animación (GSAP + Lenis) | ScrollTrigger, ScrollSmoother, Framer Motion |
| **Brief 3** | Assets 3D (glTF + IA) | Blender, Draco, KTX2, Meshy, Luma, Splatting |
| **Brief 4** | WebXR y AR | model-viewer, 8th Wall, Spline, Rive |
| **Brief 5** | Puente Cine ↔ Web | Física de cámara, fotometría, colorimetría |

### 3.2 Estado
- Los 5 briefs están redactados y almacenados en el repositorio.
- **Falta lanzarlos como Deep Research en Gemini** para generar los reportes técnicos que alimentarán a la Gema en su faceta 3D.
- El Brief 5 (Puente Cine↔Web) es el conector crítico entre la serie AV y la serie 3D.

---

## 4. SISTEMA DE LA GEMA (PROTOCOLOS DE OPERACIÓN)

### 4.1 Capas de extracción de calidad
1.  **System Prompt Maestro:** Árbol de decisión que obliga a la Gema a recopilar variables antes de responder (objetivo emocional, audiencia, restricciones, referencias).
2.  **Plantillas Parametrizadas:** 8-12 formularios reutilizables para pedir contenido audiovisual/3D.
3.  **"Muestra tu Trabajo":** Cada respuesta debe incluir recomendación + justificación + alternativas con tradeoffs.

### 4.2 Memoria persistente (NotebookLM Espejo)
Al final de cada sesión, la Gema genera una `NOTA_PERSISTENTE` con: fecha, tipo de decisión, configuración, justificación y etiquetas. Se copia manualmente a NotebookLM.

### 4.3 Traducción cine → web (cuando la serie 3D esté lista)
```
"Cuando te pida una escena 3D, traduce los parámetros cinematográficos a parámetros Three.js:
- Focal length real → FOV de PerspectiveCamera: 2 × atan(sensor_height / (2 × focal_length)) × (180/π)
- Tipo de luz cinematográfica → tipo de luz Three.js con intensidad en lúmenes
- T-stop → configuración de DepthOfField del postprocessing
Entrega código React Three Fiber listo para pegar."
```

---

## 5. REPOSITORIO Y ENLACES

### 5.1 Repositorio GitHub
- **URL:** `https://github.com/omarvalle0905-poolbalance/pool-balance-memory`
- **Archivos activos:**
  - `AV-1-camaras-v1.3.md`
  - `AV-2-opticas-y-filtros-v1.2.md`
  - `AV-3-iluminacion-v1.3.md`
  - `AV-4-sonido-v1.2.md`
  - `AV-5-postproduccion-v1.2.md`
  - `dossier-maestro-pool-balance.md` (este archivo)
  - `Investigación Técnica de Cámaras Cine Profesional.pdf` (archivo original unificado, legacy)
  - `Investigación de Postproducción.pdf` (archivo original, legacy)

### 5.2 Enlaces externos
- **Google AI Studio:** `https://aistudio.google.com`
- **NotebookLM:** `https://notebooklm.google.com`

---

## 6. HOJA DE RUTA

| Fase | Tarea | Estado |
|------|-------|--------|
| 1 | Cerrar los 5 briefs AV con auditoría completa | ✅ COMPLETADO |
| 2 | Cargar los 5 archivos .md como Knowledge Base de la Gema | ⏳ PENDIENTE |
| 3 | Redactar el System Prompt unificado con las 3 capas + protocolo de memoria | ⏳ PENDIENTE |
| 4 | Lanzar Deep Research de los 5 briefs 3D | ⏳ PENDIENTE |
| 5 | Cargar reportes 3D a la Gema y activar el puente cine↔web | ⏳ PENDIENTE |
| 6 | Primer despliegue de la Gema produciendo contenido real para Pool Balance | ⏳ PENDIENTE |

---

## 7. CONTROL DE VERSIONES DEL DOSSIER

| Versión | Fecha | Cambios |
|---------|-------|---------|
| V1.0 | 16 mayo 2026 | Creación inicial. AV-1 en borrador, AV-2 a AV-5 pendientes de auditoría. |
| V1.1 | 17 mayo 2026 | Actualización post-auditoría. Los 5 briefs AV cerrados. Versiones finales registradas. |
```

Listo, Omar. El dossier está actualizado. ¿Quieres que avancemos con el System Prompt unificado o prefieres lanzar los Deep Research de la serie 3D?
