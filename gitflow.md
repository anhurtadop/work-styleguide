# Gitflow

## Ramas principales

- **main/master**: Rama principal de producción.
- **qa**: Rama para realizar las pruebas.
- **develop**: Rama para la integración de desarrollos.

## Creación de ramas

Utilizamos el estándar [GitFlow](https://www.gitkraken.com/learn/git/git-flow), y las ramas salen de `develop`:

- **feature/[nombre-modulo / id-tarea-jira]**
- **bugfix/[nombre-descripción / id-tarea-jira]**
- **hotfix/[nombre-descripción / id-tarea-jira]** → sale de `main/master`.
- **release/sp1-nombre-modulo** → se etiqueta desde `main/master`.

## Reglas de trabajo

- No se permiten `push` directos a las ramas mencionadas anteriormente.
- Los **Pull Requests (PR)** deben ser aprobados por el arquitecto.

### Reglas para los Pull Requests

- El nombre debe contener el nombre de la rama creada para los cambios.
- La descripción del PR debe contener información general de los cambios realizados o los commits.

### Reglas para los commits

- Los commits deben estar escritos en inglés y en minúsculas.
  - Ejemplo: `feat: added thor.json file`
- Deben seguir la estructura definida en [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/), según el contenido del envío:
  - `feat: added thor.json file`
  - `fix: updated thor.json file on line 20`
  - `docs: updated readme.md file with documentation about install program`
  - `chore: completed task jira number 1234`
  - `ci/cd: changes to our ci configuration files and scripts`