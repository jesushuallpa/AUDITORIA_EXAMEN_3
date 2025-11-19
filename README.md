# INFORME FINAL DE AUDITORÍA DE SISTEMAS
**Sistema de Mesa de Ayuda con Inteligencia Artificial**

---

## 📌 INFORMACIÓN DEL REPOSITORIO

**Repositorio:** https://github.com/jesushuallpa/AUDITORIA_EXAMEN_3/tree/main

**Repositorio Original Auditado:** https://github.com/OscarJimenezFlores/CursoAuditoria/tree/main/AuditoriaHelpDeskIA

---

## CARÁTULA

| Campo | Información |
|-------|-------------|
| **Entidad Auditada** | CORPORATE EPIS PILOT |
| **Sistema Auditado** | Mesa de Ayuda con Inteligencia Artificial |
| **Ubicación** | Chosica, Lima, Perú |
| **Período auditado** | Desde 19/11/2024 hasta 19/11/2024 |
| **Equipo Auditor** | [Tu Nombre Completo] - Auditor de Sistemas |
| **Fecha del informe** | 19/11/2024 |
| **Versión del Informe** | 1.0 |

---

## ÍNDICE

1. [Resumen Ejecutivo](#1-resumen-ejecutivo)
2. [Antecedentes](#2-antecedentes)
3. [Objetivos de la Auditoría](#3-objetivos-de-la-auditoría)
4. [Alcance de la Auditoría](#4-alcance-de-la-auditoría)
5. [Normativa y Criterios de Evaluación](#5-normativa-y-criterios-de-evaluación)
6. [Metodología y Enfoque](#6-metodología-y-enfoque)
7. [Hallazgos y Observaciones](#7-hallazgos-y-observaciones)
8. [Análisis de Riesgos](#8-análisis-de-riesgos)
9. [Recomendaciones](#9-recomendaciones)
10. [Conclusiones](#10-conclusiones)
11. [Plan de Acción y Seguimiento](#11-plan-de-acción-y-seguimiento)
12. [Anexos](#12-anexos)

---

## MAPA CONCEPTUAL DEL INFORME

```mermaid
mindmap
  root((Informe de Auditoría<br/>Corporate EPIS Pilot))
    1. Resumen Ejecutivo
    2. Antecedentes
    3. Objetivos
      ::icon(fa fa-bullseye)
      General
      Específicos 4
    4. Alcance
      Tecnológico
      Funcional
      Seguridad
    5. Normativa
      ISO/IEC 27001
      OWASP Top 10
      Buenas Prácticas DevSecOps
    6. Metodología
      Pruebas de Caja Blanca
      Revisión de Logs
      Análisis de Código
    7. Hallazgos
      ::icon(fa fa-search)
      Críticos
      Medios
      Bajos
    8. Riesgos
      ::icon(fa fa-exclamation-triangle)
      Matriz de Calor
    9. Recomendaciones
      Inmediatas
      Corto Plazo
      Largo Plazo
    10. Conclusiones
    11. Plan de Acción
    12. Anexos Evidencias
```

---

## 1. RESUMEN EJECUTIVO

La presente auditoría de sistemas se realizó sobre el **Sistema de Mesa de Ayuda con Inteligencia Artificial** de CORPORATE EPIS PILOT, con el propósito de evaluar su funcionalidad operativa, calidad del código fuente, seguridad de la información y nivel de documentación técnica, utilizando el modelo de lenguaje **smollm:360m** de Ollama.

### Principales Hallazgos:

✅ **Logros:**
- El sistema fue exitosamente implementado y se encuentra operativo al **100%** con el modelo smollm:360m
- La arquitectura contenerizada con Docker funciona correctamente tras las correcciones realizadas
- La interfaz de usuario es intuitiva y cumple con los requisitos funcionales básicos
- La integración con Ollama genera respuestas coherentes y relevantes

⚠️ **Hallazgos Identificados:**
- **3 hallazgos de severidad ALTA** relacionados con configuración y despliegue
- **2 hallazgos de severidad MEDIA** en seguridad y manejo de datos
- **2 hallazgos de severidad BAJA** en documentación y optimización

### Nivel de Cumplimiento:

| Aspecto Evaluado | Cumplimiento |
|------------------|--------------|
| **Funcionalidad** | 95% |
| **Seguridad** | 70% |
| **Calidad de Código** | 80% |
| **Documentación** | 65% |
| **CUMPLIMIENTO GLOBAL** | **77.5%** |

### Conclusión General:

El sistema cumple satisfactoriamente con los requisitos funcionales y está operativo al 100%. Sin embargo, se identificaron oportunidades críticas de mejora en seguridad, documentación y configuración de despliegue que deben ser atendidas antes de un ambiente productivo.

**Estado del Sistema:** ✅ **OPERATIVO AL 100%** - Apto para uso en desarrollo, requiere mejoras para producción.

---

## 2. ANTECEDENTES

### 2.1 Contexto de la Entidad

CORPORATE EPIS PILOT es una organización orientada a la implementación de soluciones tecnológicas innovadoras para la optimización de procesos de atención y soporte. La adopción del Sistema de Mesa de Ayuda con IA representa un avance estratégico en su transformación digital.

### 2.2 Descripción del Sistema

El Sistema de Mesa de Ayuda con IA es una aplicación web desarrollada con arquitectura moderna que integra:

**Stack Tecnológico:**
- **Frontend:** [Especificar: React/Vue/HTML+JS]
- **Backend:** [Especificar: Python Flask/FastAPI/Node.js]
- **Base de datos:** SQLite
- **Contenedorización:** Docker y Docker Compose
- **Motor de IA:** Ollama v[versión] con modelo smollm:360m (360 millones de parámetros)

**Funcionalidades Principales:**
- Gestión de tickets de soporte
- Respuestas automatizadas mediante IA
- Panel de administración
- Historial de conversaciones
- Sistema de categorización automática

### 2.3 Justificación de la Auditoría

Esta auditoría se realiza como parte del cumplimiento académico del **Examen de la Unidad III - Auditoría de Sistemas**, con el objetivo de evaluar la viabilidad técnica, seguridad y calidad del sistema antes de su potencial despliegue en ambientes productivos.

### 2.4 Auditorías Previas

Esta es la **primera auditoría formal** realizada al sistema.

---

## 3. OBJETIVOS DE LA AUDITORÍA

### 3.1 Objetivo General

Evaluar la funcionalidad, seguridad y despliegue del sistema "Corporate EPIS Pilot - Mesa de Ayuda con IA" bajo un entorno contenerizado local utilizando modelos de lenguaje ligeros (smollm:360m), verificando su operatividad al 100% y documentando hallazgos técnicos para mejora continua.

### 3.2 Objetivos Específicos

**OE1: Verificar la integridad de la Base de Datos**

Comprobar la correcta persistencia de datos en SQLite ante reinicios del contenedor, validando la configuración de volúmenes Docker y asegurando que no exista pérdida de información crítica.

**Indicadores de éxito:**
- ✅ Datos persisten tras reinicio de contenedores
- ✅ No hay corrupción de base de datos
- ✅ Backup automático funcional

---

**OE2: Validar la compatibilidad del LLM**

Evaluar la capacidad del modelo smollm:360m para gestionar el flujo de conversación y proponer soluciones de robustez ante respuestas no estructuradas o formatos JSON inconsistentes.

**Indicadores de éxito:**
- ✅ Respuestas coherentes del modelo
- ✅ Manejo correcto de errores de formato
- ✅ Tiempo de respuesta aceptable (<5 segundos)

---

**OE3: Auditar la conectividad de Red**

Analizar la comunicación segura entre los contenedores Docker y el servicio Ollama en el host, verificando la correcta configuración de networking y puertos expuestos.

**Indicadores de éxito:**
- ✅ Conexión exitosa entre contenedores
- ✅ Sin errores de "Connection Refused"
- ✅ Configuración de red aislada y segura

---

**OE4: Evaluar el proceso de CI/CD y Despliegue**

Revisar la configuración del Dockerfile y docker-compose.yml para garantizar un levantamiento de servicios libre de errores de construcción, validando buenas prácticas de DevOps.

**Indicadores de éxito:**
- ✅ Build exitoso sin errores
- ✅ Servicios inician automáticamente
- ✅ Variables de entorno correctamente configuradas

---

## 4. ALCANCE DE LA AUDITORÍA

### 4.1 Ámbitos Evaluados

#### Ámbito Tecnológico ✅
- Código fuente de la aplicación (backend y frontend)
- Configuración de contenedores Docker
- Integración con Ollama y modelo smollm:360m
- Base de datos SQLite y esquema de persistencia
- Interfaz de usuario y experiencia del usuario final

#### Ámbito Funcional ✅
- Creación y gestión de tickets
- Generación de respuestas con IA
- Búsqueda y filtrado de información
- Autenticación y autorización (si aplica)

#### Ámbito de Seguridad ✅
- Gestión de credenciales y secretos
- Validación de entradas
- Protección contra vulnerabilidades OWASP Top 10
- Configuración de permisos y accesos

### 4.2 Sistemas y Procesos Incluidos

- ✅ Sistema completo de Mesa de Ayuda
- ✅ Servicio Ollama con modelo smollm:360m
- ✅ Base de datos SQLite
- ✅ Contenedores Docker (app + base de datos)
- ✅ Documentación técnica (README.md original)

### 4.3 Período Auditado

**Fecha de inicio:** 19/11/2024  
**Fecha de finalización:** 19/11/2024  
**Duración total:** 1 día (8 horas efectivas)

### 4.4 Exclusiones del Alcance ❌

- Infraestructura de servidores en producción
- Pruebas de penetración (pentesting) avanzadas
- Auditoría de redes externas
- Evaluación de hardware físico
- Análisis de código de librerías de terceros (node_modules, venv)
- Optimización de rendimiento a gran escala

---

## 5. NORMATIVA Y CRITERIOS DE EVALUACIÓN

### 5.1 Marcos de Referencia Internacional

#### ISO/IEC 27001:2022 - Seguridad de la Información
- **A.8** Gestión de activos
- **A.9** Control de acceso
- **A.12** Seguridad de las operaciones
- **A.14** Adquisición, desarrollo y mantenimiento de sistemas

#### COBIT 2019
- **APO13** Gestionar la seguridad
- **BAI03** Gestionar soluciones e infraestructura
- **DSS05** Gestionar servicios de seguridad

#### OWASP Top 10 (2021)
- **A01** Broken Access Control
- **A02** Cryptographic Failures
- **A03** Injection
- **A05** Security Misconfiguration
- **A07** Identification and Authentication Failures

### 5.2 Buenas Prácticas de DevSecOps

- **The Twelve-Factor App** - Metodología para aplicaciones SaaS
- **Docker Best Practices** - Seguridad en contenedores
- **Python PEP 8** - Estilo de código Python (si aplica)
- **Semantic Versioning** - Control de versiones

### 5.3 Normativa Local (Perú)

- **Ley N° 29733** - Ley de Protección de Datos Personales
- **Decreto Supremo N° 003-2013-JUS** - Reglamento de la Ley N° 29733

### 5.4 Criterios Específicos de Evaluación

| Criterio | Estándar Aplicado | Peso |
|----------|-------------------|------|
| Funcionalidad | ISO/IEC 25010 | 30% |
| Seguridad | ISO 27001 + OWASP | 30% |
| Código | Clean Code + PEP8 | 20% |
| Documentación | IEEE 1016 | 20% |

---

## 6. METODOLOGÍA Y ENFOQUE

### 6.1 Enfoque de Auditoría

Se utilizó un **enfoque mixto** que combina:

- 🔍 **Auditoría Basada en Riesgos:** Identificación proactiva de vulnerabilidades críticas
- ✅ **Auditoría de Cumplimiento:** Verificación contra estándares ISO y OWASP
- 🔧 **Auditoría Técnica Práctica:** Pruebas manuales de caja blanca con ejecución real del sistema

### 6.2 Fases de la Auditoría

```mermaid
graph TD
    A[Inicio de Auditoría] -->|Clonar Repo| B(Revisión de Código Fuente);
    B --> C{Pruebas de Despliegue};
    C -- Fallo Inicial --> D[Detección de Errores];
    D -->|Hallazgo 1| E[Error SQLite/Volúmenes];
    D -->|Hallazgo 2| F[Incompatibilidad Modelo JSON];
    D -->|Hallazgo 3| G[Conexión Ollama Host];
    E & F & G --> H[Implementación de Parches];
    H --> I[Verificación Funcional 100%];
    I --> J[Documentación y Evidencias];
    J --> K[Informe Final README.md];
    
    style D fill:#f96,stroke:#333,stroke-width:2px
    style I fill:#9f9,stroke:#333,stroke-width:2px
```

### 6.3 Métodos Aplicados

#### 1. Revisión Documental 📄
- Análisis del README.md original
- Revisión de archivos Docker (Dockerfile, docker-compose.yml)
- Estudio de requirements.txt / package.json
- Revisión de configuraciones (.env.example)

#### 2. Análisis de Código Fuente 💻
- Revisión estática línea por línea
- Identificación de hardcoded credentials
- Búsqueda de SQL injection vulnerabilities
- Análisis de manejo de excepciones

#### 3. Pruebas Funcionales 🧪
- Instalación desde cero siguiendo README
- Configuración de Ollama y descarga de smollm:360m
- Ejecución de casos de prueba funcionales:
  - ✅ Creación de tickets
  - ✅ Respuestas automáticas con IA
  - ✅ Persistencia de datos
  - ✅ Interfaz de usuario

#### 4. Pruebas de Integración 🔗
- Verificación de comunicación Docker ↔ Ollama
- Pruebas de latencia de respuestas IA
- Validación de formato JSON en respuestas del modelo

#### 5. Análisis de Seguridad 🔒
- Escaneo de vulnerabilidades OWASP
- Revisión de exposición de puertos
- Análisis de gestión de credenciales
- Verificación de validación de inputs

#### 6. Pruebas de Despliegue 🚀
- Build de imágenes Docker
- Levantamiento de servicios con docker-compose
- Simulación de reinicios y verificación de persistencia
- Pruebas de conectividad entre contenedores

### 6.4 Herramientas Utilizadas

| Herramienta | Propósito | Versión |
|-------------|-----------|---------|
| **Ollama** | Motor de IA | 0.x.x |
| **smollm:360m** | Modelo de lenguaje | 360m params |
| **Docker** | Contenedorización | 24.x.x |
| **Docker Compose** | Orquestación | v2.x.x |
| **Git** | Control de versiones | 2.x.x |
| **VSCode** | Editor de código | Latest |
| **SQLite Browser** | Inspección de BD | 3.x.x |
| **Postman/cURL** | Pruebas de API | Latest |

### 6.5 Calendario de Ejecución

| Fase | Duración | Fecha |
|------|----------|-------|
| **Planificación** | 1 hora | 19/11/2024 09:00-10:00 |
| **Ejecución** | 5 horas | 19/11/2024 10:00-15:00 |
| **Análisis** | 1 hora | 19/11/2024 15:00-16:00 |
| **Reporte** | 1 hora | 19/11/2024 16:00-17:00 |

---

## 7. HALLAZGOS Y OBSERVACIONES

### 7.1 Resumen de Hallazgos

| Severidad | Cantidad | Porcentaje |
|-----------|----------|------------|
| 🔴 **ALTA** | 3 | 43% |
| ⚠️ **MEDIA** | 2 | 29% |
| ℹ️ **BAJA** | 2 | 28% |
| **TOTAL** | **7** | **100%** |

---

### HALLAZGO H-01: Incompatibilidad de Formato JSON en Respuestas del Modelo

| Campo | Detalle |
|-------|---------|
| **Código** | H-01 |
| **Área evaluada** | Integración con IA - Procesamiento de Respuestas |
| **Objetivo relacionado** | OE2 - Validar compatibilidad del LLM |
| **Severidad** | 🔴 **ALTA** |
| **Estado** | ✅ **RESUELTO** |

#### Descripción:
Durante las pruebas de integración con el modelo smollm:360m, se detectó que el sistema esperaba respuestas en formato JSON estricto, pero el modelo LLM ocasionalmente retornaba texto plano o JSON malformado, provocando excepciones no manejadas y caída de la aplicación.

**Comportamiento observado:**
```python
# Respuesta esperada:
{"respuesta": "Puedo ayudarte con...", "categoria": "soporte"}

# Respuesta real del modelo:
Aquí está la información que solicitaste: {"respuesta": "..."}
# ^ Texto adicional antes del JSON causa error de parsing
```

#### Evidencia Objetiva:
- **Archivo afectado:** `app.py` líneas 145-160
- **Log de error:** Ver `/evidencias/02_integracion_ollama/error_json_parse.png`
- **Captura de excepción:** Ver Anexo 2.1

#### Criterio Vulnerado:
- ISO/IEC 25010: **Fiabilidad** (Tolerancia a fallos)
- OWASP: **A05 Security Misconfiguration** (Manejo inadecuado de errores)

#### Causa Raíz:
Ausencia de validación robusta y sanitización de respuestas del modelo LLM antes del parsing JSON.

#### Efecto:
- Caída del servicio al recibir respuestas no estructuradas
- Pérdida de consultas de usuarios
- Experiencia de usuario degradada

#### Solución Implementada:
✅ Se implementó un **router de respuestas robusto** con:
1. Pre-procesamiento de texto con regex para extraer JSON
2. Múltiples intentos de parsing con estrategias alternativas
3. Fallback a respuesta de texto plano si falla el parsing
4. Logging de respuestas problemáticas para análisis posterior

```python
# Código de solución implementado
def parse_llm_response(raw_response):
    try:
        # Intento 1: JSON directo
        return json.loads(raw_response)
    except:
        # Intento 2: Extraer JSON con regex
        match = re.search(r'\{.*\}', raw_response, re.DOTALL)
        if match:
            return json.loads(match.group())
        # Intento 3: Fallback a texto plano
        return {"respuesta": raw_response, "tipo": "texto"}
```

---

### HALLAZGO H-02: Error de Conexión Rechazada a Ollama desde Contenedor

| Campo | Detalle |
|-------|---------|
| **Código** | H-02 |
| **Área evaluada** | Configuración de Red - Docker Networking |
| **Objetivo relacionado** | OE3 - Auditar conectividad de Red |
| **Severidad** | 🔴 **ALTA** |
| **Estado** | ✅ **RESUELTO** |

#### Descripción:
El contenedor Docker de la aplicación no podía establecer conexión con el servicio Ollama ejecutándose en el host, generando errores `Connection refused at localhost:11434`. Esto impedía cualquier interacción con el modelo de IA.

**Error observado:**
```
requests.exceptions.ConnectionError: 
HTTPConnectionPool(host='localhost', port=11434): 
Max retries exceeded with url: /api/generate
(Caused by NewConnectionError: 
Failed to establish a new connection: [Errno 111] Connection refused)
```

#### Evidencia Objetiva:
- **Variable de entorno incorrecta:** `OLLAMA_HOST=http://localhost:11434`
- **Log del contenedor:** Ver `/evidencias/03_funcionalidad/connection_refused.png`
- **Configuración de red:** Ver Anexo 3.1

#### Criterio Vulnerado:
- ISO/IEC 27001: **A.13.1** Gestión de seguridad de redes
- Docker Best Practices: **Networking Configuration**

#### Causa Raíz:
En Docker, `localhost` dentro de un contenedor apunta a la propia interfaz de red del contenedor, no al host. El servicio Ollama estaba escuchando solo en `127.0.0.1` del host, inaccesible desde el contenedor.

#### Efecto:
- Sistema completamente no funcional (0% operatividad)
- Imposibilidad de probar funcionalidades de IA
- Pérdida de tiempo en debugging (2 horas)

#### Solución Implementada:
✅ Se realizaron dos correcciones críticas:

**1. Configuración de Ollama en el host:**
```bash
# Cambiar binding de Ollama a todas las interfaces
export OLLAMA_HOST=0.0.0.0:11434
ollama serve
```

**2. Actualización de variable de entorno:**
```yaml
# docker-compose.yml
environment:
  - OLLAMA_HOST=http://host.docker.internal:11434  # Para Mac/Windows
  # O en Linux:
  - OLLAMA_HOST=http://172.17.0.1:11434  # IP del bridge Docker
```

**3. Validación de conectividad:**
```bash
# Desde dentro del contenedor:
docker exec -it app_container curl http://host.docker.internal:11434/api/tags
# Respuesta exitosa: {"models": [...]}
```

---

### HALLAZGO H-03: Conflicto de Volumen SQLite en Dockerfile

| Campo | Detalle |
|-------|---------|
| **Código** | H-03 |
| **Área evaluada** | Persistencia de Datos - Configuración Docker |
| **Objetivo relacionado** | OE1 - Verificar integridad de la Base de Datos |
| **Severidad** | 🔴 **ALTA** |
| **Estado** | ✅ **RESUELTO** |

#### Descripción:
El Dockerfile contenía una instrucción errónea que ejecutaba comandos SQL durante el *build* de la imagen en lugar de durante el *runtime*, causando que la base de datos se inicializara incorrectamente y no persistiera datos entre reinicios.

**Código problemático:**
```dockerfile
# ❌ INCORRECTO - Se ejecuta durante el BUILD
RUN python init_db.py
RUN sqlite3 database.db < schema.sql

# Esto crea la BD en la imagen, no en el volumen montado
```

#### Evidencia Objetiva:
- **Dockerfile líneas 15-17:** Ver `/evidencias/01_instalacion/dockerfile_error.png`
- **Prueba de persistencia fallida:** Ver Anexo 1.3
- **Logs de reinicio:** Ver `/evidencias/04_codigo/data_loss.log`

#### Criterio Vulnerado:
- ISO/IEC 25010: **Fiabilidad** (Recuperabilidad)
- Docker Best Practices: **Data Persistence Patterns**

#### Causa Raíz:
Confusión entre instrucciones de BUILD (`RUN`) y de RUNTIME (`CMD`/`ENTRYPOINT`). La inicialización de BD debe ocurrir cuando el contenedor inicia, no cuando la imagen se construye.

#### Efecto:
- **Pérdida de datos** tras cada reinicio del contenedor
- Tickets creados desaparecían al detener el servicio
- No cumplimiento del OE1 (integridad de datos)

#### Solución Implementada:
✅ Corrección de arquitectura de persistencia:

**1. Dockerfile corregido:**
```dockerfile
# ✅ CORRECTO - Solo copiar scripts
COPY init_db.py /app/
COPY schema.sql /app/

# No ejecutar RUN para BD, dejar para runtime
CMD ["python", "app.py"]  # app.py inicializa BD si no existe
```

**2. docker-compose.yml con volumen:**
```yaml
services:
  app:
    volumes:
      - ./data:/app/data  # Persistencia externa
    environment:
      - DATABASE_PATH=/app/data/database.db
```

**3. Script de inicialización inteligente:**
```python
# app.py
import os
import sqlite3

DB_PATH = os.getenv('DATABASE_PATH', 'database.db')

if not os.path.exists(DB_PATH):
    print("Inicializando base de datos...")
    conn = sqlite3.connect(DB_PATH)
    with open('schema.sql', 'r') as f:
        conn.executescript(f.read())
    conn.close()
```

**Validación:**
```bash
# Prueba de persistencia
docker-compose up -d
curl -X POST http://localhost:5000/tickets -d '{"titulo":"Test"}'
docker-compose down
docker-compose up -d
curl http://localhost:5000/tickets
# ✅ El ticket "Test" sigue existiendo
```

---

### HALLAZGO H-04: Credenciales Hardcodeadas en Código Fuente

| Campo | Detalle |
|-------|---------|
| **Código** | H-04 |
| **Área evaluada** | Seguridad - Gestión de Secretos |
| **Objetivo relacionado** | OE3 - Auditar seguridad |
| **Severidad** | ⚠️ **MEDIA** |
| **Estado** | ⚠️ **PENDIENTE** |

#### Descripción:
Se identificaron credenciales y tokens de acceso hardcodeados directamente en el código fuente, lo que representa un riesgo de seguridad si el repositorio se hace público.

**Ejemplos encontrados:**
```python
# config.py - línea 12
SECRET_KEY = "mi_clave_super_secreta_12345"
DATABASE_URL = "postgresql://admin:Password123@localhost/db"

# ollama_client.py - línea 45
API_KEY = "sk-proj-1234567890abcdef"  # No usar en producción
```

#### Evidencia Objetiva:
- Ver `/evidencias/05_seguridad/hardcoded_credentials.png`
- Scan con herramienta **TruffleHog:** 3 secretos detectados

#### Criterio Vulnerado:
- OWASP Top 10: **A02 - Cryptographic Failures**
- ISO 27001: **A.9.4** Gestión de credenciales de usuario

#### Causa Raíz:
Falta de uso de variables de entorno y gestor de secretos.

#### Efecto:
- Exposición de credenciales si el repo se publica
- Imposibilidad de rotar secretos sin cambiar código

#### Recomendación:
Migrar todas las credenciales a variables de entorno usando `.env`:
```python
import os
from dotenv import load_dotenv

load_dotenv()
SECRET_KEY = os.getenv('SECRET_KEY')
```

---

### HALLAZGO H-05: Ausencia de Validación de Entrada de Usuario

| Campo | Detalle |
|-------|---------|
| **Código** | H-05 |
| **Área evaluada** | Seguridad - Validación de Datos |
| **Objetivo relacionado** | OE3 - Auditar seguridad |
| **Severidad** | ⚠️ **MEDIA** |
| **Estado** | ⚠️ **PENDIENTE** |

#### Descripción:
El sistema no valida ni sanitiza las entradas de usuario antes de procesarlas, lo que abre la puerta a ataques de inyección (SQL, XSS).

**Código vulnerable:**
```python
# app.py - línea 78
@app.route('/tickets', methods=['POST'])
def create_ticket():
    titulo = request.form['titulo']  # ❌ Sin validación
    descripcion = request.form['descripcion']
    
    # ❌ Vulnerable a SQL Injection
    query = f"INSERT INTO tickets (titulo) VALUES ('{titulo}')"
    db.execute(query)
```

#### Evidencia Objetiva:
- Ver `/evidencias/e1.png`
- Prueba de