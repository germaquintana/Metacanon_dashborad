# Metacanon — arquitectura v0.1 (13/11/2026)

## Propósito
Dashboard público federado que reúne enlaces y metadatos expresamente publicables, sin convertirse en fuente de verdad de otros ámbitos.

## Separación
- Laboral: fuente de verdad independiente en `germaquintana/Gestionambientaltrabajo_recoleta`.
- Personal: fuente privada por definir.
- Participación política: fuente separada por definir, sin uso de recursos institucionales.
- Transversal: clasificación y permisos por proyecto.

## Política de datos
**Nunca** incluir credenciales, tokens, expedientes, datos personales, correos, tareas privadas, filiaciones políticas individuales, registros internos o JSON privado en GitHub Pages. Un filtro de interfaz NO constituye control de acceso. Cualquier vista privada debe usar autenticación y backend autorizados, separados de los artefactos públicos.

## Contrato de integración futuro
Cada adaptador deberá exponer exclusivamente campos autorizados: `source_id`, `scope`, `title_public`, `status_public`, `last_verified_at`, `source_url_public`. Los conteos no disponibles se representan como null/— y nunca como cero. No hay adaptadores activos en v0.1.

## Fases
1. Inventariar fuentes y clasificación de acceso.
2. Validar contratos y permisos.
3. Implementar adaptadores de solo lectura y pruebas de filtración.
4. Incorporar métricas verificadas y frescura de datos.
5. Implementar vista privada autenticada fuera de Pages.
6. Monitorear, auditar y documentar cambios.

## Publicación
Archivo estático `index.html` en raíz, compatible con GitHub Pages desde rama main y carpeta / (requiere habilitar Pages en Settings > Pages si no está habilitado). La existencia de este archivo no confirma el despliegue.
