# 🚚 ISY1101 - Proyecto Semestral DevOps

## Descripción

Este proyecto corresponde a la Evaluación Final Transversal de la asignatura **ISY1101 - Introducción a Herramientas DevOps**.

La solución implementa una plataforma para la gestión de ventas y despachos utilizando una arquitectura basada en contenedores Docker, automatización CI/CD mediante GitHub Actions y publicación automática de imágenes en Docker Hub.

---

# Arquitectura del Proyecto

El sistema está compuesto por los siguientes componentes:

- Frontend desarrollado en React.
- Backend Ventas desarrollado en Spring Boot.
- Backend Despachos desarrollado en Spring Boot.
- Base de datos MySQL.
- Orquestación mediante Docker Compose.
- Automatización CI/CD mediante GitHub Actions.
- Registro de imágenes en Docker Hub.

---

# Tecnologías utilizadas

- Java 21
- Spring Boot
- React
- Node.js
- MySQL 8
- Docker
- Docker Compose
- GitHub
- GitHub Actions
- Docker Hub
- AWS (ECS)

---

# Estructura del proyecto

```
proyecto semestral
│
├── .github
│   └── workflows
│       └── ci.yml
│
├── back-Ventas_SpringBoot
│
├── back-Despachos_SpringBoot
│
├── front_despacho
│
├── docker-compose.yml
│
└── README.md
```

---

# Docker

Cada componente fue dockerizado mediante un Dockerfile independiente.

Se construyen tres imágenes:

- Backend Ventas
- Backend Despachos
- Frontend

---

# Docker Compose

Docker Compose permite levantar todo el entorno local mediante un único comando.

```
docker compose up --build
```

Servicios desplegados:

- frontend
- backend-ventas
- backend-despachos
- mysql

---

# Docker Hub

Las imágenes son publicadas automáticamente mediante GitHub Actions.

Repositorios utilizados:

- backend-ventas
- backend-despachos
- frontend-despacho

---

# GitHub Actions

El pipeline automatiza:

- Compilación del Backend Ventas
- Compilación del Backend Despachos
- Compilación del Frontend
- Construcción de imágenes Docker
- Login automático en Docker Hub
- Publicación automática de imágenes

El workflow se ejecuta automáticamente en cada Push sobre la rama principal.

---

# CI/CD

Pipeline implementado

```
Push a GitHub
        │
        ▼
GitHub Actions
        │
        ▼
Compilación
        │
        ▼
Build Docker
        │
        ▼
Docker Hub
        │
        ▼
AWS ECS
```

---

# Ejecución local

Clonar repositorio

```
git clone https://github.com/cris200304/ISY1101_EP2_Proyecto_Semestral.git
```

Entrar al proyecto

```
cd proyecto semestral
```

Levantar los servicios

```
docker compose up --build
```

---

# URLs

Frontend

```
http://localhost:3000
```

Swagger Backend Ventas

```
http://localhost:8080/swagger-ui/index.html
```

Swagger Backend Despachos

```
http://localhost:8081/swagger-ui/index.html
```

---

# Docker Hub

Usuario

```
cris200304
```

---

# Integrantes

- Cristian Cerda
- Camila Pascal

---

# Estado del proyecto

✔ Frontend funcionando

✔ Backend Ventas funcionando

✔ Backend Despachos funcionando

✔ Docker Compose funcionando

✔ GitHub Actions funcionando

✔ Docker Hub funcionando

✔ Preparado para despliegue en AWS ECS

---

# Asignatura

ISY1101 - Introducción a Herramientas DevOps

Duoc UC
2026