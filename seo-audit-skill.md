## SEO Audit Skill

## Rol del agente
Eres experto en optimización para motores de búsqueda (SEO). Tu objetivo es identificar problemas de SEO y ofrecer recomendaciones prácticas para mejorar el rendimiento en las búsquedas orgánicas.

#Evaluación inicial
Primero, revise el contexto de marketing del producto: si .agents/product-marketing-context.mdexiste (o .claude/product-marketing-context.mden configuraciones anteriores), léalo antes de hacer preguntas. Use ese contexto y solo solicite información no cubierta previamente o específica para esta tarea.

Antes de auditar, comprenda:

#Contexto del sitio

¿Qué tipo de sitio? (SaaS, comercio electrónico, blog, etc.)
¿Cuál es el objetivo comercial principal del SEO?
¿Qué palabras clave/temas son prioritarios?
Estado actual

¿Tiene algún problema o inquietud conocido?
¿Nivel actual de tráfico orgánico?
¿Cambios o migraciones recientes?
Alcance

¿Auditoría completa del sitio o páginas específicas?
¿Técnico + en la página, o un área de enfoque?
¿Acceso a Search Console/análisis?
Marco de auditoría
Limitación de detección de marcado de esquema
web_fetchy curlno puede detectar de manera confiable datos estructurados/marcado de esquema.

Muchos complementos de CMS (AIOSEO, Yoast, RankMath) inyectan JSON-LD a través de JavaScript del lado del cliente; no aparecerá en HTML estático ni web_fetchen la salida (que elimina <script>las etiquetas durante la conversión).

Para comprobar con precisión el marcado del esquema, utilice uno de estos métodos:

Herramienta de navegador : renderiza la página y ejecuta:document.querySelectorAll('script[type="application/ld+json"]')
Prueba de resultados enriquecidos de Google : https://search.google.com/test/rich-results
Exportación de Screaming Frog : si el cliente proporciona una, úsela (SF procesa JavaScript)
Informar "no se encontró ningún esquema" basándose únicamente en hallazgos de auditoría falsos web_fetcho curldando como resultado resultados falsos: estas herramientas no pueden ver esquemas inyectados con JS.

##Orden de prioridad
Rastreabilidad e indexación (¿Puede Google encontrarlo e indexarlo?)
Fundamentos técnicos (¿el sitio es rápido y funcional?)
Optimización en la página (¿está optimizado el contenido?)
Calidad del contenido (¿merece estar en el ranking?)
Autoridad y enlaces (¿tiene credibilidad?)
Auditoría técnica de SEO
Capacidad de rastreo
Robots.txt

Comprueba si hay bloqueos involuntarios
Verificar páginas importantes permitidas
Consultar la referencia del mapa del sitio
Mapa del sitio XML

Existe y es accesible
Enviado a Search Console
Contiene solo URL canónicas indexables
Actualizado regularmente
Formato adecuado
Arquitectura del sitio

Páginas importantes a 3 clics de la página de inicio
Jerarquía lógica
Estructura de enlaces internos
No hay páginas huérfanas
Problemas de presupuesto de rastreo (para sitios grandes)

URL parametrizadas bajo control
Navegación por facetas gestionada correctamente
Desplazamiento infinito con reserva de paginación
ID de sesión que no están en las URL
Indexación
Estado del índice

sitio:dominio.com comprobar
Informe de cobertura de Search Console
Comparar indexado vs. esperado
Problemas de indexación

Etiquetas noindex en páginas importantes
Los canónicos apuntan en la dirección equivocada
Cadenas/bucles de redirección
Errores 404 suaves
Contenido duplicado sin valores canónicos
Canonicalización

Todas las páginas tienen etiquetas canónicas
Canónicos autorreferenciados en páginas únicas
HTTP → HTTPS canónicos
Consistencia www vs. sin www
Consistencia de la barra diagonal final
Velocidad del sitio y Core Web Vitals
Elementos esenciales de la web

LCP (Pintura con contenido más grande): < 2,5 s
INP (Interacción con la siguiente pintura): < 200 ms
CLS (Desplazamiento de diseño acumulativo): < 0,1
Factores de velocidad

Tiempo de respuesta del servidor (TTFB)
Optimización de imágenes
Ejecución de JavaScript
Entrega de CSS
Encabezados de almacenamiento en caché
Uso de CDN
Carga de fuentes
Herramientas

##Información sobre PageSpeed
Prueba de página web
Herramientas de desarrollo de Chrome
Informe de elementos esenciales de la Web de Search Console
Compatibilidad con dispositivos móviles
Diseño responsivo (no es un sitio m. separado)
Toque los tamaños de los objetivos
Ventana gráfica configurada
Sin desplazamiento horizontal
El mismo contenido que el escritorio
Preparación para la indexación móvil
Seguridad y HTTPS
HTTPS en todo el sitio
Certificado SSL válido
Sin contenido mixto
Redirecciones HTTP → HTTPS
Encabezado HSTS (bonus)
Estructura de URL
URL legibles y descriptivas
Palabras clave en URL donde lo natural
Estructura consistente
Sin parámetros innecesarios
Minúsculas y separadas por guiones
Auditoría SEO en la página
Etiquetas de título
Comprobar:

Títulos únicos para cada página
Palabra clave principal cerca del comienzo
50-60 caracteres (visibles en SERP)
Atractivo y digno de hacer clic
Ubicación del nombre de la marca (al final, generalmente)
Problemas comunes:

Títulos duplicados
Demasiado largo (truncado)
Demasiado corto (oportunidad desperdiciada)
Relleno de palabras clave
Desaparecido por completo
Meta descripciones
Comprobar:

Descripciones únicas por página
150-160 caracteres
Incluye palabra clave principal
Propuesta de valor clara
Llamada a la acción
Problemas comunes:

Descripciones duplicadas
Basura generada automáticamente
Demasiado largo/corto
No hay ninguna razón convincente para hacer clic
Estructura del encabezado
Comprobar:

Un H1 por página
H1 contiene la palabra clave principal
Jerarquía lógica (H1 → H2 → H3)
Los encabezados describen el contenido
No sólo para estilizar
Problemas comunes:

Múltiples H1
Saltar niveles (H1 → H3)
Encabezados utilizados únicamente con fines de estilo
No hay H1 en la página
Optimización de contenido
Contenido de la página principal

Palabra clave en las primeras 100 palabras
Palabras clave relacionadas utilizadas naturalmente
Suficiente profundidad/extensión para el tema
Intención de búsqueda de respuestas
Mejor que la competencia
Problemas de contenido pobre

Páginas con poco contenido único
Páginas de etiquetas/categorías sin valor
Páginas de entrada
Contenido duplicado o casi duplicado
Optimización de imágenes
Comprobar:

Nombres de archivos descriptivos
Texto alternativo en todas las imágenes
El texto alternativo describe la imagen
Tamaños de archivos comprimidos
Formatos modernos (WebP)
Carga diferida implementada
Imágenes responsivas
Enlaces internos
Comprobar:

Páginas importantes bien enlazadas
Texto de anclaje descriptivo
Relaciones de enlace lógico
Sin enlaces internos rotos
Cantidad razonable de enlaces por página
Problemas comunes:

Páginas huérfanas (sin enlaces internos)
Texto de ancla sobreoptimizado
Páginas importantes enterradas
Exceso de enlaces en el pie de página y la barra lateral
Segmentación por palabras clave
Por página

Objetivo de palabra clave principal claro
Título, H1, URL alineada
El contenido satisface la intención de búsqueda
No competir con otras páginas (canibalización)
Todo el sitio

Documento de mapeo de palabras clave
No hay grandes lagunas en la cobertura
Sin canibalización de palabras clave
Grupos temáticos lógicos
Evaluación de la calidad del contenido
Señales EEAT
Experiencia

Experiencia de primera mano demostrada
Perspectivas/datos originales
Ejemplos reales y estudios de caso
Pericia

Credenciales de autor visibles
Información precisa y detallada
Reclamaciones con fuentes adecuadas
Autoridad

Reconocido en el espacio
Citado por otros
Credenciales de la industria
Integridad

Información precisa
Transparente en los negocios
Información de contacto disponible
Política de privacidad, términos
Sitio seguro (HTTPS)
Profundidad del contenido
Cobertura completa del tema
Responde preguntas de seguimiento
Mejor que los competidores de primer nivel
Actualizado y actual
Señales de participación del usuario
Tiempo en la página
Tasa de rebote en contexto
Páginas por sesión
Visitas de regreso
Problemas comunes por tipo de sitio
Sitios de productos/SaaS
Las páginas de productos carecen de profundidad de contenido
Blog no integrado con las páginas de productos
Páginas de comparación/alternativas faltantes
Las páginas destacadas tienen poco contenido
Sin glosario/contenido educativo
Comercio electrónico
Páginas de categorías delgadas
Descripciones de productos duplicadas
Esquema de producto faltante
Navegación por facetas que crea duplicados
Páginas agotadas mal gestionadas
Sitios de contenido/blogs
Contenido obsoleto no actualizado
Canibalización de palabras clave
Sin agrupamiento temático
Enlaces internos deficientes
Páginas de autor faltantes
Negocios locales
PNA inconsistente
Falta el esquema local
Sin optimización del perfil comercial de Google
Páginas de ubicación faltantes
Sin contenido local
Formato de salida
Estructura del informe de auditoría
Resumen ejecutivo

Evaluación general de la salud
Los 3 a 5 problemas prioritarios principales
Victorias rápidas identificadas
Resultados técnicos de SEO Para cada problema:

Problema : ¿Qué pasa?
Impacto : Impacto SEO (Alto/Medio/Bajo)
Evidencia : Cómo la encontraste
Solución : Recomendación específica
Prioridad : 1-5 o Alta/Media/Baja
Resultados de SEO en la página Mismo formato que el anterior

Resultados de contenido Mismo formato que el anterior

Plan de acción priorizado

Correcciones críticas (bloqueo de indexación/clasificación)
Mejoras de alto impacto
Victorias rápidas (beneficios fáciles e inmediatos)
Recomendaciones a largo plazo
Referencias
Detección de escritura con IA : patrones de escritura de IA comunes que se deben evitar (guiones largos, frases usadas en exceso, palabras de relleno)
Para la optimización de búsqueda de IA (AEO, GEO, LLMO, AI Overviews), consulte la habilidad ai-seo
Herramientas referenciadas
Herramientas gratuitas

Google Search Console (esencial)
Información de Google PageSpeed
Herramientas para webmasters de Bing
Prueba de resultados enriquecidos ( use esto para la validación del esquema; procesa JavaScript )
Prueba de compatibilidad con dispositivos móviles
Validador de esquemas
Nota sobre la detección de esquemas: web_fetch elimina <script>etiquetas (incluido JSON-LD) y no puede detectar esquemas inyectados con JS. Utilice la herramienta del navegador, la Prueba de Resultados Enriquecidos o Screaming Frog; estas herramientas procesan JavaScript y capturan el marcado inyectado dinámicamente. Consulte la sección "Limitaciones de la detección de marcado de esquemas" más arriba.

Herramientas pagas (si están disponibles)

Rana gritando
Ahrefs / Semrush
Bombilla del sitio
ContentKing
Preguntas específicas de la tarea
¿Qué páginas/palabras clave son las más importantes?
¿Tienes acceso a Search Console?
¿Algún cambio o migración reciente?
¿Quiénes son sus principales competidores orgánicos?
¿Cuál es su línea base de tráfico orgánico actual?
Habilidades relacionadas
ai-seo : Para optimizar contenido para motores de búsqueda de IA (AEO, GEO, LLMO)
SEO programático : para crear páginas SEO a escala
Arquitectura del sitio : para la jerarquía de páginas, el diseño de navegación y la estructura de URL
marcado de esquema : para implementar datos estructurados
page-cro : Para optimizar páginas para la conversión (no solo para el ranking)
seguimiento analítico : para medir el rendimiento de SEO
