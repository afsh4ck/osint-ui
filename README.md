# OSINT-UI
### Professional Open Source Intelligence Platform
OSINT UI es un entorno de escritorio virtual diseñado para profesionales y entusiastas de la Inteligencia de Fuentes Abiertas (OSINT). Proporciona un conjunto de herramientas integradas en una interfaz de estilo "hacker" para facilitar la recopilación y el análisis de información de fuentes públicas.

<img width="1728" height="992" alt="Captura de pantalla 2025-09-02 a las 13 01 39" src="https://github.com/user-attachments/assets/01da5093-d09f-4648-bd1c-c49ed7ed41fd" />

---

## 1. Introducción

El entorno simula un sistema operativo con ventanas que puedes mover, redimensionar, minimizar y maximizar. Cada herramienta está diseñada para una tarea OSINT específica, desde analizar perfiles de redes sociales hasta escanear la infraestructura de un dominio.

<img width="1728" height="992" alt="Captura de pantalla 2025-09-02 a las 13 35 30" src="https://github.com/user-attachments/assets/d111a487-9826-4037-8381-4ed0a73fff32" />

---

## 2. Cómo Utilizar cada Funcionalidad

Para usar una herramienta, simplemente haz clic en su icono en el escritorio para abrir su ventana correspondiente.

### Username Analyzer
Busca un nombre de usuario específico en cientos de plataformas de redes sociales y sitios web para encontrar perfiles existentes.

<img width="1728" height="991" alt="Captura de pantalla 2025-09-02 a las 13 04 17" src="https://github.com/user-attachments/assets/4458d183-9b3b-47bb-a764-87e2ae089d37" />


- **Modo de uso:**
  1. Introduce el nombre de usuario en el campo de texto.
  2. Haz clic en "Analyze". La herramienta escaneará las plataformas y mostrará los resultados.
  3. Los resultados se codifican por colores:
     - **Verde (Found):** Se encontró una cuenta. Puedes hacer clic para visitar el perfil.
     - **Gris (Not Found):** No se encontró una cuenta.
     - **Naranja/Rojo (Error/Filtered):** Hubo un problema al verificar el sitio o se ha filtrado como un falso positivo.
  4. Para mayor precisión, puedes usar el botón "Verify False Positives" para realizar una comprobación más exhaustiva de las cuentas encontradas.
  5. Exporta los resultados en formato JSON con el botón de descarga.

---

### Email Analyzer
Verifica una dirección de correo electrónico para determinar su validez, reputación y presencia online.

<img width="3840" height="1666" alt="image" src="https://github.com/user-attachments/assets/c2a80d6e-66f5-4c53-b89b-a1761f6fe846" />

- **Modo de uso:**
  1. Introduce la dirección de correo electrónico a analizar.
  2. Haz clic en "Analyze".
  3. La herramienta te proporcionará un resumen técnico (validez de la sintaxis, registros MX, SPF, DMARC) y una evaluación de riesgo.
  4. También analizará con la API de Dymo si puede ser un email de phising, corporativo, no-reply, etc...
  5. Puedes generar "Google Dorks" para iniciar una investigación más profunda sobre ese correo en Google.
  6. Exporta los resultados en formato JSON.

---

### Phone Analyzer
Recopila información básica sobre un número de teléfono, incluyendo su tipo de línea (móvil, fijo), país y formato internacional.

<img width="1534" height="936" alt="Captura de pantalla 2025-09-02 a las 13 13 08" src="https://github.com/user-attachments/assets/c1e8a746-6dc7-466e-96ba-9ecfd93c77af" />

- **Modo de uso:**
  1. Introduce el número de teléfono en formato internacional (ej: +14155552671).
  2. Haz clic en "Analyze".
  3. Revisa la información de formato, país y tipo de línea.
  4. Genera "Google Dorks" para buscar el número de teléfono en la web.
  5. Exporta los resultados en formato JSON.

---

### Domain Analyzer
Obtiene información pública sobre un dominio, incluyendo datos de WHOIS, registros DNS y una lista de subdominios comunes validados.

<img width="1535" height="981" alt="Captura de pantalla 2025-09-02 a las 13 17 06" src="https://github.com/user-attachments/assets/587f71e1-4186-495d-bd4a-75167664947e" />


- **Modo de uso:**
  1. Introduce el nombre de dominio (ej: google.com).
  2. Haz clic en "Analyze".
  3. Explora la información de WHOIS (registrador, fechas de creación/expiración).
  4. Revisa la tabla de registros DNS (A, MX, TXT, etc.).
  5. Consulta la lista de subdominios que se ha confirmado que existen.
  6. Genera "Google Dorks" para buscar el dominio en la web.
  7. Exporta los resultados en formato JSON.

---

### Port Scanner
Escanea una dirección IP o un dominio para descubrir qué puertos están abiertos y qué servicios podrían estar ejecutándose en ellos.

<img width="1537" height="970" alt="Captura de pantalla 2025-09-02 a las 13 20 41" src="https://github.com/user-attachments/assets/b21ea5dd-9968-4c30-a565-d3f701df7c61" />


- **Modo de uso:**
  1. Introduce la IP o el dominio a escanear.
  2. Elige el tipo de escaneo:
     - **Fast Scan:** Comprueba los 100 puertos más comunes. Rápido e ideal para una primera pasada.
     - **Complete Scan:** Comprueba los 1000 puertos más comunes. Más lento pero más exhaustivo.
  3. Haz clic en "Scan".
  4. Revisa la tabla de resultados para ver los puertos abiertos, cerrados o filtrados.
  5. Exporta los resultados en formato JSON.

---

### Reputation Checker
Comprueba la reputación de una IP o un dominio consultando bases de datos de inteligencia de amenazas (CTI) para ver si está asociado con actividades maliciosas.

<img width="1535" height="882" alt="Captura de pantalla 2025-09-02 a las 13 22 45" src="https://github.com/user-attachments/assets/89be3446-bedb-4796-9601-0e75c26c8ac6" />


- **Modo de uso:**
  1. Introduce la IP o el dominio.
  2. Haz clic en "Check".
  3. La herramienta te dará un veredicto (Benign, Malicious) y una puntuación de riesgo.
  4. Revisa los detalles de las fuentes de inteligencia de amenazas consultadas.
  5. Genera "Google Dorks" para buscar el dominio en la web.
  6. Exporta el informe en formato JSON.

---

### Metadata Extractor
Extrae datos EXIF ocultos de una imagen, como la ubicación GPS con link a Google Maps, el modelo de la cámara, fechas y otros detalles técnicos.

<img width="1537" height="934" alt="Captura de pantalla 2025-09-02 a las 13 31 37" src="https://github.com/user-attachments/assets/31f98095-2129-48f1-b99f-eafdbac73410" />


- **Modo de uso:**
  1. Puedes analizar una imagen desde una URL o subiendo un archivo desde tu ordenador.
  2. Pega la URL o selecciona el archivo y haz clic en "Extract" o "Upload Image".
  3. Si se encuentran datos EXIF, se mostrarán en tarjetas:
     - **Camera:** Marca y modelo.
     - **Timestamps:** Fechas de creación/modificación.
     - **GPS Location:** Si hay coordenadas, se mostrarán junto a un enlace a Google Maps.
     - **Raw EXIF Data:** Una tabla completa con todos los metadatos encontrados.
  4. Exporta los resultados en formato JSON.

---

### Hash Analyzer
Identifica el tipo de algoritmo de un hash (ej: MD5, SHA-256, bcrypt) con opción de crackearlo online a través de Crackstation.

<img width="3078" height="1486" alt="image" src="https://github.com/user-attachments/assets/b4e96c45-7fee-47b6-a77b-dfc5d09431e4" />


- **Modo de uso:**
  1. Pega el hash en el campo de texto.
  2. Haz clic en "Identify".
  3. La herramienta mostrará una lista de los posibles tipos de hash con una probabilidad estimada para cada uno.
  4. Se proporciona un enlace a CrackStation, un servicio online para intentar Crackear el hash si es de un tipo común.
  5. Exporta los resultados en formato JSON.

