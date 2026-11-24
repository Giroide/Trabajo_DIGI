# Informe THD: Niantic (Niantic Spatial, Inc.)

## 1. Portada

* **Título:** Informe THD: Niantic (Niantic Spatial, Inc.)
* **Autores:** Jorge hernández muñoz, Ivan  Oliinechuk, Telmo Trallero 
* **Fecha:** 24 de noviembre de 2026
* **Módulo:** 1° DAW - DIGI

---

## 2. Datos de la empresa elegida

* **Nombre de la empresa y enlace a la web corporativa:** **Niantic, Inc.** —actualmente centrada en su división tecnológica **Niantic Spatial, Inc.** tras la venta de su catálogo de videojuegos licenciados a Scopely en 2025—. Web corporativa: [https://www.nianticspatial.com/](https://www.nianticspatial.com/) (portal histórico de videojuegos: [https://nianticlabs.com/](https://nianticlabs.com/)).
* **Sector concreto:** Ingeniería de software geoespacial, desarrollo de kits de desarrollo (SDK) de realidad aumentada e inteligencia artificial espacial (*Spatial AI*).
* **Tamaño aproximado:** **Grande** (cuenta con una plantilla estimada de entre 460 y 560 empleados a nivel internacional, superando el umbral de 250 trabajadores que define a una gran empresa).
* **Producto o servicio principal:** Desarrollo de plataformas de mapeo 3D, posicionamiento visual y computación espacial (*Niantic Lightship*) diseñadas para conectar aplicaciones digitales con el mundo físico, además de ser la creadora original de videojuegos móviles geolocalizados como *Ingress* y *Pokémon GO*.
* **Justificación de la elección:** Es una empresa nativa del sector TIC que ejemplifica de forma clara cómo integrar computación en la nube, sensores móviles, inteligencia artificial y realidad aumentada en aplicaciones masivas en tiempo real.

---

## 3. Resumen ejecutivo

**Niantic, Inc.** es una empresa tecnológica estadounidense especializada en el desarrollo de software de realidad aumentada (AR), computación espacial e infraestructura geoespacial a escala planetaria. Aunque alcanzó fama mundial por videojuegos basados en geolocalización (*Ingress*, *Pokémon GO*), su modelo de negocio central gira en torno a la plataforma **Niantic Lightship** y el desarrollo de un **Sistema de Posicionamiento Visual (VPS)** y un **Modelo Geoespacial Grande (LGM)** que permiten a dispositivos móviles y gafas inteligentes interactuar digitalmente con el mundo físico en tiempo real.

Para sostener esta infraestructura que conecta millones de ubicaciones físicas con servidores centrales, Niantic integra de forma crítica las siguientes **cuatro Tecnologías Habilitadoras Digitales (THD)**:

1. **Realidad Aumentada (AR) y Computación Espacial:** Base de la experiencia de usuario para superponer objetos virtuales persistentes y ocluidos sobre el entorno físico.
2. **Inteligencia Artificial (IA) y Visión por Computador:** Motor para el mapeo 3D del mundo real, segmentación semántica del entorno y entrenamiento de modelos espaciales.
3. **Cloud Computing (Computación en la Nube) y Edge Computing:** Infraestructura distribuida que soporta millones de peticiones geoespaciales concurrentes con baja latencia.
4. **Big Data y Analítica Geoespacial:** Procesamiento masivo de telemetría, escaneos 3D aportados por usuarios y datos cartográficos para optimizar rutas, eventos y mapas digitales.

---

## 4. Cuerpo: Análisis de las Tecnologías Habilitadoras Digitales (THD)

### 4.1. Realidad Aumentada (AR) y Computación Espacial

* **Definición breve:** Tecnología que permite integrar elementos gráficos virtuales en tiempo real sobre la visión del mundo físico captada por la cámara de un dispositivo, manteniendo coherencia espacial y física con el entorno.
* **Características principales:**
  * **Persistencia espacial:** Los objetos virtuales permanecen anclados en coordenadas físicas exactas para que múltiples usuarios puedan verlos desde distintos ángulos y en diferentes momentos.
  * **Oclusión dinámica:** Capacidad del software para detectar la profundidad del entorno y ocultar objetos virtuales detrás de obstáculos reales (paredes, personas, mobiliario urbano).
  * **Interacción multiusuario sincronizada:** Varios dispositivos comparten una misma sesión AR en tiempo real sobre un espacio físico común.
* **Aplicación concreta en Niantic:**
  Niantic implementa esta tecnología a través de su **Lightship ARDK (Augmented Reality Developer Kit)** y su **Sistema de Posicionamiento Visual (VPS)**. A diferencia del GPS tradicional —que tiene un margen de error de varios metros y falla en interiores—, el VPS utiliza la cámara del móvil para comparar la geometría del entorno con un mapa 3D preexistente, logrando una localización con precisión centimétrica. Esto se aplica en funciones como *Pokémon Playgrounds* o experiencias empresariales de *Niantic Spatial*, donde un usuario deja un objeto virtual en una plaza pública y otro usuario, horas después, lo encuentra exactamente en el mismo banco.
* **Mejora en la integración IT-OT:**
  En el ecosistema de Niantic, el entorno físico (las calles, edificios, monumentos y el movimiento de los dispositivos en el terreno) actúa como el entorno operativo (**OT**), mientras que los servidores de estado del juego y bases de datos constituyen el entorno **IT**. La AR y el VPS actúan como puente directo entre ambos: traducen la geometría física del mundo real (OT) en coordenadas digitales estructuradas (IT), permitiendo que los sistemas informáticos reaccionen con precisión a cambios físicos en el terreno sin intervención manual.

---

### 4.2. Inteligencia Artificial (IA) y Visión por Computador

* **Definición breve:** Conjunto de algoritmos y redes neuronales profundas capaces de interpretar imágenes, reconocer patrones espaciales y tomar decisiones automatizadas a partir de datos visuales y sensoriales.
* **Características principales:**
  * **Segmentación semántica en tiempo real:** Clasificación píxel a píxel de lo que capta la cámara (cielo, asfalto, vegetación, edificios, agua).
  * **Reconstrucción 3D mediante NeRF y Gaussian Splatting:** Generación de mallas tridimensionales fotorrealistas a partir de secuencias de vídeo 2D tomadas por usuarios.
  * **Inferencia local (On-device ML):** Ejecución de modelos neuronales optimizados directamente en el procesador del teléfono móvil para evitar latencias de red.
* **Aplicación concreta en Niantic:**
  Niantic emplea redes neuronales convolucionales en su motor de **Segmentación Semántica** dentro de Lightship para que las criaturas o elementos virtuales interactúen de forma lógica con el entorno (por ejemplo, que un personaje virtual solo aparezca sobre el césped o evite caminar sobre el agua). Asimismo, la compañía ha desarrollado el **Large Geospatial Model (LGM)**, un modelo de IA entrenado con millones de escaneos visuales aportados por los jugadores (más de 10 millones de ubicaciones escaneadas) capaz de inferir la geometría completa de un lugar incluso desde ángulos que nunca han sido fotografiados.
* **Mejora en la integración IT-OT:**
  Automatiza la digitalización del mundo físico (OT) hacia los sistemas centrales (IT). Antes de integrar visión por computador avanzada, la validación de puntos de interés (Wayspots) requería revisión humana intensiva; ahora, los modelos de IA filtran automáticamente imágenes borrosas, detectan matrículas o rostros para cumplir con la privacidad (RGPD), reconstruyen el modelo 3D del entorno físico y actualizan la base de datos IT sin fricción operativa.

---

### 4.3. Cloud Computing y Edge Computing

* **Definición breve:** Modelo de provisión de recursos informáticos bajo demanda a través de internet (Cloud), complementado con el procesamiento de datos cerca de la fuente donde se generan (Edge) para minimizar la latencia.
* **Características principales:**
  * **Escalabilidad elástica horizontal:** Capacidad de multiplicar automáticamente los nodos de procesamiento ante picos masivos de demanda sin degradar el servicio.
  * **Arquitectura distribuida de baja latencia:** Despliegue de servidores en múltiples regiones geográficas para acercar el cómputo al usuario final.
  * **Procesamiento híbrido (Edge-to-Cloud):** Ejecución de cálculos críticos de renderizado y sensores en el dispositivo móvil (Edge), sincronizando únicamente los estados ligeros con la nube (Cloud).
* **Aplicación concreta en Niantic:**
  Niantic opera sobre **Google Cloud Platform (GCP)** utilizando **Google Kubernetes Engine (GKE)** y bases de datos distribuidas como **Cloud Spanner**. Durante eventos presenciales masivos como los *Pokémon GO Fest* (que congregan a decenas de miles de jugadores simultáneos en un mismo parque físico), la arquitectura de Niantic escala dinámicamente sus microservicios en Kubernetes para gestionar millones de peticiones por segundo sin caídas. Paralelamente, delegan en el *Edge* (el smartphone del usuario) el cálculo de SLAM (Localización y Mapeo Simultáneos) para no saturar el ancho de banda enviando vídeo continuo a la nube.
* **Mejora en la integración IT-OT:**
  Resuelve el cuello de botella de la sincronización entre la movilidad física en tiempo real (OT) y la consistencia de datos centralizada (IT). El procesamiento *Edge* absorbe el ruido y la alta frecuencia de los sensores físicos (giroscopio, acelerómetro, cámara) en el terreno, enviando al entorno *Cloud* (IT) únicamente metadatos limpios y validados, lo que garantiza que el estado lógico de la aplicación coincida al milisegundo con la posición física del usuario.

---

### 4.4. Big Data y Analítica Geoespacial

* **Definición breve:** Conjunto de tecnologías destinadas a capturar, almacenar, procesar y analizar volúmenes masivos de datos heterogéneos (estructurados y no estructurados) asociados a coordenadas geográficas.
* **Características principales:**
  * **Procesamiento de alto volumen y velocidad (Streaming):** Ingesta continua de petabytes de telemetría GPS, interacciones y escaneos visuales.
  * **Indexación espacial jerárquica:** División del globo terráqueo en celdas matemáticas (como la librería *S2 Geometry*) para realizar consultas geográficas ultrarrápidas.
  * **Detección de anomalías en tiempo real:** Análisis estadístico continuo para identificar patrones fraudulentos o incoherencias físicas.
* **Aplicación concreta en Niantic:**
  Niantic utiliza la librería **Google S2 Geometry** para dividir toda la superficie de la Tierra en celdas jerárquicas, lo que permite gestionar su base de datos global de *Wayspots* (puntos de interés físico) y calcular qué elementos aparecen cerca de cada usuario. Además, sus pipelines de Big Data analizan en tiempo real la telemetría de movimiento para detectar sistemas de falsificación de ubicación (*GPS spoofing*): si los datos muestran que un dispositivo recorre 500 kilómetros en dos minutos o carece de las microvariaciones naturales de los sensores físicos, el sistema automatizado bloquea la acción.
* **Mejora en la integración IT-OT:**
  Aporta trazabilidad, seguridad y optimización operativa entre ambos mundos. Permite auditar que las acciones registradas en los servidores IT corresponden realmente a presencia física verificada en el entorno OT, protegiendo la integridad del ecosistema frente a manipulaciones digitales y permitiendo ajustar dinámicamente la carga operativa en zonas físicas con alta densidad de usuarios.

---

### Cuadro resumen

| THD | Herramienta / Tecnología en Niantic | Impacto principal IT-OT |
| :--- | :--- | :--- |
| **Realidad Aumentada** | Lightship ARDK / Niantic VPS | Traduce la geometría física del entorno (OT) en anclajes digitales persistentes (IT). |
| **IA y Visión Artificial** | Segmentación Semántica / LGM | Automatiza la digitalización 3D del mundo real hacia las bases de datos centrales. |
| **Cloud y Edge Computing** | Google Cloud (GKE, Spanner) + SLAM móvil | Sincroniza la alta frecuencia de sensores físicos con microservicios escalables sin latencia. |
| **Big Data Geoespacial** | Google S2 Geometry / Pipelines telemetría | Verifica la autenticidad física de las operaciones digitales y detecta anomalías espaciales. |

---

## 5. Conclusiones

Tras analizar la arquitectura tecnológica de **Niantic (Niantic Spatial, Inc.)**, se concluye que la Tecnología Habilitadora Digital más determinante para su modelo de negocio actual es la **Inteligencia Artificial (IA) y Visión por Computador**.

Aunque las cuatro tecnologías estudiadas trabajan de forma estrechamente acoplada, la IA espacial destaca como el pilar estratégico fundamental por tres motivos principales:

1. **Núcleo de su ventaja competitiva actual:** Tras la venta de su catálogo de videojuegos licenciados a Scopely en 2025, el valor diferencial de Niantic Spatial ya no reside en las franquicias de entretenimiento, sino en su **Large Geospatial Model (LGM)** y en su plataforma de computación espacial. La capacidad de entrenar modelos de IA con millones de escaneos reales crea una barrera de entrada tecnológica muy difícil de replicar para otros competidores del sector TIC.
2. **Motor habilitador del resto de THD:** Sin los algoritmos de visión por computador (segmentación semántica en tiempo real, reconstrucción 3D mediante NeRF y *Gaussian Splatting*), la **Realidad Aumentada** y el **Sistema de Posicionamiento Visual (VPS)** carecerían de precisión centimétrica y coherencia física. Del mismo modo, la IA es indispensable para extraer valor del **Big Data geoespacial** y optimizar qué datos se procesan en el *Edge* antes de enviarse al *Cloud*.
3. **Clave en la integración IT-OT a escala planetaria:** Digitalizar y mantener actualizado un mapa 3D del mundo físico (OT) dentro de bases de datos corporativas (IT) sería económicamente inviable mediante trabajo manual. La IA automatiza este puente de principio a fin: valida escaneos, anonimiza datos sensibles para cumplir con la normativa de privacidad y reconstruye entornos tridimensionales de forma autónoma.

En definitiva, mientras que el *Cloud/Edge Computing* aporta la estabilidad operativa y el *Big Data* garantiza la integridad geográfica, la **Inteligencia Artificial y Visión por Computador** es la tecnología que convierte el mundo físico en un producto digital escalable y monetizable para Niantic.

---

## 6. Fuentes

### Fuentes generales de la empresa
* **Niantic Spatial, Inc. — Web corporativa oficial:** [https://www.nianticspatial.com/](https://www.nianticspatial.com/)
* **Niantic, Inc. — Portal corporativo y sala de prensa:** [https://nianticlabs.com/](https://nianticlabs.com/)

### 6.1. Realidad Aumentada (AR) y Computación Espacial
* **Niantic Lightship — Plataforma oficial para desarrolladores AR:** [https://lightship.dev/](https://lightship.dev/)
* **Documentación técnica de Lightship ARDK y Visual Positioning System (VPS):** [https://lightship.dev/docs/ardk/](https://lightship.dev/docs/ardk/)

### 6.2. Inteligencia Artificial (IA) y Visión por Computador
* **Niantic Research — Publicaciones sobre visión por computador, reconstrucción 3D y Spatial AI:** [https://research.nianticlabs.com/](https://research.nianticlabs.com/)
* **Niantic News — Anuncios técnicos sobre el Large Geospatial Model (LGM) y segmentación semántica:** [https://nianticlabs.com/news](https://nianticlabs.com/news)

### 6.3. Cloud Computing y Edge Computing
* **Google Cloud — Caso de estudio oficial de Niantic (arquitectura escalable con GKE y Spanner):** [https://cloud.google.com/customers/niantic](https://cloud.google.com/customers/niantic)
* **Google Cloud — Documentación técnica de Google Kubernetes Engine (GKE):** [https://cloud.google.com/kubernetes-engine](https://cloud.google.com/kubernetes-engine)
* **Google Cloud — Documentación técnica de Cloud Spanner:** [https://cloud.google.com/spanner](https://cloud.google.com/spanner)

### 6.4. Big Data y Analítica Geoespacial
* **S2 Geometry — Documentación oficial de la librería de indexación espacial jerárquica:** [https://s2geometry.io/](https://s2geometry.io/)
* **Niantic Wayfarer — Portal oficial de gestión y validación de puntos de interés geoespaciales (Wayspots):** [https://wayfarer.nianticlabs.com/](https://wayfarer.nianticlabs.com/)