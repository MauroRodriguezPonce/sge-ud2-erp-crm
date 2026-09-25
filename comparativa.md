* Datos:
    -Propietario: MauroRodriguezPonce
    -Empresa: Caso 08 — Taller mecánico "AutoExpress"

## 2. Licencias y modelos (Libre, Código Abierto y Propietario)
* **Software Libre (FSF):** Garantiza las cuatro libertades esenciales definidas por la Free Software Foundation (ejecutar, estudiar, modificar y redistribuir). El foco está en la libertad ética del usuario.
* **Código Abierto (OSI):** Concepto impulsado por la Open Source Initiative enfocado en las ventajas prácticas del modelo de desarrollo (acceso al código fuente, revisión por pares). Todo software libre suele ser de código abierto, pero no a la inversa estricta según los criterios de gobernanza.
* **Software Propietario:** El código fuente está restringido y pertenece a una empresa. Los usuarios adquieren una licencia de uso con limitaciones estrictas de modificación, estudio y redistribución.
* **¿Por qué "libre" no significa "gratuito"?** El software libre permite cobrar por su distribución, soporte técnico, personalización o servicios asociados. La libertad se refiere al control sobre el programa, no a su coste económico directo.
* **Edición Community vs. Enterprise:** 
  * *Community:* Gratuita, código accesible (habitualmente bajo licencias como AGPL o LGPL), orientada a PYMEs o comunidades, con soporte de la comunidad y limitaciones en funcionalidades avanzadas o soporte oficial garantizado.
  * *Enterprise:* De pago (por suscripción), incluye soporte técnico oficial SLA, herramientas avanzadas de gestión, mayor seguridad y módulos certificados para grandes empresas.

----

## 3. Fichas técnicas de productos

### 3.1. ERP Libre: Odoo Community
* **Licencia exacta:** LGPL v3
* **Versión vigente:** 17.0 / 18.0 (Consultado: Septiembre 2026)
* **Lenguaje del servidor:** Python
* **SGBD compatibles:** PostgreSQL
* **Modalidad:** Instalación local (On-Premise) / Nube (Odoo.sh / SaaS)
* **Módulos principales:** Ventas, Inventario, Fabricación (Obrador), Facturación, Sitio Web/E-commerce.
* **Requisitos:** Python 3.10+, PostgreSQL 13+, Servidor Linux (Ubuntu recomendado), mínimo 2 vCPU y 4 GB RAM.
* **Fuente oficial:** [Odoo Community](https://www.odoo.com/) (Consultado el 24/09/2026).

### 3.2. ERP Propietario: Microsoft Dynamics 365 Business Central
* **Licencia exacta:** Propietaria (SaaS / Suscripción por usuario)
* **Versión vigente:** Dynamics 365 Business Central 2026 Release Wave 1 (Consultado: Septiembre 2026)
* **Lenguaje del servidor:** AL / .NET
* **SGBD compatibles:** Azure SQL Database (Gestionado en la nube de Microsoft)
* **Modalidad:** Nube (Cloud SaaS) principalmente, con opciones híbridas.
* **Módulos principales:** Gestión financiera, Ventas, Compras, Gestión de inventario, Fabricación básica, Gestión de proyectos.
* **Requisitos:** Navegador web moderno, conexión a internet estable; suscripción a Microsoft 365 recomendada.
* **Fuente oficial:** [Microsoft Dynamics 365](https://dynamics.microsoft.com/) (Consultado el 24/09/2026).

### 3.3. CRM Libre: SuiteCRM
* **Licencia exacta:** AGPL v3
* **Versión vigente:** SuiteCRM 8.x (Consultado: Septiembre 2026)
* **Lenguaje del servidor:** PHP
* **SGBD compatibles:** MySQL, MariaDB, PostgreSQL
* **Modalidad:** Instalación local (On-Premise) / Nube propia (Hosting VPS)
* **Módulos principales:** Gestión de cuentas y contactos, Leads, Oportunidades, Casos de soporte, Campañas de marketing.
* **Requisitos:** PHP 8.1/8.2, servidor web Apache/Nginx, MySQL 8.0 o MariaDB 10.5+, mínimo 2 GB RAM.
* **Fuente oficial:** [SuiteCRM](https://suitecrm.com/) (Consultado el 24/09/2026).

### 3.4. CRM Propietario: Salesforce Sales Cloud
* **Licencia exacta:** Propietaria (SaaS multi-tenant por usuario/mes)
* **Versión vigente:** Salesforce Summer/Autumn 2026 Release (Consultado: Septiembre 2026)
* **Lenguaje del servidor:** Apex (Plataforma propietaria Force.com)
* **SGBD compatibles:** Base de datos propietaria gestionada en la nube (Oracle/Cloud nativa)
* **Modalidad:** Nube (SaaS puro)
* **Módulos principales:** Gestión de oportunidades, Leads, Cuentas, Automatización de marketing (Cloud), Informes y paneles analíticos.
* **Requisitos:** Dispositivo con navegador web y conexión a internet.
* **Fuente oficial:** [Salesforce](https://www.salesforce.com/) (Consultado el 24/09/2026).

----

## 4. Fe de erratas del tema 2

1. **Dato en el tema:** El documento PDF afirma en la sección de CRM que **SuiteCRM** (clasificado como CRM libre) es compatible con MySQL, MariaDB y **SQL Server**[cite: 1].
   * **Realidad actual:** SuiteCRM no ofrece soporte oficial para Microsoft SQL Server. Está diseñado y optimizado estrictamente para motores de bases de datos de código abierto como MySQL y MariaDB. Atribuirle compatibilidad con SQL Server es un error técnico de arquitectura.
   * **Fuente:** Documentación oficial de requisitos y matriz de compatibilidad de SuiteCRM (`docs.suitecrm.com`).

2. **Dato en el tema:** En la categorización de herramientas, se presenta a **Fat Free CRM** como el referente principal de los CRM libres de código abierto más valorados y activos[cite: 1], infravalorando el peso de **SuiteCRM**.
   * **Realidad actual:** Aunque Fat Free CRM es de código abierto (bajo licencia MIT), **SuiteCRM** (bajo AGPL-3.0) es el estándar de la industria y la alternativa libre orientada a entornos empresariales reales más robusta, con soporte completo para flujos corporativos avanzados frente a proyectos más minimalistas.
   * **Fuente:** Repositorios oficiales en GitHub de SuiteCRM y comparativas del sector del software de gestión libre..

---

## 5. Matriz de decisión y recomendación (Empresa 1: Panadería artesanal)

1. Contexto

Empresa: Caso 08 — Taller mecánico “AutoExpress”
Empleados: 10

AutoExpress es un taller mecánico multimarca que también vende recambios mediante una tienda online propia. Actualmente, las citas se gestionan con una agenda de papel y la tienda online funciona con un programa independiente que no está integrado con el taller. Esto provoca problemas de coordinación y puede llegar a producir ventas online de recambios que ya se han utilizado en una reparación.

Palabra del día: Compañero

El objetivo de la solución tecnológica es integrar la gestión del taller, las citas, el inventario y la tienda online, reduciendo errores de stock y facilitando el trabajo de los empleados.


2. Soluciones candidatas

Solución 1: ERP taller + tienda integrada

Solución 2: Gestión de taller + integración con la tienda

Solución 3: ERP generalista + APIs


3. Criterios de decisión

La matriz utiliza 7 criterios y sus pesos suman el 100 %:

              Criterio                        Peso

- Integración taller + tienda online          25 %

- Gestión de inventario en tiempo real        20 %

- Coste total de implantación y uso           15 %

- Facilidad de uso para 10 empleados          15 %

- Soporte y mantenimiento                     10 %

- Integración con proveedores                  5 %

- Migración y escalabilidad futura            10 %

Total                                        100 %

La puntuación utilizada es de 1 a 5, donde 1 representa una valoración baja para ese criterio y 5 una valoración alta.

4. Resultados de la matriz

El total ponderado se calcula multiplicando cada puntuación por su peso y sumando los resultados. Por ejemplo, para la Solución 1:

(5×25 + 5×20 + 3×15 + 4×15 + 4×10 + 4×5 + 4×10) / 100 = 4,45


5. Justificación de las puntuaciones y recomendación

- Solución 1 — ERP taller + tienda integrada

Integración taller + tienda online — 5/5: integra las operaciones del taller y el comercio electrónico, por lo que permite mantener conectados los procesos y reducir el riesgo de vender un recambio que ya se ha utilizado.

Gestión de inventario en tiempo real — 5/5: centraliza el inventario y permite actualizar el stock utilizado en reparaciones y vendido en la tienda online.

Coste total — 3/5: una solución integrada puede requerir una inversión inicial mayor en licencias, implantación, configuración y formación.

Facilidad de uso — 4/5: disponer de una plataforma integrada reduce la necesidad de cambiar continuamente entre aplicaciones.

Soporte y mantenimiento — 4/5: el soporte puede centralizarse en un proveedor, aunque esto también aumenta la dependencia de dicho proveedor.

Integración con proveedores — 4/5: puede centralizar las compras y facilitar futuras conexiones con proveedores.

Migración y escalabilidad futura — 4/5: puede crecer junto con AutoExpress y centralizar más procesos conforme aumenten las necesidades.


- Solución 2 — Gestión de taller + integración con la tienda

Integración taller + tienda online — 4/5: permite conectar ambos sistemas, aunque depende de que el conector o integración funcione correctamente.

Gestión de inventario en tiempo real — 5/5: puede sincronizar el stock del taller y de la tienda si la integración está correctamente configurada.

Coste total — 4/5: puede permitir conservar parte de las herramientas actuales y reducir la inversión inicial.

Facilidad de uso — 4/5: los empleados pueden trabajar con herramientas conocidas, aunque existen varios sistemas que deben mantenerse coordinados.

Soporte y mantenimiento — 4/5: el soporte se reparte entre el sistema principal y la integración con la tienda.

Integración con proveedores — 4/5: puede ampliarse mediante módulos o integraciones específicas.

Migración y escalabilidad futura — 4/5: su estructura modular permite añadir funcionalidades posteriormente.


- Solución 3 — ERP generalista + APIs

Integración taller + tienda online — 3/5: puede conseguirse mediante APIs, pero requiere más configuración y trabajo técnico.

Gestión de inventario en tiempo real — 4/5: es posible centralizar el inventario, aunque puede depender de módulos y desarrollos adicionales.

Coste total — 4/5: el ERP puede tener un coste competitivo, pero las APIs y conectores pueden aumentar el gasto de implantación y mantenimiento.

Facilidad de uso — 3/5: una configuración más técnica puede aumentar la complejidad para una empresa pequeña de 10 empleados.

Soporte y mantenimiento — 4/5: el ERP puede ofrecer soporte consolidado, pero las integraciones mediante APIs también necesitan mantenimiento.

Integración con proveedores — 3/5: puede realizarse, pero probablemente requiere configurar integraciones específicas.

Migración y escalabilidad futura — 5/5: las APIs ofrecen flexibilidad para conectar nuevos sistemas y ampliar la solución en el futuro.


- Recomendación

Según la matriz de decisión, la Solución 1 obtiene 4,45/5, frente a 4,20/5 de la Solución 2 y 3,65/5 de la Solución 3. La puntuación se debe principalmente a que responde directamente al problema central de AutoExpress: conectar el taller, el inventario y la tienda online.

Antes de implantarla, AutoExpress debería comprobar los siguientes riesgos:

Coste total: no hay que valorar únicamente el precio de la licencia. Se deben tener en cuenta implantación, configuración, formación, mantenimiento, actualizaciones y posibles conectores.

Dependencia del proveedor: una solución integrada puede dificultar el cambio a otro proveedor en el futuro. Es importante comprobar que los datos puedan exportarse y revisar las condiciones de salida.

Soporte: conviene definir los canales de soporte, tiempos de respuesta y condiciones del servicio, especialmente cuando una incidencia pueda afectar simultáneamente al taller y a la tienda online.

Migración futura: se debe comprobar que clientes, vehículos, citas, recambios, stock y ventas puedan exportarse en formatos reutilizables para facilitar una futura migración.

Por tanto, la decisión debe basarse en la matriz y, antes de contratar, en la comprobación real del coste, las condiciones de soporte, la portabilidad de los datos y las posibilidades de integración.

