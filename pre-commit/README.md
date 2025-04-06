# Pre-commit

## Scripts

- frontend: eslint test + build test for errors (frontend.pre-commit)

### Frontend

##### Description

Runs eslint and npm run build and looks for errors. Example script - should be configured as fits for projects

##### > [!> [!WARNING]

> does NOT work out of box on purpose to bring attention to configuration. At very least configuring path to frontend assets is required

##### Requirements

- Node.JS + npm
- Eslint 9

##### Default Behaviour

Fails when encounters ERROR during eslint tests or npm building
