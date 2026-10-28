# n8n Lab — documentación pública para Meta

Sitio estático independiente del laboratorio privado. Responsable: **Edgar Cristian González**, persona física y desarrollador independiente en Argentina. n8n Lab es un proyecto personal de demostración tecnológica, sin sociedad constituida ni servicio comercial operativo.

El correo de los HTML es el contacto configurado en Meta. No se publica domicilio particular ni teléfono personal. El sitio no contiene scripts, formularios, analítica ni recursos externos automáticos.

## Repositorio y estado

Usuario GitHub confirmado por la cuenta autenticada localmente: **edcris05**.
Repositorio público independiente: **https://github.com/edcris05/n8n-lab-legal**.
La publicación fue autorizada expresamente por el responsable. El historial es propio, sin copiar el del proyecto privado. La publicación del sitio conserva los avisos de borrador y no resuelve los pendientes documentados abajo. Comprobar el despliegue en Settings → Pages.

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

El receptor conserva número remitente, texto, respuesta, identificadores, fechas, estados y solicitudes demo/humanas. No hay un conversationId separado ni una vinculación fiable con conversaciones de otros laboratorios.

Desde la activación, los mensajes y respuestas nuevos vencen a los **7 días**, junto con las solicitudes vinculadas. Los estados de entrega nuevos vencen a las **24 horas**. La depuración se ejecuta al iniciar y cada 60 minutos mientras funciona el servicio; los envíos en curso se excluyen y se señalan si siguen vencidos. Si el servicio está detenido, la revisión ocurre al reiniciar. Los datos anteriores quedaron preservados sin vencimiento retroactivo: necesitan revisión manual. La lista permitida tiene retirada manual y no se elimina con el TTL de mensajes.

El workflow 06 mantiene desactivado el guardado de datos de ejecución y no tiene datos fijados; se verificaron cero ejecuciones guardadas. Los logs actuales no tienen rotación activa: está preparada una configuración de tres archivos de 1 MiB, pero requiere una intervención posterior. Esto limita por volumen, no por días; el vencimiento temporal de logs sigue pendiente.

No se encontró una tarea automática de backups y las dos copias SQLite conocidas no tienen tablas del 06. La pauta es no incorporar conversaciones a nuevas copias manuales. La auditoría sólo comprueba el directorio conocido y avisa si encuentra registros 06; no elimina archivos ni descubre snapshots externos.

El borrado selectivo inmediato por solicitud está probado con datos ficticios sobre el esquema actualizado. Usa simulación, huella, confirmación, bot apagado y servicio detenido; verifica conservación de terceros. No se ejecutó contra datos reales. No cubre logs, copias externas, proveedores ni datos no atribuibles. No se garantiza borrado forense ni se implementa un registro permanente automático de supresiones.

La activación conservó los datos originales y backups, comprobados mediante huellas. Se dispone de una auditoría local de sólo lectura, fuera de este repositorio, que informa estado de tarea, vencidos, datos anteriores, configuración n8n, logs y copias conocidas sin imprimir teléfonos o mensajes. Los scripts privados y resultados no deben publicarse aquí.

GitHub Pages también registra IP de visitantes por seguridad, según su documentación:
https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages#data-collection

## Pendientes antes de publicar como política definitiva

1. Confirmar la supervisión del correo y la gestión humana de solicitudes.
2. Resolver tratamiento de registros anteriores, logs actuales y copias externas; controlar restauraciones. La retención automática ya está activa para registros nuevos, con las excepciones indicadas.
3. Confirmar cualquier dato legal adicional obligatorio. No inventar ni publicar domicilio particular, teléfono u otra información no autorizada.
4. Revisar texto y fecha, resolver pendientes y sólo entonces retirar los avisos de borrador.
5. La versión inicial y esta actualización cuentan con autorización expresa de publicación. El alojamiento público no garantiza aprobación de Meta; futuras actualizaciones necesitan su correspondiente autorización.

Referencia legal oficial: https://www.argentina.gob.ar/normativa/nacional/ley-25326-64790/texto
Estas páginas describen la implementación; no certifican cumplimiento legal ni reemplazan la revisión del responsable.

## Vista previa

Desde esta carpeta:

```bash
python3 -m http.server 8090 --bind 127.0.0.1
```

Revisar http://127.0.0.1:8090/ en escritorio/móvil, contacto y navegación. Detener con Ctrl+C. No es el alojamiento público.

## Actualizaciones de la publicación

Antes de subir, revisar `git status`, `git ls-files` y el historial. Deben contener exclusivamente los siete archivos públicos listados; nunca copiar el historial o remoto del laboratorio privado.

El remoto público ya fue creado con autorización. Para futuras actualizaciones revisadas, desde esta carpeta:

```bash
git add -- index.html privacidad.html terminos.html eliminacion.html styles.css .nojekyll README.md
git diff --cached --check
git commit -m "Actualizar documentación pública de n8n Lab"
git push -u origin main
```

Ejecutarlos únicamente desde esta carpeta independiente y con autorización para publicar los cambios. Revisar el destino con `git remote -v` antes de subir.

Después, en GitHub: **Settings → Pages → Deploy from a branch → main → /(root) → Save**. Confirmar HTTPS y que cada página abre sin sesión. GitHub puede tardar en completar el despliegue.

Guía oficial:
https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site

## URLs de GitHub Pages para Meta

Verificar que estas direcciones respondan por HTTPS sin iniciar sesión después de cada despliegue:

| Campo | URL |
|---|---|
| Sitio web de la app, si se solicita | https://edcris05.github.io/n8n-lab-legal/ |
| Política de privacidad | https://edcris05.github.io/n8n-lab-legal/privacidad.html |
| Términos/condiciones del servicio | https://edcris05.github.io/n8n-lab-legal/terminos.html |
| Instrucciones de eliminación de datos | https://edcris05.github.io/n8n-lab-legal/eliminacion.html |

Elegir **instrucciones de eliminación**, no callback de eliminación: este sitio estático no recibe POST ni devuelve códigos de confirmación. Si Meta exige un callback y no acepta instrucciones, sigue siendo un bloqueo técnico.

No reemplazar el callback de mensajes de WhatsApp por una URL de GitHub Pages. Publicar el sitio no publica automáticamente la app de Meta ni activa el bot.
