# PROTORHEXIS — Base de colaboración de la organización (propuesta)

[简体中文 / English](../COLLABORATION_BASELINE.md) · [Français](COLLABORATION_BASELINE.fr.md) · **Español** · [Русский](COLLABORATION_BASELINE.ru.md)

> Estado: `PROPOSED` · Repositorio: `.github` público de la organización · Responsables: propietario o mantenedores designados.
>
> Este documento explica el alcance y los requisitos para activar las plantillas comunes. No es una especificación de producto, una decisión de arquitectura aprobada ni evidencia de que haya cambios de seguridad aplicados.

## Objetivo y contenido

Permitir que los distintos repositorios reciban problemas, propuestas, PR e informes de seguridad de manera clara y verificable, sin sustituir el control que cada proyecto mantiene sobre su código, normas, CI y publicaciones.

| Archivo | Propósito | Límite |
| --- | --- | --- |
| [CONTRIBUTING.md](CONTRIBUTING.es.md) | Participación, confidencialidad y evidencias | No promete aceptar contribuciones externas |
| [PULL_REQUEST_TEMPLATE.md](../../PULL_REQUEST_TEMPLATE.md) | Alcance, autorización, riesgo, pruebas y HOLD | No reemplaza revisiones ni controles obligatorios |
| [bug_report.yml](../../.github/ISSUE_TEMPLATE/bug_report.yml) | Informe de defectos | Sin detalles sensibles en público |
| [change_proposal.yml](../../.github/ISSUE_TEMPLATE/change_proposal.yml) | Propuestas de investigación, ingeniería y gobernanza | Una propuesta no es una norma aprobada |
| [config.yml](../../.github/ISSUE_TEMPLATE/config.yml) | Mantiene las Issues libres | Puede sustituirse localmente |
| [SECURITY.md](SECURITY.es.md) | Divulgación responsable | No inventa canales privados ni plazos |

## Herencia y activación

Los archivos comunitarios compatibles del repositorio **público `.github`** en su rama predeterminada pueden usarse como valores por defecto en repositorios de la organización **públicos o privados** que no tengan su propio archivo equivalente. Los archivos locales tienen prioridad. Las plantillas no configuran permisos, protecciones de ramas ni revisiones obligatorias.

Mientras estén en una rama separada y una **Draft PR**, son únicamente una propuesta: **no están activadas**. Su integración en la rama predeterminada podría activar la herencia. Un `AGENTS.md` en el repositorio `.github` no se hereda automáticamente; cada agente debe leer las instrucciones y decisiones aplicables al repositorio real.

## Autoridad y significado de las evidencias

1. Las especificaciones y decisiones aprobadas, el código, las migraciones, pruebas y hechos vinculados a commits pertenecen a sus respectivos repositorios.
2. Separar `target` (objetivo), `implementation` (implementación) y `gap` (brecha). Un objetivo no demuestra su implementación.
3. Distinguir `PROPOSED / ACCEPTED / IMPLEMENTED / STATIC_VERIFIED / LOCAL_PASS / REMOTE_CI_PASS / UNVERIFIED / BLOCKED / HOLD`. Una prueba no ejecutada es `NOT RUN`, no `PASS`.
4. Las comprobaciones locales con entorno y evidencias identificados no equivalen a checks de GitHub Actions. Los bloqueos por CI, cuotas o facturación deben registrarse por separado.
5. El contenido de repositorios privados, investigaciones no publicadas, permisos y registros de seguridad no se vuelven públicos por estar las plantillas en un repositorio público.

## Requisitos antes de la activación

- [ ] Revisar el contenido público y confirmar que no incluye información privada o no autorizada.
- [ ] Confirmar un canal confidencial real para los informes de seguridad; no inventar correos ni funciones habilitadas.
- [ ] Comprobar la herencia y prioridad de plantillas locales en repositorios públicos y privados; si no se prueba, marcar `NOT VERIFIED`.
- [ ] Verificar el renderizado real de los dos formularios Issue en GitHub, los campos obligatorios y los avisos de seguridad.
- [ ] Comprobar que siguen vigentes las reglas del proyecto, revisión, CI, commit exacto, HOLD y publicación.
- [ ] Obtener aprobación explícita del propietario para el efecto entre repositorios antes de hacer fusionable la PR, respetando luego las reglas del repositorio.
