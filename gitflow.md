# Gitflow

## Ramas principales

- **main/master**: Rama principal de producción.
- **qa**: Rama para realizar las pruebas.
- **develop**: Rama para la integración de desarrollos.

## Creación de ramas

Utilizamos el estándar [GitFlow](https://www.gitkraken.com/learn/git/git-flow), y las ramas salen de `develop`:

- **feature/[nombre-modulo / id-tarea-jira]**
- **bugfix/[nombre-descripción / id-tarea-jira]**
- **hotfix/[nombre-descripción / id-tarea-jira]** → sale de `main/master`
- **release/sp1-nombre-modulo** → se etiqueta desde `main/master`

## Reglas de trabajo

- No se permiten `commits` o `push` directos a las ramas mencionadas anteriormente
- Los **Pull Requests (PR)** deben ser aprobados por el arquitecto

### Reglas para los Pull Requests (PR)

- El título del PR debe:
  - Estar escrito en inglés y en minúsculas
  - Debe tener un descripción corta y clara de los cambios o usar el ID de la tarea en Jira
  - Seguir la estructura definida en [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/), según el contenido del envío, ejemplos:
    - `feat: JIRA-123`
    - `fix: login process adjustment`
- La descripción del PR debe contener información general de los cambios realizados o los commits generados
- Se le debe asignar el PR al arquitecto para su revisión

### Reglas para los commits

- Los commits deben estar escritos en inglés y en minúsculas.
  - Ejemplo: `feat: added thor.json file`
- Deben seguir la estructura definida en [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/), según el contenido del envío, ejemplos:
  - `feat: added thor.json file`
  - `fix: updated thor.json file on line 20`
  - `docs: updated readme.md file with documentation about install program`
  - `chore: completed task jira number 1234`
  - `ci/cd: changes to our ci configuration files and scripts`