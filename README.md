# nodejs-demo-app

Este proyecto es una aplicación Node.js simple con una pipeline de CI/CD implementada usando **GitHub Actions**.

## 🚀 Objetivo del laboratorio

Simular un flujo de entrega continua similar a AWS (CodeCommit, CodeBuild, CodePipeline y CodeDeploy), pero usando:

- GitHub como repositorio.
- GitHub Actions para CI/CD.
- Simulación de despliegue con logs.

## ⚙️ Flujo CI/CD

El pipeline ejecuta lo siguiente:

1. Clona el repositorio.
2. Instala dependencias (`npm install`).
3. Ejecuta pruebas (`npm test`).
4. Simula el despliegue de la app (`echo "Desplegando..."`).

> Cada vez que se hace push a `main`, se activa automáticamente el workflow.

## ✅ Captura de pantalla del pipeline funcionando

![alt text](image.png)

---

## 📁 Estructura del proyecto

```bash
nodejs-demo-app/
├── app.js                     # Archivo principal de la aplicación
├── package.json              # Definición del proyecto y dependencias
├── package-lock.json         # Archivo generado automáticamente por npm
├── README.md                 # Documentación del proyecto
├── node_modules/             # Dependencias instaladas (se ignora en Git)
└── .github/
    └── workflows/
        └── ci-cd.yml         # Pipeline CI/CD con GitHub Actions

---
