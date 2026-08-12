# Amenazas, vulnerabilidades y riesgo

## Idea central

Una estrategia defensiva necesita distinguir claramente entre amenaza, vulnerabilidad, impacto y riesgo.

Confundir estos conceptos dificulta la priorización.

## Amenaza

Una amenaza es un actor, condición o evento con capacidad de producir daño.

Las amenazas relevantes cambian según el contexto de la organización.

Un banco, una empresa de retail, una organización pública o una infraestructura crítica no necesariamente enfrentan los mismos actores ni las mismas motivaciones.

## Vulnerabilidad

Una vulnerabilidad es una debilidad o condición que una amenaza puede aprovechar.

Puede existir en:

- tecnología;
- configuración;
- arquitectura;
- procesos;
- personas;
- controles;
- permisos.

## Riesgo

Para priorizar riesgos es necesario considerar al menos dos dimensiones:

- **probabilidad de ocurrencia**;
- **impacto potencial**.

El riesgo debe analizarse dentro de un contexto concreto.

```text
Amenaza
   +
Vulnerabilidad
   +
Contexto
   ↓
Probabilidad e impacto
   ↓
Riesgo
```

## El contexto modifica el riesgo

Una misma vulnerabilidad puede tener consecuencias muy distintas dependiendo de:

- activo afectado;
- exposición;
- actor de amenaza;
- privilegios disponibles;
- dependencia del negocio;
- capacidad de detección y respuesta.

Por eso no conviene evaluar riesgos de manera aislada.

## Modelado de amenazas

Modelar amenazas ayuda a pensar:

- quién podría atacar;
- qué podría buscar;
- qué caminos tendría disponibles;
- qué debilidades podría aprovechar;
- qué activos serían atractivos;
- qué impacto podría generar.

La pregunta defensiva debería ser primero:

> ¿Qué amenaza o riesgo intento reducir?

y después:

> ¿Qué control o capacidad necesito?

## Alerta e incidente

No todo evento extraño es automáticamente un incidente.

Una señal debe ser:

1. recibida;
2. analizada;
3. contextualizada;
4. validada;
5. clasificada.

Una alerta es una señal que requiere análisis. Un incidente implica que existe una situación validada que necesita respuesta.

## Ejemplo simplificado

```text
Amenaza:
Atacante intenta acceder a una cuenta corporativa.

Vulnerabilidad:
Credenciales débiles o ausencia de un control adicional.

Activo:
Cuenta con acceso a información relevante.

Impacto:
Acceso no autorizado y posible expansión hacia otros servicios.

Riesgo:
Se prioriza considerando probabilidad, impacto y contexto.
```

## Puntos clave

- Amenaza y vulnerabilidad son conceptos diferentes.
- El riesgo depende del contexto.
- Probabilidad e impacto ayudan a priorizar.
- Modelar amenazas evita diseñar controles sin objetivo.
- Una alerta necesita análisis antes de considerarse incidente.
- La criticidad del activo modifica la prioridad del riesgo.
