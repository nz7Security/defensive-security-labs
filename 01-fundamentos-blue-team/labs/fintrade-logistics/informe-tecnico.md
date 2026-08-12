# Informe técnico — Fintrade Logistics

> Escenario de laboratorio sobre una organización ficticia.

## 1. Contexto y alcance

Fintrade Logistics es una organización regional con operaciones en varios países y una fuerte dependencia de servicios digitales para coordinar entregas, proveedores, facturación y seguimiento de órdenes.

El entorno combina infraestructura y servicios cloud, Microsoft 365, un ERP accesible desde la red interna, un portal web para clientes y proveedores, accesos remotos, endpoints corporativos distribuidos y soporte IT parcialmente tercerizado.

Este informe responde tres preguntas:

- qué estamos defendiendo realmente;
- qué objetivos debería tener el Blue Team;
- qué debilidades de madurez aparecen con mayor claridad.

El análisis utiliza únicamente la información disponible en el escenario. Algunas dependencias técnicas y de negocio no están completamente especificadas, por lo que no se presentan como hechos relaciones que todavía deberían relevarse.

---

## 2. ¿Qué estamos defendiendo realmente?

El objetivo de la defensa no es proteger tecnología de forma aislada, sino preservar la capacidad de Fintrade para continuar operando de forma confiable.

### 2.1 Procesos de alta relevancia operativa

El escenario muestra una fuerte dependencia digital para sostener:

- coordinación de entregas;
- gestión de proveedores;
- facturación;
- seguimiento de órdenes.

Estos procesos son prioritarios para el análisis defensivo porque forman parte directa de la operación descrita.

Su criticidad formal y el impacto relativo de una interrupción deberían validarse mediante un análisis de impacto de negocio más profundo.

### 2.2 Identidades, accesos y privilegios

Las identidades son una dependencia transversal porque habilitan el acceso a aplicaciones, datos e infraestructura.

El escenario establece que:

- existen distintos niveles de privilegio;
- la revisión periódica de accesos es escasa;
- existe acceso remoto para personal administrativo y técnico;
- se observaron inicios de sesión fuera de horario utilizando cuentas válidas.

Además, dos campañas de phishing afectaron a usuarios administrativos.

Estos hechos justifican priorizar la gestión de identidades, accesos y privilegios. Sin embargo, los inicios de sesión fuera de horario no demuestran por sí solos que las cuentas hayan sido comprometidas, y el escenario tampoco permite afirmar que las campañas de phishing hayan sido dirigidas específicamente a esos usuarios.

### 2.3 Aplicaciones y servicios

La operación incluye varias plataformas relevantes:

- Microsoft 365 para correo, colaboración y almacenamiento;
- ERP accesible desde la red interna;
- portal web para clientes y proveedores;
- infraestructura y servicios cloud.

El escenario no especifica qué proceso depende exactamente de cada componente ni todas las relaciones entre aplicaciones, por lo que esas dependencias deberían relevarse antes de construir un mapa definitivo.

### 2.4 Datos operativos y de negocio

La organización depende de información relacionada con órdenes, entregas, proveedores, facturación y clientes.

La defensa debe contemplar:

- confidencialidad;
- integridad;
- disponibilidad.

La importancia relativa de cada dimensión depende del proceso y del impacto de negocio asociado, información que no está completamente disponible en el escenario.

### 2.5 Endpoints, acceso remoto y terceros

Los endpoints corporativos están distribuidos entre oficina y trabajo remoto y existe acceso remoto para personal administrativo y técnico.

Parte del soporte IT está tercerizado.

Estos elementos amplían el entorno defensivo y agregan relaciones de confianza que deben relevarse en términos de accesos, permisos, responsabilidades y alcance.

La existencia de soporte tercerizado no implica por sí misma una vulnerabilidad.

### 2.6 Arquitectura cloud y cadena de despliegue

El entorno técnico disponible muestra principalmente una cadena de aplicación y cloud con capacidades de identidad, desarrollo, repositorios, seguridad de código, pipelines, registro de contenedores, Kubernetes, políticas, gestión de secretos, base de datos, observabilidad, infraestructura como código y acceso de usuarios.

Esta vista no representa toda la arquitectura organizacional. Debe complementarse con Microsoft 365, ERP, endpoints, acceso remoto y soporte IT tercerizado.

La exposición accidental de un recurso cloud durante un cambio operativo hace relevante revisar cómo se validan configuraciones y cambios antes y después de su aplicación.

### Síntesis

Fintrade no está defendiendo solamente cuentas, servidores o aplicaciones. Está defendiendo la capacidad de sostener procesos de alta relevancia operativa mediante servicios disponibles, datos confiables, accesos controlados y dependencias conocidas.

---

## 3. Superficie de exposición y señales relevantes

Los hechos observados permiten identificar áreas que requieren atención defensiva.

### 3.1 Phishing

**Hecho:** dos campañas de phishing afectaron a usuarios administrativos.

**Limitación:** no puede afirmarse que hayan sido campañas específicamente dirigidas ni que Microsoft 365 haya sido necesariamente el canal utilizado.

**Implicación defensiva:** conviene revisar controles de correo, señales de identidad y capacidad de detección y respuesta frente a phishing.

### 3.2 Actividad con cuentas válidas

**Hecho:** se observaron múltiples inicios de sesión fuera de horario utilizando cuentas válidas.

**Inferencia:** es una señal que merece investigación, pero no prueba por sí sola actividad maliciosa ni compromiso de las cuentas.

**Implicación defensiva:** resulta relevante mejorar el contexto sobre autenticaciones, privilegios y patrones de acceso.

### 3.3 Acceso remoto y endpoints

**Hecho:** existen endpoints distribuidos y accesos remotos para personal administrativo y técnico.

**Inferencia:** estos elementos amplían la superficie que debe monitorearse.

El escenario no identifica una vulnerabilidad concreta en los mecanismos de acceso remoto ni en los endpoints.

### 3.4 Portal externo

**Hecho:** existe un portal para clientes y proveedores.

**Inferencia:** por su exposición a usuarios externos, debe incluirse dentro del relevamiento de superficie de ataque.

No se aportan evidencias de una vulnerabilidad específica en el portal.

### 3.5 Cambios y configuraciones cloud

**Hecho:** un recurso cloud quedó expuesto accidentalmente durante un cambio operativo.

**Inferencia:** el proceso de cambios puede introducir exposición si las configuraciones no se validan adecuadamente.

El escenario no permite determinar qué control específico falló.

### 3.6 Relación con terceros

**Hecho:** parte del soporte IT está tercerizado.

**Inferencia:** existe una relación de confianza que debe incorporarse al análisis de accesos y responsabilidades.

No existe evidencia suficiente para afirmar que el tercero sea inseguro.

---

## 4. Objetivos del Blue Team

### 4.1 Obtener claridad sobre el entorno

El primer objetivo debería ser consolidar una visión del entorno que permita relacionar:

- activos;
- procesos de negocio;
- dependencias;
- responsables;
- nivel de relevancia para la operación.

La ausencia de un inventario consolidado y de ownership completo sobre activos críticos limita la capacidad de priorizar correctamente la defensa.

### 4.2 Fortalecer identidades, privilegios y accesos

El Blue Team debería reducir el riesgo asociado al uso indebido o eventual compromiso de cuentas válidas.

Esto requiere revisar y mejorar, donde corresponda:

- privilegios;
- revisiones periódicas de acceso;
- accesos remotos;
- accesos de terceros;
- mecanismos de autenticación;
- supervisión de comportamientos anómalos.

La recomendación es validar y reforzar los mecanismos de autenticación donde corresponda, no asumir que toda la autenticación existente es débil.

### 4.3 Mejorar visibilidad, detección y priorización

El objetivo no debería ser generar más alertas, sino aumentar su utilidad operativa.

El Blue Team debería reducir ruido y aportar contexto suficiente para priorizar eventos según:

- relevancia del activo;
- identidad involucrada;
- proceso de negocio afectado;
- impacto potencial.

### 4.4 Validar y fortalecer la capacidad de respuesta

La organización debería contar con una capacidad repetible para:

- validar incidentes;
- tomar decisiones;
- contener impacto;
- escalar cuando corresponda;
- recuperar la operación;
- documentar lo ocurrido.

El escenario no permite afirmar que Incident Response sea inexistente. Por eso debe tratarse como una capacidad a evaluar y fortalecer, no como una carencia confirmada.

### 4.5 Fortalecer cambios y configuraciones cloud

El Blue Team debería mejorar la capacidad de prevenir, validar y detectar configuraciones inseguras introducidas durante cambios operativos.

La exposición accidental del recurso cloud justifica revisar controles antes y después de los cambios.

### 4.6 Validar periódicamente la cobertura defensiva

La organización debería incorporar mecanismos que permitan comprobar si sus controles, detecciones y procesos de respuesta funcionan frente a técnicas de ataque relevantes.

Las prácticas Purple Team pueden utilizarse como una etapa posterior de madurez para identificar brechas de cobertura y alimentar ciclos de mejora.

---

## 5. Debilidades de madurez identificadas

### 5.1 Gestión de activos insuficiente

La organización presenta crecimiento desordenado de activos y no dispone de un inventario consolidado.

Esto reduce la claridad sobre el entorno y dificulta relacionar activos, dependencias y prioridades defensivas.

### 5.2 Ownership incompleto

No todos los activos críticos tienen un responsable claramente asignado.

Esto puede dificultar decisiones de priorización, gestión de riesgos, escalamiento y respuesta.

### 5.3 Revisión de accesos insuficiente

La revisión periódica de accesos es escasa a pesar de existir distintos niveles de privilegio.

Esta debilidad adquiere mayor relevancia frente a los antecedentes de phishing sobre usuarios administrativos y la actividad fuera de horario utilizando cuentas válidas.

### 5.4 Baja calidad operativa de las alertas

Las alertas de seguridad existen, pero generan mucho ruido y poca priorización.

Esto muestra una brecha entre disponer de señales y convertirlas en información suficientemente contextualizada para tomar decisiones defensivas.

### 5.5 Gestión de cambios y configuraciones cloud mejorable

La exposición accidental de un recurso cloud durante un cambio operativo demuestra que una modificación produjo exposición.

El escenario no permite determinar qué control falló, pero sí justifica revisar la capacidad de prevenir, validar y detectar este tipo de situaciones.

### 5.6 Falta de validación periódica de cobertura

No existen ejercicios formales de Purple Team ni validaciones periódicas de cobertura.

Esto dificulta comprobar de forma sistemática si los controles y detecciones funcionan como se espera frente a técnicas relevantes.

### 5.7 Falta de una visión consolidada de madurez

La organización considera que está protegida porque cuenta con varias herramientas, pero no posee una visión clara de su madurez defensiva.

Esto evidencia una diferencia entre disponer de tecnología de seguridad y desarrollar capacidades defensivas integradas, priorizadas y validadas.

---

## 6. Prioridades técnicas derivadas

A partir del análisis, las prioridades técnicas iniciales son:

1. consolidar inventario, dependencias y ownership;
2. revisar identidades, accesos y privilegios;
3. mejorar la calidad y priorización de alertas;
4. fortalecer validaciones de cambios y configuraciones cloud;
5. validar y fortalecer la capacidad de Incident Response.

Estas prioridades no implican que las demás capacidades carezcan de importancia. Representan un orden inicial basado en los hechos y limitaciones disponibles.

---

## 7. Limitaciones del análisis

El escenario no permite confirmar:

- la criticidad formal de cada proceso;
- todas las dependencias entre aplicaciones y procesos;
- si los inicios de sesión fuera de horario fueron maliciosos;
- si alguna cuenta fue comprometida;
- si el phishing utilizó Microsoft 365;
- si existen debilidades generales de autenticación;
- si el soporte tercerizado presenta controles insuficientes;
- si Incident Response está ausente;
- qué control específico permitió la exposición cloud.

Estas limitaciones deben considerarse antes de convertir inferencias en hallazgos definitivos.

---

## 8. Conclusión técnica

Fintrade dispone de múltiples servicios y herramientas, pero las principales debilidades observadas se relacionan con el conocimiento del entorno, la gestión de accesos, la calidad de las alertas, la validación de cambios cloud y la medición de capacidades defensivas.

El desafío inicial no es incorporar más tecnología de forma aislada, sino transformar activos, señales y controles existentes en una capacidad defensiva coherente.

Para ello, el Blue Team debería priorizar claridad sobre activos y dependencias, gestión de identidades y privilegios, detección con contexto, respuesta estructurada, seguridad de cambios cloud y validación periódica de cobertura.

Esto permitiría evolucionar hacia una defensa más priorizada, medible y orientada a sostener la operación.
