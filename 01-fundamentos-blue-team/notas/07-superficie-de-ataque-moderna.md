# Superficie de ataque moderna

## Idea central

La superficie de ataque moderna está distribuida entre múltiples tecnologías, identidades, servicios y relaciones.

Ya no puede analizarse solamente desde la red corporativa.

## Componentes habituales

La superficie puede incluir:

- infraestructura on-premise;
- cloud;
- SaaS;
- endpoints;
- identidades;
- terceros;
- integraciones;
- aplicaciones.

Cada componente presenta una lógica de exposición distinta.

## On-premise

Suele ofrecer mayor control directo sobre infraestructura, pero requiere administración, mantenimiento y visibilidad propios.

## Cloud

Aporta elasticidad y rapidez, pero también introduce:

- exposición configurable;
- recursos dinámicos;
- fuerte dependencia de identidad;
- riesgo de errores de configuración.

## SaaS

Reduce parte de la administración técnica directa, pero aumenta la dependencia de:

- cuentas;
- permisos;
- sesiones;
- configuraciones;
- seguridad del proveedor.

## Identidad como punto crítico

En entornos distribuidos, una identidad puede habilitar acceso a varios servicios.

Por eso resultan especialmente relevantes:

- autenticación;
- sesiones;
- permisos;
- privilegios;
- accesos distribuidos;
- abuso de cuentas legítimas.

Una cuenta válida comprometida puede permitir avanzar sin explotar una vulnerabilidad técnica tradicional.

## Endpoint como puerta de entrada

Los endpoints continúan siendo una superficie importante por su relación con:

- phishing;
- ejecución de archivos;
- ejecución de scripts;
- persistencia local;
- robo de credenciales;
- acceso a otros sistemas.

## Amenazas sigilosas

Algunas amenazas intentan mezclarse con actividad legítima utilizando:

- credenciales válidas;
- herramientas legítimas;
- Living off the Land;
- persistencia discreta;
- movimiento lateral silencioso.

Esto obliga a analizar comportamiento y contexto, no solamente firmas o archivos maliciosos.

## Perspectiva del atacante

Donde la organización puede ver productividad e integración, un atacante puede ver:

- rutas;
- permisos reutilizables;
- identidades;
- privilegios;
- servicios conectados;
- integraciones;
- proveedores;
- herramientas desatendidas.

Analizar el entorno desde ambas perspectivas ayuda a descubrir exposiciones que pueden pasar desapercibidas.

## Modelo mental

```text
Superficie de ataque
│
├── Red
├── Cloud
├── SaaS
├── Endpoints
├── Identidades
├── Aplicaciones
├── Terceros
└── Integraciones
```

Para cada capa conviene analizar:

1. qué activos existen;
2. quién puede acceder;
3. qué privilegios posee;
4. qué exposición tiene;
5. qué visibilidad existe;
6. qué comportamiento sería anómalo;
7. cómo respondería la organización.

## Puntos clave

- La superficie moderna es distribuida.
- Las identidades atraviesan múltiples servicios.
- Los endpoints siguen siendo una puerta frecuente de entrada.
- Las herramientas legítimas también pueden ser abusadas.
- La complejidad operativa puede favorecer al atacante.
- La perspectiva adversaria ayuda a identificar rutas de ataque.
