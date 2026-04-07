# EV_01 - Gestión de Ciclo de Vida y Automatización

Este repositorio ha sido creado para demostrar el dominio de estrategias de control de versiones, flujos de trabajo colaborativos y la implementación de CI/CD (Integración Continua) utilizando **GitFlow**.

## Objetivo del Proyecto
El proyecto simula un entorno de desarrollo real donde se gestionan cambios a través de diferentes ramas, se aplican correcciones de emergencia (hotfixes) y se automatizan tareas básicas mediante GitHub Actions.

##Tecnologías Utilizadas
- Git & GitHub: Control de versiones y alojamiento de código.
- GitHub Actions: Automatización de flujos de trabajo.
- Markdown: Documentación técnica.

## Estrategia de Ramas (GitFlow)
Seguimos estrictamente el modelo de GitFlow para asegurar la estabilidad del código:

- main: Contiene el código en producción, siempre estable.
- develop: Rama de integración para las nuevas funcionalidades.
- feature/: Ramas dedicadas al desarrollo de nuevas características (ej: `feature/fecha-1`). Se integran a `develop`.
- hotfix/: Ramas para correcciones críticas inmediatas (ej: `hotfix/fix-fecha`). Se integran tanto a `main` como a `develop`.


## Automatización (CI)
Contamos con un flujo de **GitHub Actions** configurado en `.github/workflows/ci.yml` que se dispara automáticamente en cada `push` a la rama `develop`. Actualmente realiza:
1. Validación de sintaxis.
2. Ejecución de scripts de comprobación de entorno.
3. Notificación de estado del flujo.

## Historial de Cambios Recientes
- `feat`: Implementación de lógica de fechas en el archivo principal.
- `fix`: Corrección de errores de formato en la visualización de datos.
- `ci`: Configuración inicial del workflow de integración continua.

## Se utiliza Pull Request para integrar cambios:

- Cada feature requiere un PR hacia develop
- Cada hotfix requiere un PR hacia main
- Antes del merge se revisan los cambios
- Se valida que el código funcione correctamente
