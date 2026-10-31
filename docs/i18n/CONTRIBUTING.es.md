# Contribuir a PROTORHEXIS

[简体中文 / English](../../CONTRIBUTING.md) · [Français](CONTRIBUTING.fr.md) · **Español** · [Русский](CONTRIBUTING.ru.md)

Aceptamos informes de problemas, ideas de investigación, debates de diseño, mejoras de documentación y contribuciones de código, según las reglas de cada repositorio. Esta es una **guía de colaboración predeterminada**: no significa que todos los repositorios acepten contribuciones externas.

## 1. Comprobar el alcance y los permisos

1. Leer `README.md`, `CONTRIBUTING.md`, `AGENTS.md`, la política de seguridad y las instrucciones aplicables del repositorio, si existen.
2. Confirmar si se permiten Issues, Pull Requests y colaboraciones externas. No divulgar contenido, configuración ni permisos de repositorios privados.
3. Las reglas específicas del repositorio, las especificaciones y decisiones aprobadas, las protecciones de ramas y los requisitos de revisión prevalecen sobre esta guía general. Ante un conflicto, consultar a quienes mantienen el proyecto.
4. Buscar Issues y PR anteriores. Antes de cambios importantes de arquitectura, interfaces, gobernanza, datos o compromisos públicos, presentar una propuesta.

## 2. Presentar cambios verificables

- En una Issue, describir el comportamiento observado, el esperado, los pasos para reproducirlo, el impacto y las evidencias; separar hechos de hipótesis.
- Mantener las PR enfocadas. Explicar el objetivo, los contratos afectados, las pruebas realmente ejecutadas, la compatibilidad, los riesgos y cómo revertir el cambio.
- Distinguir objetivo, implementación actual y brecha. Una comprobación no ejecutada debe figurar como `NOT RUN` o `UNVERIFIED`, nunca como `PASS`.
- Vincular la evidencia al entorno, comandos y commit exacto. Las pruebas locales no equivalen a CI remoto ni a autorización para publicar.
- Evitar modificaciones ajenas al objetivo. Las migraciones, cambios de permisos, acciones destructivas o divulgaciones sensibles requieren autorización aplicable.
- No publicar secretos, datos personales, registros privados ni información no autorizada. Para vulnerabilidades, consultar la [política de seguridad](SECURITY.es.md).

## 3. Revisión y estados

`PROPOSED`, `IMPLEMENTED`, `STATIC_VERIFIED`, `LOCAL_PASS`, `REMOTE_CI_PASS`, `UNVERIFIED`, `BLOCKED` y `HOLD` representan niveles distintos de evidencia. Abrir una PR no supone aprobación. Siguen vigentes las revisiones, los controles obligatorios, el commit exacto, los bloqueos `HOLD` y las reglas de publicación del repositorio.

## 4. Conducta de colaboración

Respetamos a las personas y examinamos críticamente las ideas. Son bienvenidos los desacuerdos fundamentados y las correcciones de buena fe; no el acoso, la discriminación, la divulgación de información privada ni los ataques personales. Comunicar incidentes mediante canales adecuados sin difundir datos sensibles públicamente.
