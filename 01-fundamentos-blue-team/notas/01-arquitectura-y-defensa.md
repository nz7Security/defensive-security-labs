# Arquitectura y defensa

## Idea central

Una defensa efectiva comienza por comprender el entorno que se quiere defender.

La arquitectura de seguridad funciona como un mapa: permite entender qué existe, cómo se relacionan los componentes, qué procesos dependen de ellos y qué estado de protección necesita alcanzar la organización.

## Qué estamos defendiendo realmente

El objetivo no es proteger servidores, cuentas o aplicaciones como elementos aislados.

La defensa busca preservar la capacidad de la organización para seguir funcionando, lo que incluye:

- procesos de negocio;
- servicios críticos;
- datos;
- identidades;
- aplicaciones;
- infraestructura;
- continuidad operativa;
- capacidad de respuesta y recuperación;
- confianza de clientes y usuarios.

Un incidente técnico puede afectar mucho más que el activo donde se originó.

## La arquitectura como mapa del Blue Team

Conocer la arquitectura permite determinar:

- qué proteger;
- dónde observar;
- qué eventos son relevantes;
- qué componentes sostienen procesos críticos;
- qué priorizar;
- qué capacidades defensivas deberían existir.

La arquitectura puede incluir:

- redes;
- infraestructura;
- aplicaciones;
- endpoints;
- servicios cloud;
- identidades;
- bases de datos;
- integraciones;
- terceros.

Sin esta visión, la defensa puede volverse reactiva y depender excesivamente de alertas aisladas.

## Conocer antes de detectar

Antes de pensar en herramientas o detecciones hay que comprender:

- qué activos existen;
- cómo funcionan;
- cómo se relacionan;
- quién los utiliza;
- de qué procesos dependen;
- cuáles son realmente importantes.

La visibilidad tiene valor cuando existe contexto para interpretar lo observado.

## Activos críticos y joyas de la corona

No todos los activos tienen la misma criticidad.

Las **joyas de la corona** son aquellos activos, datos o procesos cuya afectación produciría un impacto especialmente importante para la organización.

Identificarlos permite concentrar recursos defensivos donde más valor generan.

## Priorización

Si todo se trata como crítico, la priorización pierde sentido.

La criticidad del activo y su relación con el negocio ayudan a decidir:

- qué proteger primero;
- dónde aumentar visibilidad;
- qué alerta merece atención inmediata;
- dónde invertir recursos;
- qué riesgo requiere tratamiento prioritario.

## El tiempo como dimensión defensiva

El impacto de un incidente también depende del tiempo.

Algunos tiempos relevantes son:

- tiempo hasta detectar;
- tiempo hasta analizar;
- ventana disponible para actuar;
- tiempo de indisponibilidad;
- tiempo necesario para recuperar la operación.

Una defensa técnicamente correcta puede fallar si la organización tarda demasiado en detectar o responder.

## Arquitectura aplicada a una implementación

Una aplicación no debería analizarse solamente como software a instalar.

También debe entenderse:

- cómo se separan sus componentes;
- dónde se ubican frontend, backend y base de datos;
- qué comunicaciones necesita;
- qué segmentos atraviesa;
- qué controles existen entre capas;
- qué puntos requieren monitoreo.

Esto permite evaluar cómo se integra la aplicación dentro de la postura de seguridad general.

## Modelo mental

```text
Negocio
  ↓
Procesos críticos
  ↓
Activos y dependencias
  ↓
Arquitectura
  ↓
Visibilidad
  ↓
Detección
  ↓
Respuesta
  ↓
Continuidad y resiliencia
```

## Puntos clave

- No se puede defender correctamente lo que no se conoce.
- La arquitectura aporta contexto a la defensa.
- Los sistemas importan por los procesos que sostienen.
- No todos los activos tienen la misma criticidad.
- La visibilidad sin priorización genera ruido.
- El tiempo de detección y respuesta también condiciona el impacto.
