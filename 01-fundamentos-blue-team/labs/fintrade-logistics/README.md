# Fintrade Logistics — Evaluación defensiva inicial

> Estado: 🟢 Completado

## Objetivo

Analizar una organización ficticia desde una perspectiva defensiva para identificar qué debe protegerse, reconocer puntos de exposición, evaluar debilidades de madurez y proponer una postura inicial de Blue Team.

## Contexto organizacional

Fintrade Logistics es una organización regional con operaciones en varios países y una fuerte dependencia de servicios digitales para coordinar entregas, proveedores, facturación y seguimiento de órdenes.

El entorno contempla servicios cloud, Microsoft 365, un ERP interno, un portal para clientes y proveedores, acceso remoto, endpoints distribuidos, distintos niveles de privilegio y soporte IT parcialmente tercerizado.

También existen señales que requieren análisis defensivo: phishing sobre usuarios administrativos, actividad fuera de horario con cuentas válidas, una exposición accidental en cloud, inventario no consolidado, ownership incompleto y alertas con mucho ruido.

## Entregables

- [Análisis defensivo](./analisis-defensivo.md) — razonamiento completo, priorización y mapa defensivo.
- [Informe técnico](./informe-tecnico.md) — contexto, alcance, objetivos del Blue Team, debilidades de madurez y limitaciones.
- [Informe ejecutivo](./informe-ejecutivo.md) — cinco acciones iniciales, asimetría defensiva y decisión ejecutiva.

## Resultado

El análisis prioriza cinco líneas de trabajo:

1. consolidar inventario, dependencias y ownership;
2. revisar identidades, accesos y privilegios;
3. mejorar la calidad y priorización de alertas;
4. fortalecer la validación de cambios y configuraciones cloud;
5. validar y fortalecer Incident Response.

La gestión de identidades, accesos y privilegios se considera la acción con mejor asimetría inicial porque puede limitar el alcance de una eventual cuenta comprometida sin asumir que los eventos observados demuestran un compromiso real.
