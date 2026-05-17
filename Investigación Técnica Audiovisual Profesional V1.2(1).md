# **Reporte Técnico Exhaustivo sobre Tecnologías de Cinematografía Digital: Cámaras, Ópticas e Iluminación**

La industria cinematográfica digital contemporánea opera en la intersección de la ciencia de la imagen, la óptica de precisión y la ingeniería fotométrica. Las decisiones técnicas adoptadas en el set dictan no solo la estética del proyecto, sino también la viabilidad de los flujos de trabajo en postproducción. Este documento presenta un análisis estructurado y exhaustivo de las plataformas de adquisición de imagen, sistemas ópticos e infraestructuras de iluminación que dominan la producción audiovisual profesional.

## **Análisis de Cámaras de Cine Digital y Video Profesional**

El ecosistema de adquisición de imágenes se define por la compleja interacción entre las dimensiones del fotodiodo en el sensor, la latitud de exposición cuantificable, la velocidad de lectura del sensor (rolling shutter) y la eficiencia del empaquetado de datos a través de códecs patentados. Es imperativo advertir que muchos de los rangos de grabación, resoluciones máximas y capacidades de conectividad detallados a continuación dependen de la versión del *firmware* instalada en la cámara; las actualizaciones periódicas de los fabricantes suelen desbloquear tasas de fotogramas superiores o compatibilidad con nuevos soportes de grabación.1

### **Ecosistema ARRI: Colorimetría y Retención de Rango Dinámico**

ARRI mantiene su hegemonía en la producción narrativa de alto nivel mediante una arquitectura de sensores enfocada en el rango dinámico, la reproducción del tono de piel y la suavidad en la caída de las altas luces (highlight rolloff).

La cámara **ARRI Alexa 35** introdujo el sensor Super 35 ALEV 4, con dimensiones exactas de 27.99 x 19.22 mm y un *pixel pitch* optimizado que permite una resolución máxima de 4.6K (4608 x 3164\) a 120 fps.2 Pruebas de laboratorio independientes demuestran que este sensor entrega un rango dinámico medido de 17 pasos teóricos, traduciéndose en 15.1 pasos con una relación señal-ruido (SNR) de 2, y 16.3 pasos con un SNR de 1.4 El fenómeno de *rolling shutter* está altamente mitigado, operando a 7.9 ms, eliminando virtualmente los artefactos de movimiento en paneos rápidos.6 A diferencia de arquitecturas *Dual Native ISO* explícitas, la Alexa 35 utiliza un sistema de *Enhanced Sensitivity* que optimiza el ruido hasta EI 6400, con una sensibilidad base nominal de 800 ISO.7 Los formatos de grabación internos incluyen MXF/ARRIRAW y Apple ProRes, con tasas de datos que alcanzan los 279 MB/s al grabar en 4.6K a 24p.2 El sistema adopta la curva gamma LogC4 y el espacio de color ARRI Wide Gamut 4, desplazando el gris medio al 28% para reasignar la latitud hacia las altas luces.1 El cuerpo desnudo pesa 2.9 kg, consume aproximadamente 85W mediante tarjetas Codex Compact Drives, y su precio base ronda los $75,000 USD.9

La **ARRI Alexa Mini LF** emplea el sensor A2X Large Format (36.70 x 25.54 mm), formado arquitectónicamente por dos sensores ALEV III empalmados.3 Ofrece una resolución máxima de 4.5K en modo Open Gate hasta 90 fps.3 El rango dinámico medido se sitúa en 14.5 pasos (SNR=2) y graba en el ecosistema tradicional LogC3.4 Su consumo ronda los 65W dependiendo del modo, con un peso de cuerpo desnudo de 2.6 kg.11 Con un precio aproximado de $58,000 USD, es la cámara estándar para la producción *Full Frame* narrativa actual.5

La **ARRI Alexa 65**, un sistema exclusivo de alquiler de ARRI Rental, utiliza el sensor A3X (54.12 x 25.58 mm) derivado de tres sensores ALEV III, logrando una resolución masiva de 6.5K en Open Gate.3 Por otro lado, la **ARRI Amira** comparte el sensor ALEV III Super 35 original (26.40 x 14.85 mm en modo 16:9), optimizada para flujos de trabajo documentales y *ENG* (Electronic News Gathering) con grabación directa en ProRes sobre tarjetas CFast 2.0, consumiendo \~50W y pesando 4.1 kg.11

### **RED Digital Cinema: Obturador Global y Compresión RAW Avanzada**

RED Digital Cinema ha revolucionado la adquisición de imágenes con sensores *VistaVision* (VV) y la adopción de la tecnología de obturador global (Global Shutter) en resoluciones extremas, eliminando las limitaciones del escaneo progresivo.

La **RED V-Raptor \[X\]** y su contraparte de estudio, la **V-Raptor XL \[X\]**, incorporan un sensor CMOS Full Frame VV (40.96 x 21.60 mm) con tecnología *Global Vision*.15 El *rolling shutter* es inexistente (0 ms), lo que permite implementaciones como *Phantom Track*, capturando flujos de video independientes para fondos de pantallas LED (virtual production) y cromas simultáneamente.16 Alcanzan resoluciones de 8K a 120 fps.15 El laboratorio de CineD reporta un rango dinámico de 13.7 pasos (SNR=2) y 15 pasos (SNR=1).4 Utilizan una arquitectura de ISO base de 800, codificando en REDCODE RAW (R3D) bajo niveles de compresión HQ, MQ y LQ, con tasas de transferencia de hasta 800 MB/s hacia medios CFexpress Type B.15 Procesan la señal a través del espacio REDWideGamutRGB y la curva Log3G10.9 El cuerpo estándar de la \[X\] pesa alrededor de 1.8 kg y consume 80W con un precio de $29,995 USD, mientras que la versión XL añade conexiones SDI adicionales, salidas de poder reguladas y filtros ND internos motorizados (de 2 a 7 pasos), apuntando a producciones de estudio a un costo aproximado de $39,995 USD, consumiendo 120W y pesando 3.6 kg.5

**Línea RED Original (Rolling Shutter):** Es imperativo distinguir la **RED Raptor 8K VV** original. Ésta comparte especificaciones de resolución y tamaño de sensor con la variante \[X\], pero utiliza un sensor *rolling shutter* convencional de alta velocidad (\<8 ms medidos), logrando un rango dinámico ligeramente superior de 13.7 pasos consolidados (SNR=2).4

La familia **Komodo** (27.03 x 14.26 mm, Super 35\) democratizó el obturador global, ofreciendo grabación 6K en tarjetas CFast 2.0 (Komodo) o CFexpress Type B (Komodo-X). La Komodo clásica presenta 12.5 pasos de latitud y 0 ms de rolling shutter, siendo el estándar industrial para *crash cams*, vehículos de seguimiento y cardanes debido a su perfil cúbico y bajo peso (0.95 kg y 1.18 kg para la X).4

### **Sony: Integración CineAlta y Línea FX**

Sony estructura su portafolio separando la cinematografía de alta gama (CineAlta) del segmento ágil de creadores y operadores individuales (Cinema Line), unificados por arquitecturas de sensor retroiluminado y capacidades híbridas.

La **Sony Venice 2** (variante 8K) alberga un sensor Full Frame (35.9 x 24.0 mm) que alcanza resoluciones de 8.6K hasta 30 fps en Open Gate, o 4K hasta 120 fps.21 Su métrica de *rolling shutter* es estelar, situándose en 3.0 ms, haciéndola sumamente capaz para secuencias de acción.24 Entrega 13.2 pasos de rango dinámico (SNR=2).4 Implementa un Dual Base ISO nativo de 800 y 3200.23 La Venice 2 elimina el grabador externo R7, codificando directamente en X-OCN (eXtended Original Camera Negative) a 16 bits en calidades XT, ST y LT sobre tarjetas AXS.25 El bitrate para X-OCN ST a 8K/24p ronda 1 GB/s.9 Su cuerpo desnudo pesa 4.3 kg, consume 76W y su precio ronda los $58,000 USD.5 Utiliza S-Log3 y S-Gamut3.Cine como espacios nativos.

La **Sony Burano** hereda el sensor 8.6K de la Venice 2, adaptándolo a un factor de forma ligero para operadores individuales. Su mayor innovación es la combinación de estabilización de imagen interna en el cuerpo (IBIS) con un filtro ND variable electrónico ultradelgado.21 No obstante, el procesamiento de estos sistemas incrementa significativamente el *rolling shutter*, el cual se eleva a \~10 ms en lectura 8K completa, afectando paneos rápidos en comparación con la Venice 2.24 Graba internamente en X-OCN LT y XAVC H a través de tarjetas CFexpress Type B. El cuerpo pesa 2.9 kg, consume 50W, con un precio aproximado de $25,000 USD.9

Dentro de la serie FX, la **FX9** (35.7 x 23.8 mm, Full Frame 6K) ofrece Dual Base ISO (800/4000) y filtros ND variables, entregando 11.5 pasos de rango dinámico (SNR=2) con grabación XAVC-I, pesando 2.0 kg y consumiendo 35W con un rolling shutter de \~22 ms.4 La **FX6** (0.89 kg, 8.7 ms de RS) y **FX3** (0.71 kg, 8.7 ms de RS) son célebres por su rendimiento en condiciones de baja luminosidad y enfoque automático predictivo.17 La **FX30** traslada este paradigma a un sensor APS-C / Super 35.4 En el ámbito de cámaras híbridas, la **A1 II**, **A7S III** (11.5 pasos de latitud) y **A7R V** continúan siendo plataformas de apoyo sustanciales para *gimbals*, grabando en XAVC S-I 4:2:2 10-bit.4

### **Canon: Sistema Cinema EOS y Expansión de la Montura RF**

La **Canon EOS C400** marca la consolidación de la montura RF en el cine profesional, alojando un sensor Full Frame retroiluminado (BSI) de 38.4 x 20.2 mm.30 Sustituye el concepto DGO por una arquitectura de *Triple Base ISO* (800, 3200 y 12,800), que optimiza la relación señal-ruido en escenarios de iluminación precaria.30 Captura video a 6K hasta 60 fps en Cinema RAW Light (12 bits) o XF-AVC hasta 120 fps en 4K en tarjetas CFexpress Type B.30 Su *rolling shutter* es de \~4.5 ms, pesa 1.54 kg (cuerpo) y consume 35W. Canon Log 2 se utiliza para priorizar el rango dinámico máximo, mientras que Canon Log 3 optimiza el flujo de trabajo con 14 pasos nominales.30

La **C500 Mark II** (38.1 x 20.1 mm, Full Frame 5.9K, rolling shutter de \~15 ms) y la **C300 Mark III** (26.2 x 13.8 mm, Super 35, rolling shutter de 15.6 ms y 1.75 kg) comparten un diseño modular.30 La C300 Mark III utiliza tecnología *Dual Gain Output* (DGO), combinando lecturas de alta y baja ganancia a nivel de pixel para lograr un rango dinámico excepcional de 12.8 pasos medidos (SNR=2) y 14.2 pasos (SNR=1).4 La **C70** (1.19 kg) empaqueta el mismo sensor DGO de la C300 Mark III en un diseño híbrido con montura RF, incorporando ND internos.32 Las **R5 C** (RS de 15.5 ms) y la reciente **R5 Mark II** fungen como puentes entre fotografía de alta resolución y grabación 8K Cinema RAW Light, integrando ventiladores activos para evadir límites térmicos de grabación.34

### **Blackmagic Design: Resolución Extrema en Arquitectura Abierta**

Blackmagic ha redefinido las barreras del costo frente al rendimiento computacional. La **URSA Cine 12K LF** implementa un sensor RGBW Large Format (35.64 x 23.32 mm) que omite el patrón Bayer tradicional, generando archivos de 12K a 80 fps en Open Gate y hasta 4K en 240 fps.37 Sorprendentemente, su velocidad de lectura del sensor (*rolling shutter*) cae a \~5.5 ms en resoluciones de 8K, compitiendo directamente con la Alexa Mini LF.39 El rango dinámico comprobado es de 13.6 pasos utilizando su tecnología Blackmagic RAW (BRAW) y la curva BMD Film Gen 5.41 Cuenta con ISO nativo dual, pesa alrededor de 3.9 kg (cuerpo desnudo), consume 85W y se comercializa por aproximadamente $14,995 USD.37

La **Pyxis 6K** introduce un factor de forma tipo caja (*box-style*) utilizando un sensor Full Frame 6K.43 Destaca por su ergonomía para drones y grúas, ofreciendo un rango dinámico robusto, aunque con un *rolling shutter* más prolongado (\~19 ms) en paneos críticos comparado con la URSA Cine.44 La **URSA Mini Pro 12K** clásica mantiene el formato Super 35 con la iteración original del sensor RGBW, mientras que las **Pocket Cinema Camera 6K Pro/G2** continúan dominando el mercado de cine independiente gracias a sus filtros ND motorizados y perfil Super 35.42

### **Panasonic, Z-Cam, DJI y Sigma**

**Panasonic:** Pioneros en tecnología dual, la **Varicam LT** (Super 35, Dual Native ISO 800/5000) cimentó el flujo de trabajo moderno de baja luz, seguido por la compacta **EVA1** (Super 35, 5.7K, 1.2 kg, 19W de consumo).46 En la actualidad, la **GH7** (Micro Cuatro Tercios) soporta grabación interna ProRes RAW a 5.7K, capturando imágenes a 60 fps con \~10 ms de rolling shutter y 11.5 pasos de rango dinámico (V-Log). Innova integrando grabación de audio a 32 bits en coma flotante y una licencia oficial para emular ARRI LogC3.48 La **S1H** y su versión box-style **BS1H** brindan capacidades Full Frame 6K, con la BS1H consumiendo apenas 15W optimizada para redes a través de PoE+.51

**Z-Cam:** Los modelos modulares **E2-F6** (Full Frame, rolling shutter de \~20 ms) y **E2-F8** capturan 6K y 8K respectivamente.53 La E2-F6 produce metraje ZRAW interno o ProRes RAW externo a 60 fps con un rango dinámico declarado de 15 pasos y opciones de montura EF o PL intercambiables por el usuario.54

**DJI Ronin 4D / 4D Flex:** Un ecosistema disruptivo que fusiona un cardán de estabilización de 4 ejes (eje Z vertical) con un sensor Full Frame (35.9 x 23.9 mm CMOS) intercambiable (X9-6K o X9-8K).56 Permite captura de Apple ProRes RAW y ProRes 4444 XQ. Incorpora 9 pasos de ND físicos internos y cuenta con Dual Native ISO (800/4000). El 4D Flex separa el bloque del sensor del cuerpo principal, reduciendo el peso de operación a una fracción.56 (RS estimado \~15 ms).

**Sigma:** La **fp** y la **fp L** (montura L, sensor Full Frame) ostentan el título de las cámaras de cine más compactas del mercado, generando archivos CinemaDNG RAW de 12 bits transmitidos directamente a discos SSD externos, sacrificando el obturador mecánico en favor de un diseño minimalista.53

### **Tablas Comparativas del Rendimiento de Sensores**

#### **Tabla 1: Cámaras de Cine de Alta Gama (High-End)**

| Fabricante / Modelo | Tamaño de Sensor (mm) | Res. Máxima | DR Medido SNR=2 (pasos) | Rolling Shutter (ms) | Dual Native ISO | Códecs Internos | Montura | Precio Aprox. USD |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **ARRI Alexa 35** | 27.99 x 19.22 | 4.6K @ 120fps | 15.1 | 7.9 ms | No (Enh. Sens) | ARRIRAW, ProRes | LPL / PL | $75,000 |
| **Sony Venice 2 8K** | 35.9 x 24.0 | 8.6K @ 30fps | 13.2 | 3.0 ms | 800 / 3200 | X-OCN, ProRes | PL / E | $58,000 |
| **RED V-Raptor \[X\]** | 40.96 x 21.60 | 8K @ 120fps | 13.7 | 0 ms (Global) | N/A (800 Base) | R3D, ProRes | RF | $29,995 |
| **ARRI Alexa Mini LF** | 36.70 x 25.54 | 4.5K @ 90fps | 14.5 | 7.4 ms | No (800 Base) | ARRIRAW, ProRes | LPL / PL | $58,000 |
| **BMD URSA Cine 12K** | 35.64 x 23.32 | 12K @ 80fps | 13.6 | \~5.5 ms (en 8K) | 400 / 3200 | BRAW | PL / EF | $14,995 |

#### **Tabla 2: Cámaras de Cine Medio y Arquitecturas Modulares**

| Fabricante / Modelo | Tamaño de Sensor | Res. Máxima | DR Medido SNR=2 | Rolling Shutter | Códecs Principales | Montura | Casos de Uso Típicos |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **Sony Burano** | Full Frame | 8.6K @ 30fps | 13.2 pasos | \~10 ms | X-OCN LT, XAVC H | PL / E | Operador único, Naturaleza |
| **Canon C400** | Full Frame | 6K @ 60fps | \~13 pasos | 4.5 ms | C. RAW Light, XF-AVC | RF | Emisión en vivo, Documental |
| **Canon C300 Mk III** | Super 35 | 4K @ 120fps | 12.8 pasos | 15.6 ms | C. RAW Light, XF-AVC | EF / PL | Producción televisiva, Indie |
| **RED Komodo-X** | Super 35 | 6K @ 80fps | 13.6 pasos | 0 ms (Global) | R3D, ProRes | RF | *Crash cams*, Gimbals, VFX |
| **DJI Ronin 4D 8K** | Full Frame | 8K @ 75fps | 11.5 pasos | \~15 ms | ProRes RAW, XQ | DL / E | Tomas en movimiento continuo |

#### **Tabla 3: Híbridas Full-Frame y Mirrorless Profesionales**

| Modelo | Sensor | Res. Máx | DR SNR=2 | Códecs | Montura | Peso | Precio USD |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **Sony FX3** | Full Frame | 4K @ 120fps | 11.5 pasos | XAVC S-I, ProRes RAW (Ext) | E | 0.71 kg | $3,899 |
| **Panasonic GH7** | Micro 4/3 | 5.7K @ 60fps | 11.5 pasos | ProRes RAW, H.265 | MFT | 0.8 kg | $2,199 |
| **Canon R5 C** | Full Frame | 8K @ 60fps | 11.5 pasos | C. RAW Light, XF-AVC | RF | 0.68 kg | $3,899 |
| **Sony A7S III** | Full Frame | 4K @ 120fps | 11.5 pasos | XAVC S-I | E | 0.61 kg | $3,499 |

### **Tendencias Operativas en Adquisición Cinematográfica**

El diseño de cámaras de la presente década obedece a cuatro vectores de desarrollo:

1. **El Estándar Open Gate:** La necesidad de entregar contenido simultáneamente en aspectos panorámicos cinematográficos (2.39:1) y verticales para consumo móvil (9:16) ha forzado a la industria a capturar la totalidad del área del sensor (formatos 3:2 o 6:5). Esto permite el reencuadre en postproducción sin comprometer la resolución base.37  
2. **Consolidación del Obturador Global:** Innovaciones arquitectónicas, como en la V-Raptor \[X\], han solucionado la histórica pérdida de rango dinámico asociada al circuito de *global shutter*. Su utilidad es innegable en los *LED volumes* (producción virtual), donde el escaneo progresivo causa patrones de muaré y desincronización con las tasas de refresco de las pantallas.15  
3. **Redes IP y Transmisión SMPTE ST 2110:** La URSA Cine 12K LF y la RED V-Raptor XL integran terminales Ethernet de cobre y fibra (10G/100G) para transmitir matrices de video en crudo a estaciones de control remoto o infraestructura de *broadcast* basada en IP, eludiendo la compresión SDI tradicional y alimentando plataformas directas a la nube (*Camera to Cloud*).19  
4. **Inteligencia Artificial en el Flujo de Adquisición:** Cámaras como la Sony A1 II y las plataformas híbridas Panasonic integran unidades de procesamiento neural que alimentan algoritmos de seguimiento ocular en tiempo real, erradicando el uso del enfoque manual en equipos reducidos.60

## **\---**

## **Ópticas: Lentes de Cine, Foto-Cine, Anamórficos y Filtros**

El carácter visual de un largometraje reside en la manipulación fenomenológica de los fotones antes de que impacten el sensor. La topografía de los lentes cinematográficos trasciende las métricas de nitidez absoluta; el análisis se centra en la aberración intencional, la caída del enfoque y el micro-contraste.

### **Conceptos Físicos de Lentes Profesionales**

Para evaluar la óptica de cine, es imperativo establecer la terminología técnica:

* **T-stop vs. f-stop:** El *f-stop* representa la relación geométrica matemática entre la longitud focal y el diámetro de la pupila de entrada. Por contraste, el *T-stop* (Transmission Stop) mide fotométricamente la cantidad absoluta de luz que penetra el lente tras sufrir atenuación por absorción y refracción en los elementos de cristal. Los lentes de cine se calibran en T-stops para garantizar que, al cambiar de una focal de 24mm a 85mm dentro de una misma familia, la exposición permanezca inalterada en el set, ahorrando costos masivos de postproducción.62  
* **Focus Breathing (Respiración):** La anomalía óptica donde la alteración del elemento de enfoque causa un cambio aparente en la longitud focal, magnificando o reduciendo el sujeto en el encuadre. La mitigación mecánica de esto es la principal diferencia de costos entre lentes fotográficos y de cine.65  
* **Focus Shift:** La pérdida de calibración del plano focal crítico conforme se cierra la apertura del iris (al incrementar la profundidad de campo). Lentes de alta gama estabilizan mecánicamente los grupos de lentes para prevenir esto.  
* **Mumps (Paperas Anamórficas):** Un artefacto originario de los primeros sistemas CinemaScope. Dado que la compresión horizontal variaba de manera no lineal dependiendo de la distancia del sujeto, los rostros en primeros planos no se comprimían suficientemente. Al des-comprimir en proyección, los rostros aparecían expandidos o inflados. El diseño óptico moderno traslada esta distorsión anómala a los elementos fuera de foco, garantizando geometría facial correcta mientras comprime el *bokeh* de fondo.66  
* **Compatibilidad PL y LPL:** La clásica montura PL ha sido el estándar. Sin embargo, para cubrir sensores grandes (*Large Format*), ARRI desarrolló la montura LPL (Large Positive Lock). Esta posee un diámetro mayor (62mm) y una distancia focal de brida más corta (44mm), lo cual permite que los rayos de luz impacten las esquinas del sensor perpendicularmente, eliminando el viñeteado y facilitando ópticas más ligeras.68

### **Esféricos Premium (Prime y Zoom)**

La neutralidad clínica ha sido reemplazada por "texturas orgánicas" programadas en las tolerancias de los vidrios.

**Ecosistema ARRI:**

* **Signature Prime y Zoom:** Diseñados nativamente para montura LPL y sensores grandes (círculo de imagen 46mm). Su rango comprende de 12mm a 280mm, operando uniformemente a un rápido T1.8.71 Las carcasas de magnesio reducen el peso (entre 1.7 kg y 2.8 kg). Su representación visual (*render*) está catalogada como atemporal: retiene micro-contrastes en la piel, transiciones cremosas a áreas desenfocadas (falloff), y produce *flares* cálidos. El precio por óptica oscila en $28,000 USD.71  
* **Master Anamorphic:** Lentes PL súper rápidos (T1.9) que buscan la perfección óptica: eliminan virtualmente la distorsión de barril típica de los anamórficos manteniendo el campo de visión elíptico.73

**Ecosistema Cooke Optics:**

* **S8/i, S7/i y S4/i:** Portadores del afamado "Cooke Look", caracterizado por una calidez inherente y un enfoque perimetral suave que realza texturas faciales humanas. La serie S8/i Full Frame empuja los límites operando a T1.4, pesando aproximadamente 2.5 kg por lente, y cubriendo sensores VV. La serie S7/i opera a T2.0.74 El precio ronda los $14,000 USD para el S8/i de 50mm.78  
* **Panchro/i Classic y Varotal:** La reinvención técnica de los diseños de la edad de oro de Hollywood. Los Panchro sacrifican correcciones modernas a favor de reflejos circulares (flare) pronunciados e imágenes con carácter antiguo, conservando engranajes 0.8 MOD modernos.75

**Ecosistema Zeiss:**

* **Supreme Prime y Supreme Prime Radiance:** Ópticas LPL/PL Full Frame (círculo 46mm). Operan a un clínico T1.5. Muy ligeros. La línea *Radiance* integra un revestimiento a medida, el *T* blue coating\*, el cual no es una simple sustracción, sino que permite *flares* de color azul altamente controlables e introduce un tono más cálido general sin sacrificar el desempeño de T1.5.79  
* **Master Prime (T1.3) y CP.3:** Los Master Primes son la cima histórica en S35 de alta apertura, mientras los CP.3 democratizan el acceso a vidrios de precisión para creadores de medio nivel.73

**Leitz / Leica:**

* **Thalia:** Primes para círculos de imagen de formato medio (60mm), con un carácter circular de enfoque y un renderizado melancólico.82  
* **Summilux-C y Summicron-C:** En el dominio de Super 35, los Summilux-C (T1.4) son legendarios por su homogeneidad milimétrica. Tienen una longitud fija (142mm), diámetro frontal de 95mm y supresión absoluta de la "respiración".83  
* **M 0.8 y Hugo:** El sistema M 0.8 traslada el cristal Leica M analógico (pesando apenas \~300g) con anillos de cine y montura Leica M. La serie Hugo, por su parte, aloja este cristal en una carcasa cinematográfica robusta con montura LPL.82

**Angénieux, Tokina y DZOFilm:**

* **Angénieux Optimo, EZ-1 y EZ-2:** Zooms paradigmáticos. La serie EZ es única porque su grupo óptico posterior es intercambiable por el operador; un EZ-1 (30-90mm T2.0 en S35) se convierte en un 45-135mm T3.0 para Full Frame, protegiendo la inversión económica en hardware.87  
* **Tokina Vista Prime:** Cubren VistaVision (46.7mm). Operan asombrosamente rápido a T1.5 pero son masivos. La versión "Vista-P" altera deliberadamente la corrección esférica para reducir el contraste y emular perfiles ópticos soviéticos.89  
* **DZOFilm Vespid y Pictor:** Lentes económicos que ofrecen un rendimiento excelente. Los Vespid (FF) operan a T2.1, pesan solo \~900g y cuestan entre $1,399 y $1,699 USD, una disrupción en la gama de entrada profesional.92

### **El Fenómeno Anamórfico**

La óptica anamórfica deforma la imagen en su eje horizontal para empacar una perspectiva panorámica en un sensor tradicional (4:3 o 3:2), que luego se "des-comprime" por software.

* **Squeeze Factors (Coeficiente de Compresión):**  
  * **2x:** El estándar clásico S35 para grabar en formato cuadrado 4:3, resultando en 2.66:1. Produce el máximo nivel de elongación ovalada en el bokeh y líneas de destello alargadas.94  
  * **1.5x y 1.6x:** La adaptación moderna para sensores Open Gate Full Frame (3:2 o 16:9), resultando en anchos de 2.25:1 a 2.40:1 sin recortar exceso de píxeles.97  
  * **1.33x:** Para sensores 16:9 tradicionales (televisión), entregando 2.39:1.99  
* **Atlas Orion y Mercury:** La serie Orion emplea 2x en S35 con frentes de 114mm. Son pesados (\~2.7 kg) pero ricos en aberración "vintage", costando $8,999 USD.95 La serie Mercury usa 1.5x en Full Frame, aliviando el peso a favor de cardanes.101  
* **Sirui (Nanomorph / Venus / Saturn) y Laowa (Proteus):** La serie Nanomorph de Sirui pesa una fracción (\<400g), logrando compresión 1.5x sobre sensores S35 y se ofrece con reflejos teñidos intencionalmente en ámbar, azul o plata, democratizando el anamórfico desde $999 USD.99 Sirui Venus y Saturn (1.6x) usan fibra de carbono para reducir masa en producciones sin espejo.93 Laowa compite fuertemente en el extremo profesional con la serie Proteus 2x Squeeze.

### **Lentes Fotográficos en Entornos Cinematográficos**

Familias de fotografía híbrida como **Sony G Master**, **Canon RF L**, **Nikon Z S-Line**, y **Sigma Art DG DN** ofrecen agudeza óptica superior y enfoque automatizado imperativo para operadores de *gimbal* comerciales.105 Sin embargo, introducen obstáculos formidables:

1. Sufren severamente de *focus breathing*, alterando la escala de la imagen.108  
2. Los sistemas de enfoque operan *fly-by-wire* (por cable electro-magnético). La rotación del anillo no es lineal; un giro de 90° rápido mueve el motor de enfoque de manera diferente que un giro de 90° lento. Esto impide que un 1st AC marque puntos de enfoque en disco o haga *rack focuses* precisos, haciéndolos subóptimos para sets de cine narrativo tradicionales.106

### **Filtros Profesionales Frente a la Lente**

Los directores de fotografía utilizan modificadores de vidrio en portafiltros (*matte boxes*, formatos 4x5.65" o 6.6x6.6"):

* **ND e IRND (Densidad Neutra / Infrarrojo):** Disminuyen los niveles de luz sin afectar el color para utilizar grandes aperturas bajo el sol. Densidades estándar van de 0.3 (1 paso) a 3.0 (10 pasos).109 Los filtros puros pueden sufrir de contaminación infrarroja (*IR pollution*) al recortar luz visible, por lo que **Tiffen, Schneider (Rhodium FSND), Formatt-Hitech (Firecrest) y NiSi** añaden recubrimientos dicroicos de bloqueo IR.112  
* **Difusión y Partículas:** El **Black Pro-Mist** de Tiffen incluye partículas oscuras que reducen el contraste clínico levantando las sombras localmente y generando un halo blando (halation) alrededor de los focos prácticos sin lavar toda la imagen. El **Glimmerglass** es menos intrusivo, empleado principalmente para mitigar el detalle de alta frecuencia que revela imperfecciones dérmicas en resoluciones 8K, manteniendo la base de contraste con microdestellos en luces puntuales. Usualmente, se instalan densidades de 1/8 o 1/4.113

## **\---**

## **Iluminación Cinematográfica**

La transición de los pesados bulbos de tungsteno (incandescentes) e hidrargiro medio (HMI) hacia matrices de LED ha consolidado un ecosistema iluminativo capaz de una reconfiguración de color instantánea (CCT) en el espectro completo y de integrarse nativamente a consolas de red.117

### **Innovaciones en Paneles LED y Motores RGBACL**

**Familia ARRI SkyPanel y Orbiter:** El legado del SkyPanel S60-C y S30-C (paneles rectangulares RGBW de 400W y 200W, respectivamente) se basaba en la homogeneidad de su luz difusa, entregando \~10,000 lux a 3m (S60-C).120 Hoy, esa hegemonía es desafiada por su sucesor, el **SkyPanel X** (modelos X21, X22, X23 modulares). El módulo X21 (800W, a 1m) sustituye los diodos RGBW por un complejo arreglo **RGBACL** (Red, Green, Blue, Amber, Cyan, Lime). Esta adición de cian y lima elimina los vacíos espectrales asociados al sistema LED previo, asegurando tonos de piel excepcionales (CRI \>95, TLCI 93\) entre 1,500K y 20,000K.117 Es capaz de emitir tanto luz suave nativa (mediante domos) como luz dura direccional. Al equipar su óptica *HyPer*, proyecta un asombroso haz focalizado de 16,602 lux a 3m (equivalente al disparo de un gran HMI a cielo abierto). Su chasis IP66 soporta lluvias intensas y lavados a alta presión.117 El **Orbiter** opera bajo la misma arquitectura de control en un chasis tipo "foco", alcanzando unos impresionantes 15,000 lux a 3m utilizando ópticas *Beam*.128

**Paneles de Alto Impacto (Creamsource, DMG, Litepanels):**

* **Creamsource Vortex8** y **Vortex24:** Sistemas robustos en carcasas mecanizadas IP65. El Vortex8 consume 650W emitiendo una base cruda (20° de ángulo) de 14,000 lux a un metro. El masivo Vortex24 opera a 1950W, despachando asombrosos 32,000 lux a 3.3 pies. Poseen atenuación absoluta, interfaces Ethernet y DMX, con valores de CRI/TLCI de 95, costando $5,500 y $16,500 USD.131  
* **DMG Lumière (Maxi / Mini MIX):** Paneles ultra delgados (1.25 pulgadas) para colocación en techos bajos y ascensores. El Maxi MIX (360W) entrega 7,500 lux a 1m con perfiles de color construidos junto a técnicos de Rosco, perfectos para igualar gelatinas físicas reales en la matriz LED.134  
* **Litepanels Gemini (1x1, 2x1, 5C):** Excelentes contendientes ligeros de panel blanco suave RGBWW enfocados en consumo por V-mount.

### **Luces Lineales e Iluminación Reactiva (Virtual Production)**

**Kino Flo MIMIK 120:** Representa un cisma tecnológico. Estos paneles de 120x60cm no se consideran meros "focos", sino *tiles* de imagen reactiva diseñadas expresamente para estudios de producción virtual o *LED Volumes*. Operan bajo el procesador de pantallas de video Megapixel VR HELIOS a 7680 Hz de *refresh rate* y procesamiento de color 10-bit, esquivando artefactos de *rolling shutter*. Reproducen el contenido de fondo (Unreal Engine) y traducen esa señal RGB a 5 emisores independientes de alto SSI, disparando la luz real a 10,000 Nits de intensidad lumínica sobre el actor. Esto previene la aberración cromática típica producida al iluminar tonos de piel con simples pantallas LED.118

**Tubos LED (Astera, Quasar Science):** Las luminarias tubulares proporcionan acentos perimetrales y reflejos oculares (*catchlights*) continuos. Los **Astera Titan Tube** (72W, 16 pixeles direccionales, batería para 20h) son omnipresentes por su supresión de cables y control de LumenRadio CRMX.137 Los **Quasar Science Rainbow 2** (R2) y **RR** empujan el formato integrando placas de montaje de cámara (*Ossium*) para empalmar docenas de tubos con efectos de píxel dinámicos, emitiendo espectros RGBX precisos.139

### **Luces de Punto (Point Source), HMI y Tungsteno Clásico**

Para sustituir la necesidad de enormes balastros magnéticos en exteriores diurnos, se han desarrollado emisores LED de punto único ultradensos.

**Nanlux Evoke y Dyno:** El **Evoke 2400B** es un monoluz *Bi-Color* que ha modificado el paradigma del rodaje nocturno. Consumiendo 2400W en corriente alterna, entrega la impactante cifra de 41,910 lux a 3m (a 5600K). Históricamente, crear un LED Bi-Color restaba un 50% de intensidad óptica por dispersión de chip; Nanlux solventó el problema densificando la matriz. Costando una fracción de lo que vale un HMI grande, y sin el riesgo de bulbos rotos o ultravioleta, cuenta con ventilación controlada, y clasificación IP55.142 La línea **Dyno 1200C** proporciona potencia equivalente a los paneles grandes de formato blando.146

**Aputure y Amaran:** El **Electro Storm CS15** (1500W RGB) e **XT26** (2600W bicolor) dominan la nueva gama industrial de Aputure. El CS15 rinde 32,000 lux a casi 3m y cuesta $6,000 USD.147 Las líneas anteriores **LS 1200d Pro** y **LS 600d/x Pro** continúan activas por su compatibilidad con placas de batería universales, monturas Bowens accesibles (Spotlight mounts, fresnels) y modulación de bajo presupuesto.148 La marca Amaran abastece la gama de entrada.

**Sistemas Clásicos HMI y Tungsteno:** Los sistemas HMI (Hydrargyrum Medium-arc Iodide) conservan ventajas en proyecciones masivas sobre grandes distancias (como bañar de luz todo un edificio). Las cabezas **ARRI M-Series** (M18, M40, M90) incorporan reflectores *MAX Technology* (sin lente de cristal grueso), lo que amplifica la focalización y aumenta la salida lumínica un 70% comparado a un PAR convencional.119 El **M18** consume 1800W, lo cual es crucial ya que es la capacidad máxima operable en una toma de pared residencial (20A) sin requerir un generador externo ruidoso.119 Las luminarias clásicas de **Tungsteno** (Fresnels de 650W, 1k, 2k, 5k) proporcionan el espectro continuo térmico absoluto (CRI 100), insuperable para tonos de piel reales, pero el ratio de vatios-por-lux es ineficiente y desprenden niveles de calor que afectan a los talentos.152

### **Fotometría Comparativa de Equipos Principales**

#### **Tabla 4: Unidades LED de Alta Potencia y Paneles RGB**

| Luminaria | Consumo (W) | Salida (lux) @ 3m | CCT (Kelvin) | Motor Color | CRI / TLCI | Modos DMX / IP | Protección | Precio USD |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **ARRI SkyPanel X21** | 800W | 16,602 Lux (@ 1m) | 1,500 \- 20,000 | RGBACL | 99 / 93 | DMX, sACN, ArtNet | IP66 | $6,000 |
| **Creamsource Vortex8** | 650W | 14,000 Lux (@ 1m) | 2,200 \- 15,000 | RRGBBW | 95 / 95 | CRMX, sACN | IP65 | $5,500 |
| **Nanlux Evoke 2400B** | 2400W | 41,910 Lux | 2,700 \- 6,500 | Bicolor | 96 / 97 | CRMX, ArtNet | IP55 | N/D |
| **Aputure Electro CS15** | 1500W | 32,000 Lux | 2,000 \- 10,000 | RGB | N/D | CRMX, ArtNet | IP65 | $6,000 |
| **Kino Flo MIMIK 120** | 120W | 2,000 Lux | N/A | 5-Emitters | Alto SSI | HELIOS Proc. | IP20 | N/D |

#### **Tabla 5: Tubos LED y Luminarias HMI Clásicas**

| Luminaria | Consumo | Tecnología | Lux a 3m | Alimentación | Formato Físico |
| :---- | :---- | :---- | :---- | :---- | :---- |
| **ARRI M18** | 1800W | Descarga HMI | 18,000 Lux | AC 110-240V | Cabeza Open Face |
| **Astera Titan Tube** | 72W | LED RGBMA | N/D | Batería / AC | Tubo 100 cm |
| **DMG Lumière Maxi** | 360W | LED Color | 10,000 Lux | V-Mount / AC | Panel Ultra Delgado |
| **ARRI 650 Plus** | 650W | Tungsteno | 5,000 Lux | AC 110-240V | Fresnel |

### **Modificadores, Difusión y Esquemas de Iluminación Aplicados**

El volumen y la cualidad direccional de una lámpara se moldean a través de herramientas de *Grip* e ingeniería de control para crear profundidad emocional en el sujeto.

**Modificadores e Infraestructura Óptica:** Para suavizar la dureza nativa de las luces (como los monoluces COB de Aputure o Nanlux), se adhieren modificadores. Los *Softboxes* (Chimera, DoPchoice Snapbag) encierran la cabeza y multiplican la superficie de emisión de la luz. Las configuraciones cenitales utilizan *Lanterns* o *Space Lights* para iluminar estudios de gran volumen (ambientales). El control de la fuga de luz (*spill*) es administrado por cortadoras, banderas sólidas (floppies) instaladas en atriles tipo *C-Stands*. En situaciones donde se emula la luz solar en un estudio, se emplea la tela *Silk* (seda) o mallas atadas sobre grandes marcos modulares de aluminio (*butterfly frames*) a las afueras de las ventanas.119

**Gelatinas de Color y Filtración Física:** Las correcciones térmicas o alteraciones dramáticas son calculadas numéricamente empleando catálogos internacionales Lee o Rosco. Para equilibrar una lámpara tungsteno (3200K) con la luz del día exterior (5600K), un técnico adhiere una lámina **Full CTB** (Color Temperature Blue, ej. Lee 201). De manera inversa, un **Full CTO** (Color Temperature Orange, Lee 204\) cálida fuentes diurnas de HMI para emular el atardecer o la luz de velas.155 Si una fuente práctica en un local introduce un velo magenta, se aplica un filtro **Plus Green** (Lee 244\) al LED, mientras un **Minus Green** resta verdes espurios comunes en la iluminación de tubos de oficinas institucionales.157 La difusión de la tela se categoriza en grados: Hampshire (muy sutil), Opal, Lee 251 (Quarter White), Lee 250 (Half White) y Lee 216 (Full White), siendo esta última la herramienta principal para suavizar y erradicar las sobras dentadas (*multiple shadows*) proyectadas por la nariz y mandíbula de los talentos.157

**Protocolos Teóricos y Esquemas de Iluminación:**

El dominio del Director de Fotografía (DoP) reside en la aplicación de la mezcla de fuentes (Tungsteno \+ HMI \+ LED calibrado) y las razones o "ratios" de intensidad.

* **El esquema de 3 puntos (Key, Fill, Back):** Establece una luz "Clave" (*Key*) angular que modela la forma del rostro. El "Relleno" (*Fill*) modera el contraste de las sombras producidas (por ejemplo un ratio de 4:1 implica sombras densas y dramáticas). La luz de "Contra" o "Separación" (*Back/Rim light*) desdibuja los contornos del sujeto frente a un fondo neutro, inyectando tridimensionalidad bidimensional.  
* **Iluminación Rembrandt y Split:** El esquema Rembrandt sitúa la Key Light a 45° de altitud y rotación, proyectando un triángulo especular en el lado sombrío de la cara del actor. La luz de *Split* divide el rostro exactamente por la mitad geométrica del tabique nasal, empleada en suspenso o introspección severa.  
* **Iluminación Motivada y Prácticos:** En decorados narrativos, la luz se justifica desde fuentes perceptibles dentro del marco (lámparas de escritorio, pantallas de TV, ventanas). Se usan "Prácticos" reforzados con fuentes LED controladas por la consola para iluminar adecuadamente a los actores mientras mantienen la ilusión del origen focal.  
* **Exteriores Día con Relleno Negativo (Negative Fill):** La luz solar rebota incontrolablemente sobre aceras, paredes y el mismo entorno de los actores, aplanando los volúmenes del rostro. Los técnicos colocan telas de terciopelo o paneles sólidos negros al costado del rostro ausente de luz solar directa. Estos absorben las fugas fotónicas (rebotes perimetrales), restituyendo el contraste visual cinemático en escenas rodadas a mediodía.  
* **Día-por-Noche (Day for Night) e Interior Noche:** Requieren exponer la imagen subtirando sombras y usando esquemas de temperatura fría predominante, o bloqueando completamente ventanas diurnas reales, usando rebotes duros de HMI azulados a través de las cortinas, simulando el ángulo agudo de la luna.

Con la evolución de plataformas de red unificadas (DMX bajo interfaces sACN y Art-Net sobre LumenRadio CRMX), un operador en un iPad puede reasignar un *gel emulation* de Lee 204 y disminuir gradualmente la intensidad de 10 SkyPanels sincronizados, permitiendo crear en milisegundos una caída del sol hiperrealista, erradicando los extenuantes requerimientos físicos que lastraban a los equipos de eléctricos en las décadas precedentes.133

#### **Fuentes citadas**

1. ARRI LogC4, acceso: mayo 16, 2026, https://www.arri.com/resource/blob/278790/dc29f7399c1dc9553d329e27f1409a89/2022-05-arri-logc4-specification-data.pdf  
2. Arri Alexa 35 Camera \- Panavision, acceso: mayo 16, 2026, https://www.panavision.com/camera-and-optics/cameras/product-detail/alex35-alexa-35  
3. Arri Alexa \- Wikipedia, acceso: mayo 16, 2026, https://en.wikipedia.org/wiki/Arri\_Alexa  
4. CineD's Dynamic Range Ranking | May 2024 : r/videography \- Reddit, acceso: mayo 16, 2026, https://www.reddit.com/r/videography/comments/1cyccwo/cineds\_dynamic\_range\_ranking\_may\_2024/  
5. Top cinema camera comparison. What do you guys think? : r/cinematography \- Reddit, acceso: mayo 16, 2026, https://www.reddit.com/r/cinematography/comments/15g2un0/top\_cinema\_camera\_comparison\_what\_do\_you\_guys/  
6. ARRI ALEXA 35 Lab Test Talk & Real-Life Footage \- YouTube, acceso: mayo 16, 2026, https://www.youtube.com/watch?v=MZlzfPaXq9I  
7. ALEXA 35 | Camera Systems | ARRI, acceso: mayo 16, 2026, https://www.arri.com/en/camera-systems/cameras/legacy-camera-systems/alexa-35  
8. THE GO-TO CAMERA FOR DRAMA SERIES, FEATURE FILMS AND COMMERCIALS \- ARRI, acceso: mayo 16, 2026, https://www.arri.com/resource/blob/261224/0654da7b1dda042b23b1b6c254c1f8c3/alexa-%20mini-lf-flyer-technical-data-sheet-data.pdf  
9. 10 Best Cinema Cameras to Buy (updated 2025\) | Topsheet Entertainment Payroll, acceso: mayo 16, 2026, https://topsheet.io/blog/best-cinema-cameras  
10. ARRI ALEXA 35: A New Standard for Digital Cinema | Tech News \- AbelCine, acceso: mayo 16, 2026, https://www.abelcine.com/articles/blog-and-knowledge/tech-news/arri-alexa-35-a-new-standard-for-digital-cinema  
11. ARRI Alexa 35 \- PhotoCineRent, acceso: mayo 16, 2026, https://photocinerent.com/en/cameras/arri/arri-alexa-35  
12. ARRI Formats and Resolutions Overview (AFRO), acceso: mayo 16, 2026, https://www.arri.com/resource/blob/390890/0ecfdcb70ea22c5fc489f0fb7267aa30/2025-11-arri-formatsandresolutionsoverview-v6-1-data.pdf  
13. ARRI ALEXA 65 \- VFX Camera Database, acceso: mayo 16, 2026, https://vfxcamdb.com/arri-alexa-65/  
14. AMIRA | Camera Systems \- ARRI, acceso: mayo 16, 2026, https://www.arri.com/en/camera-systems/cameras/amira  
15. RED V-Raptor-X Specifications \- Thom Hogan, acceso: mayo 16, 2026, https://www.zsystemuser.com/z-mount-cameras/z-camera-database/red-v-raptor-x-specificatio.html  
16. V-RAPTOR | RED Digital Cinema, acceso: mayo 16, 2026, https://www.red.com/v-raptor  
17. You Won't Believe These 2024 Camera Tests Results\! \- YouTube, acceso: mayo 16, 2026, https://www.youtube.com/watch?v=m4Ue\_vvBuVk  
18. RED V-Raptor \[X\] and Komodo-X In-Depth workshop \- YouTube, acceso: mayo 16, 2026, https://www.youtube.com/watch?v=FzqvHqiO8Sg  
19. V-RAPTOR XL \[X\] \- RED Digital Cinema, acceso: mayo 16, 2026, https://www.red.com/v-raptor-xl-x-black  
20. KOMODO-X 6K KOMODO 6K v-raptor \[X\] 8K v-raptor XL \[X\] 8K \- Teltec.de, acceso: mayo 16, 2026, https://teltec.de/media/pdf/a3/13/3a/red2024-fullsheet-comparison-specs.pdf  
21. Sony \- Keslow Camera, acceso: mayo 16, 2026, https://www.keslowcamera.com/gear/digital-cameras-and-media/sony/  
22. Compare Sony FX6 vs Sony VENICE 2 8K vs Sony BURANO vs Sony PXW-FX9, acceso: mayo 16, 2026, https://www.bhphotovideo.com/c/compare/Sony\_FX6\_vs\_Sony\_VENICE+2+8K\_vs\_Sony\_BURANO\_vs\_Sony\_PXW-FX9/BHitems/1592066-REG\_1746509-REG\_1786230-REG\_1506002-REG  
23. Sony Digital Cameras (Videofax | Motion Picture and Digital Cinema Camera Equipment Rental Specialists, acceso: mayo 16, 2026, https://www.videofax.com/sony-digital-cameras.htm  
24. Sony Burano? Do you think this camera will be in demand? : r/cinematography \- Reddit, acceso: mayo 16, 2026, https://www.reddit.com/r/cinematography/comments/17da1x6/sony\_burano\_do\_you\_think\_this\_camera\_will\_be\_in/  
25. X-OCN explained \- Sony Pro, acceso: mayo 16, 2026, https://pro.sony/ue\_US/technology/recording-formats/technology-xocn  
26. Real-World Testing with the Sony BURANO | Tech News | Blog & Knowledge \- AbelCine, acceso: mayo 16, 2026, https://www.abelcine.com/articles/blog-and-knowledge/tech-news/real-world-testing-with-the-sony-burano  
27. Camera Comparison Chart | Sony Cine, acceso: mayo 16, 2026, https://sony-cinematography.com/camera-comparison/  
28. Sony Burano: how does a $25k camera have this bad of rolling shutter? \- Reddit, acceso: mayo 16, 2026, https://www.reddit.com/r/cinematography/comments/1bsq1y7/sony\_burano\_how\_does\_a\_25k\_camera\_have\_this\_bad/  
29. Opinion on dual iso? : r/cinematography \- Reddit, acceso: mayo 16, 2026, https://www.reddit.com/r/cinematography/comments/1d9euoi/opinion\_on\_dual\_iso/  
30. Canon C400 vs Canon C300 Mark III vs Canon C500 Mark II: Which cinema camera is best?, acceso: mayo 16, 2026, https://wolfcrow.com/canon-c400-vs-canon-c300-mark-iii-vs-canon-c500-mark-ii-which-cinema-camera-is-best/  
31. Compare Canon C400 vs Canon R5 C vs Canon C300 Mark III vs Canon C500 Mark II \- B\&H Photo, acceso: mayo 16, 2026, https://www.bhphotovideo.com/c/compare/Canon\_C400\_vs\_Canon\_R5+C\_vs\_Canon\_C300+Mark+III\_vs\_Canon\_C500+Mark+II/BHitems/1833189-REG\_1684244-REG\_1557488-REG\_1633519-REG  
32. Canon EOS C70, CANON EOS C50 and EOS R5 C compared \- Canon Georgia, acceso: mayo 16, 2026, https://www.canon.ge/pro/stories/eos-c70-vs-eos-c50-vs-eos-r5-c/  
33. Canon C70 vs C80 vs C300 Mkiii vs C400 Which to Buy \- YouTube, acceso: mayo 16, 2026, https://www.youtube.com/watch?v=fE8q0KAdONQ  
34. Comparing Canon C500 Mark II vs Canon C400 vs Canon C300 Mark ... \- B\&H Photo, acceso: mayo 16, 2026, https://www.bhphotovideo.com/c/compare/Canon\_C500+Mark+II\_vs\_Canon\_C400\_vs\_Canon\_C300+Mark+III\_vs\_Canon\_R5+C/BHitems/1633519-REG\_1833189-REG\_1557488-REG\_1773805-REG  
35. Canon EOS C400: Unleash Your Ambition in 6K, acceso: mayo 16, 2026, https://en.canon-cna.com/cameras/eos-c400/  
36. NEW POST from CineDnews: Canon EOS R5 C Lab Test – Rolling Shutter, Dynamic Range and Latitude \- Reddit, acceso: mayo 16, 2026, https://www.reddit.com/r/CanonR5/comments/vwme0x/new\_post\_from\_cinednews\_canon\_eos\_r5\_c\_lab\_test/  
37. Blackmagic URSA Cine – Tech Specs | Blackmagic Design, acceso: mayo 16, 2026, https://www.blackmagicdesign.com/products/blackmagicursacine/techspecs  
38. Blackmagic URSA Cine 12K LF vs PYXIS 12K: Two Filmmakers, Two Perspectives, One Sensor \- Y.M.Cinema Magazine, acceso: mayo 16, 2026, https://ymcinema.com/2026/02/24/blackmagic-ursa-cine-12k-lf-vs-pyxis-12k-comparison/  
39. So I like Blackmagic, but I never expected these results from their new camera, wow. Blackmagic URSA Cine 12K LF Lab Test: Rolling Shutter, Dynamic Range, and Exposure Latitude | CineD : r/cinematography \- Reddit, acceso: mayo 16, 2026, https://www.reddit.com/r/cinematography/comments/1gph4me/so\_i\_like\_blackmagic\_but\_i\_never\_expected\_these/  
40. Blackmagic URSA Cine 12K lab test is out\! : r/cinematography \- Reddit, acceso: mayo 16, 2026, https://www.reddit.com/r/cinematography/comments/1govuyb/blackmagic\_ursa\_cine\_12k\_lab\_test\_is\_out/  
41. Blackmagic URSA Cine 12K LF Lab Test: Rolling Shutter, Dynamic Range, and Exposure Latitude | REDUSER.NET, acceso: mayo 16, 2026, https://reduser.net/threads/blackmagic-ursa-cine-12k-lf-lab-test-rolling-shutter-dynamic-range-and-exposure-latitude.3830139/  
42. Blackmagic URSA Mini Pro 12K, acceso: mayo 16, 2026, https://www.blackmagicdesign.com/products/blackmagicursaminipro  
43. Blackmagic PYXIS 12K versus 6K Comparison. What's the Difference? \- Sample Footage, acceso: mayo 16, 2026, https://www.youtube.com/watch?v=fRCmv0m9X2A  
44. Differences in image quality between Pyxis 6 and Ursa Cine 12K LF \- Reddit, acceso: mayo 16, 2026, https://www.reddit.com/r/blackmagicdesign/comments/1l2uvfu/differences\_in\_image\_quality\_between\_pyxis\_6\_and/  
45. PYXIS 12K VS PYXIS 6K | Comparison between two Blackmagic Pyxis (resolution, ISO & rolling shutter) \- YouTube, acceso: mayo 16, 2026, https://www.youtube.com/watch?v=4MHR9f43otE  
46. VariCam LT | Products | Cinema Camera Global \- Panasonic Pro AV, acceso: mayo 16, 2026, https://pro-av.panasonic.net/en/cinema\_camera\_varicam\_eva/products/varicam\_lt/  
47. EVA1 | Products | Cinema Camera Global \- Panasonic Pro AV, acceso: mayo 16, 2026, https://pro-av.panasonic.net/en/cinema\_camera\_varicam\_eva/products/eva1/  
48. Specs \- DC-GH7 LUMIX G Mirrorless 4K Cameras \- Panasonic UK & Ireland, acceso: mayo 16, 2026, https://www.panasonic.com/uk/consumer/cameras-camcorders/lumix-mirrorless-cameras/lumix-g-cameras/dc-gh7.specs.html  
49. Features and Specifications \- LUMIX G-Series \- Model DC-GH7 \- Panasonic, acceso: mayo 16, 2026, https://help.na.panasonic.com/answers/features-and-specifications-lumix-g-series-model-dc-gh7/  
50. Panasonic Lumix DC-GH7 review: A mature video camera disguised as a hybrid: DPReview, acceso: mayo 16, 2026, https://www.dpreview.com/reviews/panasonic-lumix-dc-gh7-review  
51. LUMIX BS1H | Products | Cinema Camera Global \- Panasonic Pro AV, acceso: mayo 16, 2026, https://pro-av.panasonic.net/en/cinema\_camera\_varicam\_eva/products/bs1h/index.html  
52. Specifications | Products | Cinema Camera Global \- Panasonic Pro AV, acceso: mayo 16, 2026, https://pro-av.panasonic.net/en/cinema\_camera\_varicam\_eva/products/s1h/spec/index.html  
53. Z CAM E2, acceso: mayo 16, 2026, https://www.z-cam.com/zcame2/  
54. Z Cam E2-F6 Full-Frame 6K Cinema Camera Review \- Newsshooter, acceso: mayo 16, 2026, https://www.newsshooter.com/2020/09/22/z-cam-e2-f6-full-frame-6k-cinema-camera-review/  
55. E2-F6 | Professional 6K Camera \- Z CAM, acceso: mayo 16, 2026, https://www.z-cam.com/products/professional-cameras/e2-f6/  
56. DJI Ronin 4D \- Specs, acceso: mayo 16, 2026, https://www.dji.com/ronin-4d/specs  
57. Bitrates. Where do you draw the line? \- Page 3 \- Cameras \- EOSHD Forum, acceso: mayo 16, 2026, https://www.eoshd.com/comments/topic/66030-bitrates-where-do-you-draw-the-line/page/3/  
58. Uncovering The EASIEST CAMERAS To Use In Virtual Production | REDUSER.NET, acceso: mayo 16, 2026, https://reduser.net/threads/uncovering-the-easiest-cameras-to-use-in-virtual-production.3812868/  
59. Blackmagic URSA Cine, acceso: mayo 16, 2026, https://www.blackmagicdesign.com/products/blackmagicursacine  
60. AI in Video Surveillance: Trends and Challenges in 2025 \- Tech Electronics, acceso: mayo 16, 2026, https://www.techelectronics.com/ai-in-video-surveillance-trends-and-challenges-in-2025/  
61. Hanwha Vision unveils video surveillance trends for 2025, acceso: mayo 16, 2026, https://hanwhavision.eu/hanwha-vision-unveils-video-surveillance-trends-for-2025/  
62. Is there a technical difference between F-Stop and T-Stop? : r/cinematography \- Reddit, acceso: mayo 16, 2026, https://www.reddit.com/r/cinematography/comments/3av0er/is\_there\_a\_technical\_difference\_between\_fstop\_and/  
63. Aperture, F-Stop, and T-Stop: Precision Cinema Production \- cine lenses \- DZOFILM, acceso: mayo 16, 2026, https://dzofilm.com/en/blog/wikis/73  
64. F-Stops vs T-Stops: The Difference Explained in Plain English | PetaPixel, acceso: mayo 16, 2026, https://petapixel.com/2016/12/30/f-stops-vs-t-stops-difference-explained-plain-english/  
65. Background “movement” in anamorphic rack focus \- why? : r/cinematography \- Reddit, acceso: mayo 16, 2026, https://www.reddit.com/r/cinematography/comments/8c4m0y/background\_movement\_in\_anamorphic\_rack\_focus\_why/  
66. Anamorphic Lens "MUMPS" Effect Explained: Don't Expand Your Face\! \#shorts \- YouTube, acceso: mayo 16, 2026, https://www.youtube.com/shorts/XRVlCwf6KGY  
67. Anamorphic Entry \- Cinematography Mailing List, acceso: mayo 16, 2026, https://www.cinematography.net/edited-pages/AnamorphicEntry.htm  
68. What's the difference? Are they all PL mounts? How do you know if it'll fit? \- Reddit, acceso: mayo 16, 2026, https://www.reddit.com/r/cinematography/comments/1hg4pd6/whats\_the\_difference\_are\_they\_all\_pl\_mounts\_how/  
69. What is the deal with LPL? : r/cinematography \- Reddit, acceso: mayo 16, 2026, https://www.reddit.com/r/cinematography/comments/cw21hq/what\_is\_the\_deal\_with\_lpl/  
70. ARRI Tech Talk: ALEXA LF/ LPL lens mount & PL-to-LPL adpater \- YouTube, acceso: mayo 16, 2026, https://www.youtube.com/watch?v=HHubvML10L0  
71. ARRI Signature Prime Lenses, acceso: mayo 16, 2026, https://www.arri.com/en/cine-lenses/signature-lenses/signature-primes-zooms/signature-primes  
72. ARRI Signature Prime Lenses | B\&H Photo Video, acceso: mayo 16, 2026, https://www.bhphotovideo.com/c/buy/arri-signature-prime-lenses/ci/45436  
73. Arri \- Lenses \- LensProToGo, acceso: mayo 16, 2026, https://www.lensprotogo.com/rent/category/lenses/brand/arri/  
74. S7/i FF \- Cooke Optics, acceso: mayo 16, 2026, https://cookeoptics.com/lens/cooke-s7-i-ff/  
75. Rent Cooke Optics Cine Lenses, acceso: mayo 16, 2026, https://cinevisuals.com/cooke-cine-lenses/  
76. S4/i Prime Lenses \- Cooke Optics, acceso: mayo 16, 2026, https://cookeoptics.com/lens/s4-i-prime/  
77. Panchro/i Classic FF \- Cooke Optics, acceso: mayo 16, 2026, https://cookeoptics.com/lens/cooke-panchro-classic-i-ff/  
78. Compare Cooke S8/i vs Cooke S7/i vs Cooke S4/i | B\&H Photo, acceso: mayo 16, 2026, https://www.bhphotovideo.com/c/compare/Cooke\_S8%2Fi\_vs\_Cooke\_S7%2Fi\_vs\_Cooke\_S4%2Fi/BHitems/1696293-REG\_1426024-REG\_831000-REG  
79. ZEISS Supreme Prime Radiance Diamond 11-Lens Set (PL, Feet) \- Hot Rod Cameras, acceso: mayo 16, 2026, https://hotrodcameras.com/products/zeiss-supreme-prime-radiance-diamond-11-lens-set-pl-feet  
80. Zeiss Supreme Zoom Radiance 70-200mm T2.9 \- Duclos Lenses, acceso: mayo 16, 2026, https://www.ducloslenses.com/products/supreme-zoom-radiance-70200  
81. ZEISS Supreme Prime Radiance 28-80mm T2.9 Cine Zoom Lens (FF, PL Mount, Feet), acceso: mayo 16, 2026, https://www.bandpro.com/zeiss-supreme-prime-radiance-28-80mm-t29-cine-zoom-lens-ff-pl-mount-feet-2597-471.html  
82. Rent Leitz Cine Lenses, acceso: mayo 16, 2026, https://cinevisuals.com/leitz-cine-lenses/  
83. SUMMILUX-C \- Leitz Cine, acceso: mayo 16, 2026, https://www.leitz-cine.com/product/summilux-c  
84. Leitz Cinema Lenses | Precision Optics for Professional Filmmaking \- CBM GmbH, acceso: mayo 16, 2026, https://www.cbm-cine.com/Brands/Leitz/  
85. M 0.8 \- Leitz Cine, acceso: mayo 16, 2026, https://www.leitz-cine.com/product/m-08  
86. Leitz M 0.8 50mm f/1.4 Cine Prime Lens (FF, M Mount, Feet) \- Band Pro, acceso: mayo 16, 2026, https://www.bandpro.com/leitz-m-08-50mm-cine-prime-lens-ff-m-mount-feet-11434-001.html  
87. Angenieux EZ Zoom Premium Kit | Cine Lenses \- AbelCine, acceso: mayo 16, 2026, https://www.abelcine.com/buy/lenses-accessories/cine-lenses/angenieux-ez-lens-series-advanced-kit  
88. Angenieux EZ-1, EZ-2, and EZ-3 Super 35 and Full-Frame Cinema Zoom Lens Kit, acceso: mayo 16, 2026, https://www.bhphotovideo.com/c/product/1885772-REG/angenieux\_ez\_1\_ez\_2\_and\_ez\_3.html  
89. Vista – Tokina Cinema USA, acceso: mayo 16, 2026, https://www.tokinacinemausa.com/collections/vista  
90. Tokina Vista Primes — OLD FAST GLASS, acceso: mayo 16, 2026, https://www.oldfastglass.com/tokina-vista-primes  
91. Tokina Cinema Vista High Speed Prime \- Lensworks Rentals, acceso: mayo 16, 2026, https://www.lensworksrentals.com/sigma-cine-ff-high-speed-prime-1  
92. Vespid Prime T2.1 FF/VV \- DZOFILM Store, acceso: mayo 16, 2026, https://store.dzofilm.com/products/dzofilm-vespid-prime  
93. Compare DZOFilm VESPID vs Sirui SATURN Anamorphic \- B\&H Photo, acceso: mayo 16, 2026, https://www.bhphotovideo.com/c/compare/DZOFilm\_VESPID\_vs\_Sirui\_SATURN+Anamorphic/BHitems/1601843-REG\_1741390-REG  
94. Laowa Proteus 2X Anamorphic Lens Series, acceso: mayo 16, 2026, https://laowacine.com/product/laowa-proteus-2x-anamorphic-series/  
95. Orion Series Anamorphic Lenses \- Atlas Lens Co., acceso: mayo 16, 2026, https://atlaslensco.com/products/orion-series-anamorphic-lenses  
96. Anamorphic format \- Wikipedia, acceso: mayo 16, 2026, https://en.wikipedia.org/wiki/Anamorphic\_format  
97. SIRUI Anamorphic Lenses, Wide Angle Camera Lens for Photos, Videos, Films, acceso: mayo 16, 2026, https://store.sirui.com/collections/anamorphic-lens  
98. Laowa Nanomorph 1.5X Anamorphic Zoom Series (28-55mm / 50-100mm), acceso: mayo 16, 2026, https://laowacine.com/product/laowa-nanomorph-1-5x-anamorphic-zoom-series/  
99. (Mirrorless) Nanomorph 1.5X Anamorphic \- Laowa Cinema Lenses, acceso: mayo 16, 2026, https://laowacine.com/product/laowa-1-5x-nanomorph-27mm-t2-8-35mm-t2-4-50mm-t2-4/  
100. What is Anamorphic Squeeze Factor? 1.33X, 1.5X, 2X Anamorphic \- Blazar Lens, acceso: mayo 16, 2026, https://blazarlens.com/blog/what-is-anamorphic-squeeze-factor-1-33x-1-5x-2x/  
101. Mercury Series Anamorphic Lenses \- Atlas Lens Co., acceso: mayo 16, 2026, https://atlaslensco.com/products/mercury-series-anamorphic-lenses  
102. Atlas Orion 2x Anamorphic Lens Rental, acceso: mayo 16, 2026, https://www.redstarpictures.com/atlas-orion/  
103. Nanomorph 1.5X LF Anamorphic Series \- Laowa Cinema Lenses, acceso: mayo 16, 2026, https://laowacine.com/product/nanomorph-lf-1-5x-anamorphic-series/  
104. (PL/EF) Nanomorph 1.5X Anamorphic \[65mm T2.4 / 80mm T2.4\] \- Laowa Lens, acceso: mayo 16, 2026, https://www.laowalenses.ca/product/pl-ef-nanomorph-1-5x-anamorphic-65mm-80mm-t2-4/  
105. 28-105mm F2.8 DG DN | LENSES \- Sigma, acceso: mayo 16, 2026, https://www.sigma-global.com/en/lenses/a024\_28\_105\_28/  
106. Best Sigma Lenses for Sony, Canon and Nikon Cameras in 2026 \- Digi Tech Trading, acceso: mayo 16, 2026, https://digitech.tv/blog/post/best-sigma-lenses-for-sony-canon-and-nikon-cameras  
107. LENS CATALOGUE \- Sigma, acceso: mayo 16, 2026, https://www.sigma-global.com/en/support/download/SIGMA\_LensCatalogue\_24Spring\_ver2\_EN.pdf  
108. DPReview TV: Sony 50mm F1.4 GM vs Sigma 50mm F1.4 DG DN Art, acceso: mayo 16, 2026, https://www.dpreview.com/videos/2798455099/dpreview-tv-sony-50mm-f1-4-gm-vs-sigma-50mm-f1-4-dg-dn-art  
109. Which ND filter to buy first? What density? ND Buying Guide \- NiSi UK, acceso: mayo 16, 2026, https://nisioptics.ie/which-nd-filter-buy-what-choose/  
110. ND 3.0 Neutral Density Filter \- Schneider-Kreuznach, acceso: mayo 16, 2026, https://schneiderkreuznach.com/en/optical-filters/nd-filters/nd-3-0  
111. NiSi Filters \- Which Neutral Density Filter Do You Need? \- YouTube, acceso: mayo 16, 2026, https://www.youtube.com/watch?v=BGToXuuiiWM  
112. IRND Filters: Explained\! (Tokina vs Schneider vs Tiffen) \- YouTube, acceso: mayo 16, 2026, https://www.youtube.com/watch?v=FioHM6XMNmc  
113. Tiffen Glimmerglass Filter Review \- Alik Griffin | Photography, acceso: mayo 16, 2026, https://alikgriffin.com/tiffen-glimmer-glass-filter-review/  
114. Battle of diffusion filters: Tiffen Black Pro-Mist vs. Tiffen Glimmer Glass vs. Moment Cinebloom | Kristoffer Trolle, acceso: mayo 16, 2026, https://www.kristoffertrolle.com/2021/battle-of-diffusion-filters-tiffen-black-pro-mist-vs-tiffen-glimmer-glass-vs-moment-cinebloom/  
115. Any Examples \- 1/16 Pro Mist, Glimmerglass, Pearlescent ? | REDUSER.NET, acceso: mayo 16, 2026, https://reduser.net/threads/any-examples-1-16-pro-mist-glimmerglass-pearlescent.185884/  
116. Diffusion Filters \- Tiffen Pro Mist, Glimmer Glass, GiAi Black Mist \- YouTube, acceso: mayo 16, 2026, https://www.youtube.com/watch?v=\_SBXeSx0cy8  
117. ARRI SkyPanel X23 Modular LED Panel \- Filmtools, acceso: mayo 16, 2026, https://www.filmtools.com/arri-sky-panel-x23-modular-led-panel.html  
118. Mimik VR \- Kino Flo, acceso: mayo 16, 2026, https://kinoflo.com/mimik/  
119. M-Series M18 \- ARRI, acceso: mayo 16, 2026, https://www.arri.com/resource/blob/31486/1a6209e7e85fadca556066f12b551f72/arri-m-series-m18-data-sheet-en-sep2018-data.pdf  
120. SkyPanel S30-C Arri LED Light L0.0007711 Price BarnDoor, acceso: mayo 16, 2026, https://www.filmandvideolighting.com/arri-skypanel-led-light-s30-c.html  
121. S30-C | C Series | SkyPanel | Lighting \- ARRI, acceso: mayo 16, 2026, https://www.arri.com/en/lighting/led-panel-lights/skypanel-classic/s30-c  
122. arri-skypanel-s60-c-data-sheet-en-data.pdf, acceso: mayo 16, 2026, https://www.arri.com/resource/blob/31124/a3ef8cd7d9f50f5dcd314e9e1b2299de/arri-skypanel-s60-c-data-sheet-en-data.pdf  
123. SkyPanel S60-C \- Lighting \- ARRI, acceso: mayo 16, 2026, https://www.arri.com/en/lighting/led-spotlights/discontinued/s60-c  
124. ARRI SkyPanel X21 Modular LED Panel \- B\&H Photo, acceso: mayo 16, 2026, https://www.bhphotovideo.com/c/product/1787327-REG/arri\_skypanel\_x21\_modular\_led.html  
125. ARRI SkyPanel X Modular All-Weather LED Lighting System with Soft & Hard Light Technology \- X21 Dome Included \- Markertek, acceso: mayo 16, 2026, https://www.markertek.com/product/arr-l1-0048487/arri-skypanel-x-modular-all-weather-led-lighting-system-with-soft-hard-light-technology-x21-dome-included  
126. arri-skypanel-x-data-sheet-en-data.pdf, acceso: mayo 16, 2026, https://www.arri.com/resource/blob/341262/e55242c6535912778f7f39d38f490c90/arri-skypanel-x-data-sheet-en-data.pdf  
127. ARRI SkyPanel X Review \- Newsshooter, acceso: mayo 16, 2026, https://www.newsshooter.com/2024/08/25/arri-skypanel-x-review/  
128. ARRI: Orbiter \- Lux Lighting, acceso: mayo 16, 2026, https://luxlightingllc.com/products/arri-orbiter/  
129. Orbiter Beam \- Lighting \- ARRI, acceso: mayo 16, 2026, https://www.arri.com/en/lighting/led-spotlights/orbiter/accessories/optics/beam  
130. Photometric Data V1.0 Orbiter Beam \- ARRI, acceso: mayo 16, 2026, https://www.arri.com/resource/blob/306136/cc0136747fad8c9129c6f829de217d73/arri-orbiter-beam-photometrics-data.pdf  
131. Shop Creamsource Products \- Adorama, acceso: mayo 16, 2026, https://www.adorama.com/brands/Creamsource  
132. Creamsource Vortex – MACCAM, acceso: mayo 16, 2026, https://www.maccam.tv/collections/creamsource-vortex  
133. Creamsource Vortex24 RGB LED Light Panel K-CSV-24-ESS B\&H Photo, acceso: mayo 16, 2026, https://www.bhphotovideo.com/c/product/1883798-REG/creamsource\_k\_csv\_24\_ess\_vortex24\_1950w\_color\_led.html  
134. DMG Lumiere MINI MIX LED Panel \- B\&H Photo, acceso: mayo 16, 2026, https://www.bhphotovideo.com/c/product/1463097-REG/dmg\_lumiere\_mini\_hl\_mx\_mini\_mix\_lamphead\_100.html  
135. DMG Lumiere by Rosco unveils MAXI MIX LED light \- Newsshooter, acceso: mayo 16, 2026, https://www.newsshooter.com/2019/04/06/dmg-lumiere-by-rosco-unveils-maxi-mix-led-light/  
136. Kino Flo Mimik Rental \- Lighting \- 4Wall Entertainment, acceso: mayo 16, 2026, https://www.4wall.com/rentals/9759353/kino-flo-mimik  
137. Astera Helios Tube 4 Set KIT & Transmitter \- Greenwood Cinema Rentals, acceso: mayo 16, 2026, https://www.greenwoodcine.com/rentals/p/astera-titan-tube-8-set-full-kit-transmitter-box-ipad-honeycrates-grids-p9kn2-4d2x2  
138. The ultimate LED tube by Astera, acceso: mayo 16, 2026, https://astera-led.com/products/titan/  
139. Rainbow 2 – Quasar Science, acceso: mayo 16, 2026, https://www.quasarscience.com/products/rainbow-2  
140. Quasar Science Rainbow 2 Linear RGB LED Tube Light (8') 924-2303 \- B\&H Photo, acceso: mayo 16, 2026, https://www.bhphotovideo.com/c/product/1686129-REG/quasar\_science\_924\_2303\_rainbow\_2\_linear\_led.html  
141. Quasar Science LED Tubes | Lamps | Bulbs \- BarnDoor Lighting, acceso: mayo 16, 2026, https://www.filmandvideolighting.com/quasar-science-led-tubes-lamps-bulbs.html  
142. Nanlux Evoke 2400B Bi-Color LED Spotlight \- Panavision, acceso: mayo 16, 2026, https://www.panavision.com/lighting/lighting-products/heads/product-detail/hop1eal-evoke-2400b  
143. Nanlux Evoke 2400B Bi-Color LED Monolight EV2400BCTNPG2BX B\&H, acceso: mayo 16, 2026, https://www.bhphotovideo.com/c/product/1796782-REG/nanlux\_ev2400bctnpg2bx\_evoke\_2400b\_ctrn\_with.html  
144. Evoke 2400B \- NANLUX, acceso: mayo 16, 2026, https://www.nanlux.com/product-evoke-2400b?t=1715948053403  
145. EVOKE 1200 SERIES \- NANLUX Americas, acceso: mayo 16, 2026, https://www.nanluxamericas.com/evoke-1200-series  
146. Dyno 650C/1200C \- NANLUX, acceso: mayo 16, 2026, https://www.nanlux.com/product-dyno-650c-1200c?t=1731329736329  
147. Aputure Electro Storm CS15 RGB LED Monolight (US Plug) \- B\&H Photo, acceso: mayo 16, 2026, https://www.bhphotovideo.com/c/product/1800069-REG/aputure\_app0307a91\_electro\_cs15us.html  
148. Sale | Aputure, acceso: mayo 16, 2026, https://aputure.com/en-US/collections/sale  
149. Aputure Nova P600c Review \- Does it keep up with the ARRI Skypanel? \- YouTube, acceso: mayo 16, 2026, https://www.youtube.com/watch?v=T-372E0LtTQ  
150. M-SERIES LAMPHEADS \- ARRI, acceso: mayo 16, 2026, https://www.arri.com/resource/blob/66428/9914fb3ffb81e397231a7b526b009450/arri-m-series-tech-specs-poster-data.pdf  
151. M-Series | Daylight \- ARRI, acceso: mayo 16, 2026, https://www.arri.com/en/lighting/daylight-tungsten/daylight/m-series  
152. ARRI 650W Plus Tungsten Fresnel (120-240 VAC) \- B\&H Photo, acceso: mayo 16, 2026, https://www.bhphotovideo.com/c/product/72020-REG/Arri\_531600\_650\_Watt\_Plus\_Tungsten.html  
153. Arri 650 Watt Plus Tungsten Fresnel L1.79400.A \- Filmtools, acceso: mayo 16, 2026, https://www.filmtools.com/ar650watfres.html  
154. Tungsten Kits | Kits | Lighting \- ARRI, acceso: mayo 16, 2026, https://www.arri.com/en/lighting/kits/tungsten-kits  
155. Lee to Rosco Equivalents, acceso: mayo 16, 2026, https://us.rosco.com/en/lee-rosco-equivalents  
156. As a producer of color filters for the performing arts, Rosco has focussed on the science of color for nearly 100 years. But stage, acceso: mayo 16, 2026, https://us.rosco.com/sites/default/files/content/resource/2016-09/Guide\_to\_Color\_Filters.pdf  
157. Color Correction Lighting Gels | Lee Master Location Pack Overview (Part 1\) \- YouTube, acceso: mayo 16, 2026, https://www.youtube.com/watch?v=vPmyUcDtBHQ