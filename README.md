# Abogados Puerto Varas

Landing page oficial de **Abogados Puerto Varas**, un estudio jurídico con atención en Puerto Varas, Región de Los Lagos, Chile.

- Sitio: <https://abogadospuertovaras.cl>
- Repositorio: `bastianaguayolisperguer/abogados-puerto-varas`
- Rama productiva: `main`
- Hosting: Cloudflare Pages
- DNS: Cloudflare
- Registrador: NIC Chile

## Stack

Sitio estático sin frameworks ni dependencias de ejecución:

- HTML5 semántico.
- CSS embebido en `index.html`.
- JavaScript nativo para navegación, animaciones y formulario de WhatsApp.
- Recurso JPG local reutilizado por la interfaz y los metadatos sociales.
- Archivos estándar de rastreo para buscadores.

No existe un proceso de compilación. Cloudflare Pages publica los archivos estáticos desde la raíz del repositorio.

## Estructura

```text
.
├── assets/
│   └── brand-abogados-puerto-varas.jpg
├── docs/
│   ├── checklist-seo.md
│   ├── informe-final-abogados-puerto-varas.md
│   ├── informe-tecnico.md
│   ├── mensaje-entrega-cliente.md
│   └── resumen-ejecutivo-cliente.md
├── index.html
├── robots.txt
├── sitemap.xml
└── README.md
```

## Despliegue GitHub → Cloudflare Pages

1. Los cambios se desarrollan en una rama separada.
2. Se abre un Pull Request hacia `main`.
3. Se revisan contenido, enlaces y validaciones.
4. Al integrar el Pull Request, la conexión existente entre GitHub y Cloudflare Pages inicia el despliegue automático.
5. Cloudflare Pages publica la nueva versión en el dominio configurado.

El dominio raíz y `www` respondieron correctamente por HTTPS durante la revisión del 6 de octubre de 2026. La publicación de esta actualización SEO se completa cuando el Pull Request se integra en `main` y finaliza el despliegue de Cloudflare Pages.

## Cómo actualizar el sitio

1. Crear una rama desde la versión actualizada de `main`.
2. Editar `index.html` y los recursos estrictamente necesarios.
3. Si se agregan páginas públicas, incorporarlas a `sitemap.xml` y revisar enlaces internos.
4. Mantener el canonical de cada página apuntando a su URL preferida.
5. Validar HTML, JSON-LD, enlaces, accesibilidad básica y visualización responsive.
6. Hacer commits claros y abrir un Pull Request.
7. Revisar el despliegue de vista previa antes de integrar.

## Checklist de publicación

- [ ] Revisar textos, teléfonos, dirección y enlaces de WhatsApp.
- [ ] Confirmar que los enlaces externos usen `target="_blank"` con `rel="noopener noreferrer"`.
- [ ] Validar que `index.html`, `robots.txt` y `sitemap.xml` respondan con estado HTTP 200.
- [ ] Comprobar canonical, meta robots, Open Graph y Twitter Card.
- [ ] Validar los datos estructurados con una herramienta compatible con Schema.org.
- [ ] Probar el formulario en escritorio y dispositivo móvil.
- [ ] Revisar la vista previa de Cloudflare Pages.
- [ ] Integrar el Pull Request en `main`.
- [ ] Verificar el dominio final después del despliegue.

## Próximos pasos SEO

- Crear o reclamar el Perfil de Empresa de Google con datos reales del estudio.
- Verificar el dominio en Google Search Console.
- Enviar `https://abogadospuertovaras.cl/sitemap.xml` y solicitar indexación.
- Obtener reseñas reales de clientes sin incentivos ni contenido fabricado.
- Crear páginas internas por área legal en una segunda fase.
- Publicar contenido jurídico útil y local, revisado profesionalmente.
- Evaluar una redirección permanente de `www` al dominio raíz para consolidar una sola URL pública; el canonical ya declara el dominio raíz como preferido.

La optimización técnica facilita el rastreo y la comprensión del sitio, pero no garantiza posiciones específicas en buscadores.
