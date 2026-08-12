# Defensive Security Labs

Portfolio técnico personal construido durante mi recorrido de especialización en **Defensive Security, Security Operations & Blue Teaming**.

Este repositorio documenta de forma progresiva mi aprendizaje en seguridad defensiva, combinando **fundamentos técnicos, análisis, razonamiento defensivo y laboratorios prácticos**.

El objetivo no es reproducir material académico, sino transformar los conceptos y ejercicios trabajados durante la especialización en **documentación técnica reutilizable y evidencia práctica de aprendizaje**, orientada a roles como **SOC Analyst, Blue Team y Security Operations**.

---

## Objetivo

A lo largo del recorrido busco desarrollar y documentar capacidades para:

- comprender arquitecturas y entornos desde una perspectiva defensiva;
- identificar activos, procesos y servicios relevantes para la operación;
- analizar superficies de ataque y exposición;
- interpretar amenazas y riesgos;
- priorizar controles según contexto, criticidad e impacto;
- trabajar con detección, respuesta y resiliencia;
- analizar incidentes y evidencia;
- documentar laboratorios y decisiones técnicas;
- diferenciar análisis técnico de comunicación ejecutiva;
- desarrollar criterio profesional para operaciones de seguridad.

El foco está puesto no solamente en **qué control aplicar**, sino en entender **qué estamos defendiendo, contra qué, por qué y con qué prioridad**.

---

## Ruta de aprendizaje

| Módulo | Tema | Estado |
|---|---|---|
| 01 | [Fundamentos de Blue Team](./01-fundamentos-blue-team/) | 🟢 Completado |
| 02 | [Atacar para Defender](./02-atacar-para-defender/) | ⚪ Pendiente |
| 03 | [Security Operations (SOC)](./03-security-operations-soc/) | ⚪ Pendiente |
| 04 | [Security Operations Engineering & IA](./04-security-operations-engineering-ia/) | ⚪ Pendiente |
| 05 | [Incident Response](./05-incident-response/) | ⚪ Pendiente |
| 06 | [Cloud Security Operations](./06-cloud-security-operations/) | ⚪ Pendiente |
| 07 | [Threat Intelligence & Threat Hunting](./07-threat-intelligence-threat-hunting/) | ⚪ Pendiente |
| 08 | [Malware Analysis](./08-malware-analysis/) | ⚪ Pendiente |

La progresión general del aprendizaje sigue esta lógica:

```text
Fundamentos de Blue Team
        ↓
Comprensión del atacante
        ↓
Security Operations
        ↓
Automatización e ingeniería
        ↓
Incident Response
        ↓
Cloud Security
        ↓
Threat Intelligence / Threat Hunting
        ↓
Malware Analysis
```

---

## Estructura del repositorio

Cada módulo utiliza la misma convención:

```text
modulo/
├── README.md
├── conceptos-clave.md
├── notas/
└── labs/
```

### `README.md`

Contexto, alcance, temas principales y navegación del módulo.

### `conceptos-clave.md`

Síntesis técnica de los conceptos más importantes del módulo para utilizar como referencia.

### `notas/`

Documentación desarrollada de los distintos temas, con énfasis en modelos mentales, relaciones entre conceptos y aplicabilidad profesional.

### `labs/`

Aplicación práctica mediante análisis de escenarios, identificación de riesgos, priorización defensiva y elaboración de documentación técnica o ejecutiva.

---

## Metodología de trabajo

Los laboratorios siguen un proceso de análisis progresivo:

```text
Contexto
   ↓
Procesos y activos relevantes
   ↓
Arquitectura y dependencias
   ↓
Superficie de ataque
   ↓
Amenazas y riesgos
   ↓
Madurez defensiva
   ↓
Objetivos de defensa
   ↓
Priorización
   ↓
Recomendaciones
   ↓
Documentación
```

Durante los análisis se distingue entre:

- **Hechos:** información proporcionada por el escenario.
- **Inferencias:** conclusiones razonables derivadas de los hechos.
- **Recomendaciones:** decisiones o controles propuestos a partir del análisis.

Esto permite mantener trazabilidad entre el contexto observado y las decisiones defensivas, evitando presentar supuestos como hechos.

---

## Criterio del portfolio

El repositorio prioriza:

- documentación técnica clara;
- terminología habitual de la industria;
- comprensión del contexto antes de aplicar controles;
- razonamiento defensivo;
- relación entre tecnología y negocio;
- priorización basada en criticidad y riesgo;
- detección y respuesta;
- resiliencia;
- laboratorios documentados;
- justificación de decisiones;
- separación entre análisis técnico y comunicación ejecutiva.

Más que mostrar una colección de herramientas, el objetivo es reflejar progresivamente **cómo analizo un entorno, qué considero importante y cómo justifico una decisión defensiva**.

---

## Seguridad del repositorio

Este repositorio es público.

Por ese motivo no se publican:

- credenciales;
- tokens;
- claves;
- información sensible;
- datos reales de clientes;
- evidencia privada;
- secretos de infraestructura;
- muestras peligrosas.

Los escenarios y laboratorios publicados están orientados exclusivamente al aprendizaje y la documentación de prácticas de seguridad defensiva.
