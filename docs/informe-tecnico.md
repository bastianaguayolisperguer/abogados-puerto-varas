# Informe técnico

## 1. Identificación

- Proyecto: Abogados Puerto Varas.
- Repositorio: `bastianaguayolisperguer/abogados-puerto-varas`.
- Dominio canónico: `https://abogadospuertovaras.cl/`.
- Rama productiva: `main`.
- Rama de trabajo: `seo-final-2026`.
- Plataforma: sitio estático sin frameworks.
- Archivo de entrada: `index.html`.

## 2. Archivos

| Ruta | Propósito |
|---|---|
| `index.html` | Documento principal, estilos, contenido, JavaScript y JSON-LD |
| `assets/brand-abogados-puerto-varas.jpg` | Imagen visual reutilizada por la interfaz y metadatos sociales |
| `robots.txt` | Reglas de rastreo y referencia al sitemap |
| `sitemap.xml` | Inventario de URLs públicas indexables |
| `README.md` | Operación técnica y flujo de publicación |
| `docs/` | Entregables para cliente y equipo técnico |

No se agregaron gestores de paquetes, frameworks ni dependencias.

## 3. Cloudflare Pages, DNS y dominio

- Registrador informado: NIC Chile.
- DNS: Cloudflare.
- Hosting: Cloudflare Pages.
- Origen de despliegue: repositorio GitHub.
- Rama de producción: `main`.
- Comando de build: no requerido para el sitio estático.
- Directorio publicado: raíz del repositorio, de acuerdo con la estructura actual.

El 6 de octubre de 2026 se realizaron solicitudes HTTPS de solo lectura:

- `https://abogadospuertovaras.cl/`: HTTP 200.
- `https://www.abogadospuertovaras.cl/`: HTTP 200.
- Servidor reportado: Cloudflare.
- HTTPS/SSL: operativo en ambas variantes.

La integración del Pull Request dispara la publicación solo después de incorporarse a `main`, conforme a la conexión GitHub → Cloudflare Pages informada para el proyecto.

## 4. SEO técnico

### Metadatos

- `title` orientado a servicio, ubicación y áreas principales.
- Meta description con propuesta clara y llamada a contacto.
- Meta robots explícita con `index, follow` y directivas de vista previa.
- Canonical absoluto hacia el dominio raíz.
- `lang="es-CL"` conservado.
- `theme-color` conservado.
- Meta keywords eliminada por no aportar una señal útil a los buscadores modernos.

### Social sharing

Open Graph incluye tipo, locale, nombre del sitio, título, descripción, URL, imagen segura, tipo MIME, dimensiones y texto alternativo. Twitter Card usa una tarjeta de resumen adecuada para la imagen cuadrada existente.

La referencia anterior a `assets/brand-placeholder.jpg` no correspondía a un archivo del repositorio. Fue reemplazada por un recurso real.

### Contenido y encabezados

- Un único H1.
- H2 para secciones.
- H3 para áreas y profesionales.
- Menciones locales moderadas a Puerto Varas y Región de Los Lagos.
- FAQ visible y consistente con el marcado estructurado.

## 5. JSON-LD

El bloque utiliza `@graph` e identificadores estables:

- `WebSite` con referencia a la entidad publicadora.
- Entidad principal con tipos `LegalService`, `LocalBusiness` y `Organization`.
- Dirección y teléfonos confirmados.
- Áreas servidas: Puerto Varas y Región de Los Lagos.
- Materias legales confirmadas mediante `knowsAbout`.
- Cinco nodos `Person` vinculados al estudio.
- `sameAs` de LinkedIn solo para Javier Mancilla Rojas y Silvana Florencia Rosas Urra.
- `FAQPage` con cuatro preguntas que coinciden con el contenido visible.

No se incluyeron precio, horario, correo, coordenadas, reseñas, puntuaciones ni métricas. `BreadcrumbList` se consideró no aplicable a la portada de una landing con una sola URL pública; deberá incorporarse si en una fase futura existe una jerarquía real de páginas.

## 6. Indexabilidad

`robots.txt` permite el rastreo general y declara:

```text
Sitemap: https://abogadospuertovaras.cl/sitemap.xml
```

`sitemap.xml` utiliza el namespace oficial y contiene únicamente:

```text
https://abogadospuertovaras.cl/
```

No se agregaron anclas internas al sitemap porque no son páginas independientes.

## 7. Accesibilidad básica

- Enlace para saltar al contenido.
- HTML semántico con `header`, `nav`, `main`, secciones y `footer`.
- Etiquetas asociadas a campos del formulario.
- Texto alternativo descriptivo para la imagen principal.
- Título para el iframe del mapa.
- Etiquetas accesibles específicas en botones y enlaces de contacto.
- Estado expandido y nombre accesible dinámico en el menú móvil.
- `aria-describedby` en el formulario.
- Soporte para `prefers-reduced-motion` conservado.
- Enlaces externos con `noopener noreferrer`.

## 8. Rendimiento

La misma fotografía JPEG estaba codificada en Base64 tres veces en `index.html`. Se extrajo a `assets/brand-abogados-puerto-varas.jpg` y se reutiliza desde CSS, HTML y metadatos. Beneficios:

- HTML sustancialmente más pequeño.
- Imagen cacheable por el navegador y la CDN.
- URL válida para Open Graph.
- Dimensiones explícitas de `1254 × 1254`.
- Sin cambios visuales en la imagen aprobada.

Se añadió precarga para la imagen principal y prioridad alta en el elemento visible sobre el primer pliegue.

## 9. Formulario y WhatsApp

El formulario no transmite datos a un backend. JavaScript:

1. Lee nombre, teléfono, área y mensaje.
2. Construye un texto legible.
3. Codifica el contenido con `encodeURIComponent`.
4. Abre `https://wa.me/56940736566` en una pestaña nueva.

También existen enlaces directos a ambos teléfonos informados. Las URLs `wa.me` utilizan números internacionales sin signos ni espacios.

## 10. Flujo de actualización

1. Actualizar la rama local desde `main`.
2. Crear una rama descriptiva.
3. Modificar archivos estáticos.
4. Ejecutar las validaciones del checklist.
5. Revisar diferencias y crear commits atómicos.
6. Subir la rama a GitHub.
7. Abrir Pull Request hacia `main`.
8. Revisar la vista previa de Cloudflare Pages.
9. Integrar y comprobar producción.

## 11. Recomendaciones futuras

- Verificar Search Console y enviar el sitemap.
- Crear o reclamar el Perfil de Empresa de Google.
- Configurar, si corresponde, redirección 301 de `www` al dominio raíz.
- Añadir páginas por área legal con contenido original y revisado.
- Incorporar correo institucional y fotografías solo cuando el cliente los confirme.
- Monitorizar errores 404, cobertura de indexación y Core Web Vitals.
- Revalidar JSON-LD y vistas previas sociales después de cada cambio de contenido.
