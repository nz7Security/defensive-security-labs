# Defensa activa y defensa pasiva

## Idea central

La seguridad defensiva puede combinar capacidades pasivas y activas.

No son enfoques excluyentes: una defensa madura necesita una base estable de controles y, progresivamente, capacidades que busquen amenazas de manera deliberada.

## Defensa pasiva

La defensa pasiva utiliza controles preparados para:

- proteger;
- observar;
- registrar;
- generar alertas;
- detectar condiciones previamente definidas.

Puede compararse con un sistema de vigilancia que permanece operativo y genera señales cuando ocurre algo relevante.

## Defensa activa

La defensa activa implica buscar intencionalmente señales de amenazas que podrían no haber producido una alerta explícita.

Se relaciona con actividades como **Threat Hunting**, donde se parte de una hipótesis o comportamiento esperado y se buscan rastros en el entorno.

```text
Hipótesis
   ↓
Búsqueda
   ↓
Evidencia
   ↓
Análisis
   ↓
Validación
```

## Defensa activa no significa 24/7

Que un equipo opere durante todo el día no lo convierte automáticamente en defensa activa.

La diferencia está en el enfoque:

- **pasiva:** procesa señales producidas por controles existentes;
- **activa:** busca deliberadamente comportamientos o rastros de una posible amenaza.

## La defensa activa necesita una base

Para buscar amenazas de forma útil se necesita previamente:

- conocimiento del entorno;
- inventario de activos;
- telemetría;
- controles básicos;
- procesos;
- capacidad de respuesta.

Sin esa base, la búsqueda puede transformarse en consultas aisladas sin contexto.

## Madurez incremental

Un error frecuente es intentar desarrollar todas las capacidades al mismo tiempo.

Una evolución más sostenible es:

```text
Conocer
   ↓
Ordenar
   ↓
Proteger
   ↓
Observar
   ↓
Detectar
   ↓
Buscar activamente
   ↓
Mejorar
```

## Entrenamiento defensivo

Las capacidades deben probarse antes de necesitarlas durante un incidente real.

Los ejercicios controlados permiten:

- descubrir fallas;
- validar procesos;
- observar reacciones;
- entrenar al equipo;
- mejorar resiliencia.

## Puntos clave

- Defensa activa y pasiva son complementarias.
- Defensa activa no equivale a operación 24/7.
- Threat Hunting es un ejemplo de búsqueda activa.
- La búsqueda necesita datos, contexto y capacidad de respuesta.
- La madurez defensiva debería crecer de forma incremental.
- Los controles y procesos deben probarse.
