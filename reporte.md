# DEVOPS CONTINUOUS FEEDBACK

## Resumen ejecutivo

Las siguientes mejoras ayudarán a incrementar la madurez DevOps del repositorio.

### 🔴 Alta prioridad

- Docker build funciona

---

## Roadmap sugerido para alcanzar el 100%

1. Docker build funciona

---

## Cómo resolver los GAPs

### Docker build funciona

Impacto: El contenedor no puede construirse correctamente.

#### Cómo resolver

- Validar sintaxis Dockerfile
- Ejecutar docker build localmente
- Revisar COPY y CMD

#### Ejemplo

```

FROM node:20-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

CMD ["npm","start"]

```

---

## Tabla evaluación


| IE | Qué se revisará |
|---|---|
| IE1 | Dockerfile existe |
| IE1 | Docker build funciona |
| IE1 | Imágenes optimizadas |
| IE1 | Multi-stage build |
| IE2 | Existen tests |
| IE2 | Pipeline ejecuta tests |
| IE2 | Coverage equivalente JaCoCo |
| IE3 | Dependabot configurado |
| IE3 | SonarCloud/Snyk |
| IE3 | Bloqueos seguridad needs |
| IE3 | Limits CPU/MEM |
| IE3 | Reservations CPU/MEM |
| IE4 | Deploy automático |
| IE4 | README documentado |
| IE5 | Docker Compose/K8s |
| IE5 | Múltiples servicios |
| IE5 | Healthchecks |
| IE5 | Volumes |
| IE5 | Networks |


---

## Resultado revisión


| IE | Evaluación | Estado |
|---|---|---|
| IE1 | Dockerfile existe | ✅ IMPLEMENTADO |
| IE1 | Multi-stage build | ✅ IMPLEMENTADO |
| IE1 | Imágenes optimizadas | ✅ IMPLEMENTADO |
| IE1 | Docker build funciona | ⚠️ MEJORA PENDIENTE |
| IE4 | Pipeline GitHub Actions | ✅ IMPLEMENTADO |
| IE2 | Pipeline ejecuta tests | ✅ IMPLEMENTADO |
| IE3 | SonarCloud/Snyk | ✅ IMPLEMENTADO |
| IE3 | Bloqueos seguridad needs | ✅ IMPLEMENTADO |
| IE4 | Deploy automático | ✅ IMPLEMENTADO |
| IE2 | Tecnología detectada | ✅ IMPLEMENTADO |
| IE2 | Coverage equivalente JaCoCo | ✅ IMPLEMENTADO |
| IE3 | Dependabot configurado | ✅ IMPLEMENTADO |
| IE5 | Docker Compose/K8s | ✅ IMPLEMENTADO |
| IE5 | Múltiples servicios | ✅ IMPLEMENTADO |
| IE5 | Healthchecks | ✅ IMPLEMENTADO |
| IE5 | Volumes | ✅ IMPLEMENTADO |
| IE5 | Networks | ✅ IMPLEMENTADO |
| IE3 | Limits CPU/MEM | ✅ IMPLEMENTADO |
| IE3 | Reservations CPU/MEM | ✅ IMPLEMENTADO |
| IE4 | README documentado | ✅ IMPLEMENTADO |


---

## Detalle validaciones

### IE1 - Dockerfile existe

- Estado: ✅ IMPLEMENTADO
- Detalle: Dockerfile encontrado

- Evidencia:
```
Dockerfile
```


### IE1 - Multi-stage build

- Estado: ✅ IMPLEMENTADO
- Detalle: Usa multi-stage

- Evidencia:
```
Dockerfile revisado
```


### IE1 - Imágenes optimizadas

- Estado: ✅ IMPLEMENTADO
- Detalle: Usa imágenes optimizadas

- Evidencia:
```
Dockerfile revisado
```


### IE1 - Docker build funciona

- Estado: ⚠️ MEJORA PENDIENTE
- Detalle: Docker build falló

- Evidencia:
```
#0 building with "default" instance using docker driver

#1 [internal] load build definition from Dockerfile
#1 transferring dockerfile: 349B 0.1s done
#1 DONE 0.1s

#2 [auth] library/eclipse-temurin:pull token for registry-1.docker.io
#2 DONE 0.0s

#3 [internal] load metadata for docker.io/library/eclipse-temurin:17-jre-alpine
#3 DONE 0.5s

#4 [internal] load metadata for docker.io/library/eclipse-temurin:17-jdk
#4 DONE 0.5s

#5 [internal] load .dockerignore
#5 transferring context: 2B done
#5 
```

- Qué falta: Corregir Docker build


### IE4 - Pipeline GitHub Actions

- Estado: ✅ IMPLEMENTADO
- Detalle: 2 workflow(s) detectados

- Evidencia:
```
/home/runner/work/ev_01/ev_01/.github/workflows/ep02-devops-continuous-feedback.yml, /home/runner/work/ev_01/ev_01/.github/workflows/ci-cd.yml
```


### IE2 - Pipeline ejecuta tests

- Estado: ✅ IMPLEMENTADO
- Detalle: Ejecuta tests

- Evidencia:
```
Workflow revisado
```


### IE3 - SonarCloud/Snyk

- Estado: ✅ IMPLEMENTADO
- Detalle: Tiene seguridad

- Evidencia:
```
Workflow revisado
```


### IE3 - Bloqueos seguridad needs

- Estado: ✅ IMPLEMENTADO
- Detalle: Usa needs

- Evidencia:
```
Workflow revisado
```


### IE4 - Deploy automático

- Estado: ✅ IMPLEMENTADO
- Detalle: Tiene deploy

- Evidencia:
```
Workflow revisado
```


### IE2 - Tecnología detectada

- Estado: ✅ IMPLEMENTADO
- Detalle: java

- Evidencia:
```
Archivos proyecto
```


### IE2 - Coverage equivalente JaCoCo

- Estado: ✅ IMPLEMENTADO
- Detalle: Coverage detectado para java

- Evidencia:
```

Tecnología: java

Coverage esperado:
JaCoCo

Keywords:
jacoco, jacocoTestReport, jacocoTestCoverageVerification, toolVersion, minimum =, violationRules
      
```


### IE3 - Dependabot configurado

- Estado: ✅ IMPLEMENTADO
- Detalle: Dependabot encontrado

- Evidencia:
```
.github/dependabot.yml
```


### IE5 - Docker Compose/K8s

- Estado: ✅ IMPLEMENTADO
- Detalle: docker-compose encontrado

- Evidencia:
```
docker-compose.yml
```


### IE5 - Múltiples servicios

- Estado: ✅ IMPLEMENTADO
- Detalle: 2 servicios

- Evidencia:
```
app, db
```


### IE5 - Healthchecks

- Estado: ✅ IMPLEMENTADO
- Detalle: Tiene healthchecks

- Evidencia:
```
docker-compose revisado
```


### IE5 - Volumes

- Estado: ✅ IMPLEMENTADO
- Detalle: Tiene volumes

- Evidencia:
```
docker-compose revisado
```


### IE5 - Networks

- Estado: ✅ IMPLEMENTADO
- Detalle: Tiene networks

- Evidencia:
```
docker-compose revisado
```


### IE3 - Limits CPU/MEM

- Estado: ✅ IMPLEMENTADO
- Detalle: Tiene limits

- Evidencia:
```
docker-compose revisado
```


### IE3 - Reservations CPU/MEM

- Estado: ✅ IMPLEMENTADO
- Detalle: Tiene reservations

- Evidencia:
```
docker-compose revisado
```


### IE4 - README documentado

- Estado: ✅ IMPLEMENTADO
- Detalle: README encontrado

- Evidencia:
```
README.md
```
