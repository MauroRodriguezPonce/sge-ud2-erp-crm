* Datos:
    -Propietario: MauroRodriguezPonce
    -Empresa: Caso 08 — Taller mecánico "AutoExpress"
    -Fichas técnicas: 
    -Fe de erratas:
    -Matriz de decisión y recomendación:

## 2. Licencias y modelos (Libre, Código Abierto y Propietario)
* **Software Libre (FSF):** Garantiza las cuatro libertades esenciales definidas por la Free Software Foundation (ejecutar, estudiar, modificar y redistribuir). El foco está en la libertad ética del usuario.
* **Código Abierto (OSI):** Concepto impulsado por la Open Source Initiative enfocado en las ventajas prácticas del modelo de desarrollo (acceso al código fuente, revisión por pares). Todo software libre suele ser de código abierto, pero no a la inversa estricta según los criterios de gobernanza.
* **Software Propietario:** El código fuente está restringido y pertenece a una empresa. Los usuarios adquieren una licencia de uso con limitaciones estrictas de modificación, estudio y redistribución.
* **¿Por qué "libre" no significa "gratuito"?** El software libre permite cobrar por su distribución, soporte técnico, personalización o servicios asociados. La libertad se refiere al control sobre el programa, no a su coste económico directo.
* **Edición Community vs. Enterprise:** 
  * *Community:* Gratuita, código accesible (habitualmente bajo licencias como AGPL o LGPL), orientada a PYMEs o comunidades, con soporte de la comunidad y limitaciones en funcionalidades avanzadas o soporte oficial garantizado.
  * *Enterprise:* De pago (por suscripción), incluye soporte técnico oficial SLA, herramientas avanzadas de gestión, mayor seguridad y módulos certificados para grandes empresas.

---

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

---

## 4. Fe de erratas del tema 2
1. **Dato en el tema:** El PDF afirma que las versiones Community de Odoo carecen por completo de módulos de fabricación o que solo funcionan con bases de datos MySQL.
   * **Realidad actual:** Odoo Community incluye de serie el módulo de fabricación (MRP) adaptado a talleres y obradores, y su SGBD nativo y exclusivo es PostgreSQL.
   * **Fuente:** Documentación oficial de Odoo / Releases de Odoo 17 y 18.
2. **Dato en el tema:** Se indica que las soluciones CRM de código abierto no permiten automatizaciones de marketing complejas sin coste.
   * **Realidad actual:** Herramientas como SuiteCRM integran motores de campañas de marketing y flujos de trabajo automatizados avanzados sin necesidad de licencias comerciales adicionales.
   * **Fuente:** Repositorio oficial y matriz de características de SuiteCRM 8.

---

## 5. Matriz de decisión y recomendación (Empresa 1: Panadería artesanal)
* **Criterios evaluados:** Coste inicial/licenciamiento (peso 25), Control de obrador y compras de harina (peso 20), Integración E-commerce / Pedidos web (peso 20), Facilidad de uso para 18 empleados (peso 15), Requisitos de mantenimiento técnico (peso 10), Escalabilidad a 3 tiendas (peso 10). *Total pesos: 100*.
* **Opciones candidatas:** 
  1. Odoo Community (ERP libre)
  2. Microsoft Dynamics 365 (ERP propietario)
  3. Odoo Enterprise (ERP propietario open-core)

*(Nota: Los detalles numéricos y totales ponderados se recogen en el fichero `matriz_decision.csv`).*

### Justificación y Recomendación Final
Para una panadería artesanal con presupuesto muy ajustado, 18 empleados y 3 tiendas, la opción ganadora es **Odoo Community**. 
* **Justificación:** Al ser software libre sin costes de licencia por usuario, encaja perfectamente con un presupuesto ajustado. Su módulo de fabricación permite gestionar el obrador y las materias primas (harina), y cuenta con potentes capacidades nativas de comercio electrónico para los pedidos web.
* **Riesgos analizados:** 
  * *Coste total (TCO):* Bajo en licencias, pero requiere un partner o perfil técnico para la configuración inicial y mantenimiento en servidor propio o VPS.
  * *Dependencia del proveedor:* Baja, al ser código abierto se puede cambiar de proveedor de soporte técnico libremente.
  * *Soporte:* Basado en comunidad o contratando un servicio externo de mantenimiento.
  * *Migración futura:* Sencilla al disponer de acceso completo al código y a la base de datos PostgreSQL.