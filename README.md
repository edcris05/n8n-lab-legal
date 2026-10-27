# n8n Lab — documentación pública para Meta

Sitio estático independiente del laboratorio privado. Responsable: **Edgar Cristian González**, persona física y desarrollador independiente en Argentina. n8n Lab es un proyecto personal de demostración tecnológica, sin sociedad constituida ni servicio comercial operativo.

El correo de los HTML es el contacto configurado en Meta. No se publica domicilio particular ni teléfono personal. El sitio no contiene scripts, formularios, analítica ni recursos externos automáticos.

## Repositorio previsto y estado

Usuario GitHub confirmado por la cuenta autenticada localmente: **edcris05**.
Nombre del repositorio público previsto: **n8n-lab-legal**.
Se prepara Git local, sin copiar historial del proyecto privado. **No se creó un remoto ni se publicó el sitio.**

Contenido permitido:

- index.html
- privacidad.html
- terminos.html
- eliminacion.html
- styles.css
- .nojekyll
- README.md

La herramienta administrativa de eliminación y sus pruebas se conservan fuera de esta carpeta y NO deben subirse. Tampoco subir configuraciones, variables, bases, archivos de mensajes, teléfonos, tokens, workflows ni copias de otros proyectos.

## Revisión efectiva de retención

El 06 conserva localmente número remitente, texto, respuesta, identificadores, fechas, estados y solicitudes demo/humanas. Las consultas de auditoría no muestran contenido de participantes. No existe un conversationId separado en este flujo: el vínculo se basa en remitente e identificadores de mensajes; no se atribuyen conversaciones de otros laboratorios por conjetura.

El workflow 06 está configurado para no guardar datos de ejecuciones exitosas, fallidas ni manuales y no tiene datos fijados. Se encontraron cero ejecuciones guardadas de ese workflow. Los contenedores conservan diagnósticos y no tienen rotación de logs configurada. Hay copias de seguridad que requieren revisión por separado.

Existe un procedimiento privado de borrado selectivo por usuario, probado con datos ficticios: simulación sin cambios, huella de confirmación, comprobación de servicio detenido/bot apagado, eliminación en transacción y verificación de conservación de terceros. Trata una base por vez y permite repetir la revisión para backups concretos. No se usó para eliminar datos reales durante las pruebas.

Límites: estados no atribuibles, logs compartidos, otras exportaciones, restauraciones y registros de proveedores requieren tratamiento adicional. No hay TTL, purga programada, borrado físico garantizado ni eliminación de todas las copias. No se promete una capacidad integral inexistente.

GitHub Pages también registra IP de visitantes por seguridad, según su documentación:
https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages#data-collection

## Pendientes antes de publicar como política definitiva

1. Confirmar la supervisión del correo y la gestión humana de solicitudes.
2. Definir y aplicar retención e inventario de copias, revisión de logs y control de restauraciones. Revisar los límites del borrado por usuario.
3. Confirmar cualquier dato legal adicional obligatorio. No inventar ni publicar domicilio particular, teléfono u otra información no autorizada.
4. Revisar texto y fecha, resolver pendientes y sólo entonces retirar los avisos de borrador.
5. Autorizar explícitamente la creación del remoto y la publicación. Preparar archivos no implica esa autorización ni garantiza aprobación de Meta.

Referencia legal oficial: https://www.argentina.gob.ar/normativa/nacional/ley-25326-64790/texto
Estas páginas describen la implementación; no certifican cumplimiento legal ni reemplazan la revisión del responsable.

## Vista previa

Desde esta carpeta:

```bash
python3 -m http.server 8090 --bind 127.0.0.1
```

Revisar http://127.0.0.1:8090/ en escritorio/móvil, contacto y navegación. Detener con Ctrl+C. No es el alojamiento público.

## Publicación futura: sólo después de autorización

Antes de subir, revisar `git status`, `git ls-files` y el historial. Deben contener exclusivamente los siete archivos públicos listados; nunca copiar el historial o remoto del laboratorio privado.

Los comandos siguientes son instrucciones futuras. **No fueron ejecutados**:

```bash
gh repo create edcris05/n8n-lab-legal --public --source=. --remote=origin
git push -u origin main
```

Ejecutarlos únicamente desde esta carpeta independiente y con autorización. No usar `--push` antes de revisar el remoto.

Después, en GitHub: **Settings → Pages → Deploy from a branch → main → /(root) → Save**. Confirmar HTTPS y que cada página abre sin sesión. GitHub puede tardar en completar el despliegue.

Guía oficial:
https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site

## URLs previstas para Meta

Son direcciones previstas, no una afirmación de que ya estén publicadas:

| Campo | URL |
|---|---|
| Sitio web de la app, si se solicita | https://edcris05.github.io/n8n-lab-legal/ |
| Política de privacidad | https://edcris05.github.io/n8n-lab-legal/privacidad.html |
| Términos/condiciones del servicio | https://edcris05.github.io/n8n-lab-legal/terminos.html |
| Instrucciones de eliminación de datos | https://edcris05.github.io/n8n-lab-legal/eliminacion.html |

Elegir **instrucciones de eliminación**, no callback de eliminación: este sitio estático no recibe POST ni devuelve códigos de confirmación. Si Meta exige un callback y no acepta instrucciones, sigue siendo un bloqueo técnico.

No reemplazar el callback de mensajes de WhatsApp por una URL de GitHub Pages. Publicar el sitio no publica automáticamente la app de Meta ni activa el bot.
