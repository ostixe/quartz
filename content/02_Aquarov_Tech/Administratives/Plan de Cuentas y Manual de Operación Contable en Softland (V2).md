
**Empresa:** Aquarov Tech  
**Sector:** Robótica Submarina, Hardware y Servicios de Ingeniería  
**Sistema ERP / Contable Target:** Softland ERP  
**Estructura de Cuentas:** 8 Dígitos (`X.X.XX.XXX`)
**Archivo Importación:**  [[https://www.icloud.com/iclouddrive/0f7-LucxJj-2nSIjXpWJATLSw]]

---

## 1. INTRODUCCIÓN Y PRINCIPIOS DE DISEÑO

Este Plan de Cuentas ha sido estructurado para **Aquarov Tech** respondiendo a su modelo de negocio de robótica y tecnología submarina:
1. **Manufactura de Equipos Estándar y Repuestos:** Fabricación de ROVs y componentes (housings de cámaras, chasis, flotadores, tarjetas).
2. **Proyectos Especiales y Adaptaciones a Medida:** Ingeniería personalizada solicitada por clientes.
3. **Arriendo de Equipos (OpEx / Leasing):** Conversión de productos terminados en activos fijos generadores de renta.
4. **Comercio Internacional:** Importación frecuente de insumos y electrónica desde China y otros mercados.

### Principios de Trazabilidad Contable:
- **Cuentas por Cobrar Simplificadas:** Control unificado en `Clientes Nacionales` e `Clientes Internacionales` (los tipos de servicio o producto se identifican en la facturación y venta, no en la cuenta de clientes).
- **Control de Inventarios:** Trazabilidad entre Materia Prima (`1.1.03.001`), Subconjuntos Fabricados (`1.1.03.002`), Productos en Proceso (`1.1.03.003`) y Productos Terminados (`1.1.03.004`).
- **Carpetas de Importación:** Uso de la cuenta puente `1.1.03.010` para valorizar el *Landing Cost* de compras desde China.

---

## 2. HERRAMIENTAS DE COSTEO: CENTROS DE COSTOS vs. ÓRDENES DE TRABAJO (OT) / PROYECTOS

Para no saturar el plan de cuentas y saber **cuánto costó exactamente un proyecto específico** o **fabricar un equipo en serie**, se utilizan tres capas complementarias en Softland:

| Herramienta Contable | ¿Para qué sirve? | Ejemplo de Aplicación |
| :--- | :--- | :--- |
| **Centro de Costos (CC)** | Medir la gestión presupuestaria por **departamento** (visión macro). | Saber cuánto gastó el departamento de *Ingeniería (CC-100)* o *Producción (CC-200)* en un mes/año. |
| **Órdenes de Trabajo (OT) / Código de Proyecto** | Medir el costo y margen real de **un proyecto específico a medida**. | Saber exactamente cuánto costó el proyecto `"PRJ-2026-001: ROV de Lavado para Cliente X"`. |
| **Órdenes de Fabricación (OF) / Hoja de Costos** | Determinar el **costo unitario de producción** en serie. | Calcular el costo exacto de fabricar 5 unidades de `"Housing de Cámara ROV V2"`. |

### Dimensión Adicional de Imputación:
En Softland, cada gasto o consumo de materiales se registra con la combinación:
`Cuenta Contable` + `Centro de Costos` + `Código de Proyecto / OT`

---

## 3. ESTRUCTURA COMPLETA DEL PLAN DE CUENTAS (V2)

```text
1. ACTIVO
   1.1. ACTIVO CORRIENTE
        1.1.01. EFECTIVO Y EQUIVALENTES DE EFECTIVO
               1.1.01.001 Caja General
               1.1.01.010 Banco Nacional (CLP)
               1.1.01.020 Banco Moneda Extranjera (USD)
        1.1.02. CUENTAS POR COBRAR Y OTRAS CUENTAS POR COBRAR
               1.1.02.001 Clientes Nacionales
               1.1.02.002 Clientes Internacionales
               1.1.02.010 Documentos por Cobrar (Cheques / Facturas a Fecha)
               1.1.02.090 Estimación de Cuentas Incobrables (Deducción)
        1.1.03. INVENTARIOS / EXISTENCIAS (BODEGA PRINCIPAL)
               1.1.03.001 Materias Primas y Componentes Importados/Locales
               1.1.03.002 Subconjuntos y Partes Fabricadas (Housings, Chasis, Tarjetas)
               1.1.03.003 Productos en Proceso (WIP - Equipos/Proyectos en Curso)
               1.1.03.004 Productos Terminados (ROVs Listos para Venta)
               1.1.03.005 Repuestos y Accesorios para Venta
               1.1.03.010 Importaciones en Tránsito (Cuenta Puente China)
        1.1.04. IMPUESTOS Y ANTICIPOS
               1.1.04.001 IVA Crédito Fiscal
               1.1.04.002 Pagos Provisionales Mensuales (PPM)
               1.1.04.003 IVA Importaciones por Recuperar
               1.1.04.010 Anticipo a Proveedores Extranjeros
   1.2. ACTIVO NO CORRIENTE
        1.2.01. PROPIEDAD, PLANTA Y EQUIPO
               1.2.01.001 Flota de Equipos ROV en Arriendo
               1.2.01.002 Maquinaria, Herramental y Equipos de Taller/CNC
               1.2.01.003 Equipos de Cómputo, Desarrollo y Laboratorio
               1.2.01.004 Instrumentos de Medición y Pruebas Submarinas
        1.2.05. DEPRECIACIÓN ACUMULADA (DEDUCCIÓN)
               1.2.05.001 Depreciación Acumulada Flota en Arriendo
               1.2.05.002 Depreciación Acumulada Maquinaria y Equipos

2. PASIVO
   2.1. PASIVO CORRIENTE
        2.1.01. CUENTAS POR PAGAR
               2.1.01.001 Proveedores Nacionales
               2.1.01.002 Proveedores Extranjeros (USD - China / Otros)
               2.1.01.003 Facturas No Llegadas (Provisiones de Compras)
        2.1.02. IMPUESTOS Y RETENCIONES POR PAGAR
               2.1.02.001 IVA Débito Fiscal
               2.1.02.002 Retenciones Impuesto 2da Categoría (Honorarios)
               2.1.02.003 Impuesto a la Renta por Pagar
        2.1.03. OBLIGACIONES LABORALES Y OTRAS
               2.1.03.001 Sueldos por Pagar
               2.1.03.002 Leyes Sociales por Pagar (AFP, Isapre, Mutual)
               2.1.03.003 Depósitos en Garantía Recibidos (Arriendo Equipos)
   2.2. PASIVO NO CORRIENTE
        2.2.01. OBLIGACIONES FINANCIERAS
               2.2.01.001 Créditos Bancarios / Financiamiento Largo Plazo

3. PATRIMONIO
   3.1. CAPITAL Y RESERVAS
        3.1.01.001 Capital Pagado
        3.2.01.001 Utilidades / Pérdidas Acumuladas
        3.3.01.001 Resultado del Ejercicio

4. INGRESOS
   4.1. INGRESOS OPERACIONALES
        4.1.01.001 Venta de Equipos Estándar (ROVs)
        4.1.01.002 Venta de Repuestos, Componentes y Housings
        4.1.01.003 Ingresos por Proyectos Especiales y Adaptaciones
        4.1.01.004 Ingresos por Arriendo de Equipos (OpEx)
        4.1.01.005 Servicios de Mantenimiento, Integración y Postventa
   4.2. INGRESOS NO OPERACIONALES
        4.2.01.001 Ganancia por Diferencia de Cambio (USD)
        4.2.01.002 Intereses y Descuentos Obtenidos

5. COSTOS Y GASTOS
   5.1. COSTOS DIRECTOS DE PRODUCCIÓN Y PROYECTOS
        5.1.01.001 Costo de Ventas - Equipos y Repuestos Estándar
        5.1.01.002 Costo de Materiales - Proyectos y Adaptaciones a Medida
        5.1.01.003 Mano de Obra Directa (Taller / Ensamblaje)
        5.1.01.004 Costos Indirectos de Fabricación (CIF - Energía, Insumos Taller)
        5.1.01.005 Depreciación Flota de Equipos en Arriendo
        5.1.01.006 Costos Mantención y Repuestos Flota de Arriendo
   5.2. GASTOS OPERACIONALES (ASOCIADOS A CENTROS DE COSTO)
        5.2.01.001 Remuneraciones y Honorarios
        5.2.01.002 Arriendos de Inmuebles y Bodega
        5.2.01.003 Software, Licencias CAD/Simulación y Servidores
        5.2.01.004 Gastos de Viaje, Demostraciones y Terreno
        5.2.01.005 Marketing, Ferias y Publicidad
        5.2.01.006 Gastos de Importación No Capitalizables
        5.2.01.007 Servicios Básicos y Mantención Oficinas
        5.2.01.008 Pérdida por Diferencia de Cambio (USD)
```

---

## 4. TABLA DE CENTROS DE COSTO (SOFTLAND)

| Código CC | Nombre del Centro de Costo | Departamento / Área | Aplicación de Gastos General |
| :--- | :--- | :--- | :--- |
| **CC-100** | Ingeniería y Proyectos | R&D y Diseño | Software CAD/CAE, licenciamiento general, sueldos base de ingenieros. |
| **CC-200** | Producción y Taller | Manufactura | Herramientas generales, EPIS, arriendo taller, mantención CNC. |
| **CC-300** | Ventas y Comercial | Comercial | Publicidad, viajes comerciales, comisiones, participación en ferias. |
| **CC-400** | Flota Arriendos / Postventa | Servicios / Terreno | Logística de despacho arriendos, mantenimiento de equipos en terreno. |
| **CC-500** | Administración y General | Central / Finanzas | Remuneraciones administrativas, arriendo oficina general, legales. |

---

## 5. CÓMO COSTEAR PROYECTOS Y FABRICACIÓN EN SOFTLAND

### Caso A: Proyecto Específico a Medida (ej. "ROV de Lavado para Cliente X")
1. **Apertura del Proyecto / OT:** Se crea la Orden de Trabajo / Proyecto en Softland con el código `PRJ-2026-001` (Nombre: *ROV Lavado Cliente X*).
2. **Imputación de Materiales:** Cada salida de bodega para este desarrollo se imputa a la cuenta `1.1.03.003 Productos en Proceso (WIP)` + `CC-100` + **`Proyecto PRJ-2026-001`**.
3. **Imputación de Servicios o Compras Directas:** Facturas de mecanizado externo o sensores específicos se cargan directamente a `5.1.01.002 Costo Materiales Proyectos` + `CC-100` + **`Proyecto PRJ-2026-001`**.
4. **Horas Hombre:** Si registran partes de horas, el costo de hora del ingeniero se distribuye al código `PRJ-2026-001`.
5. **Cierre y Evaluación de Rentabilidad:** Al facturar el proyecto (`4.1.01.003`), el módulo de Proyectos emite el estado de resultado donde compara:
   $$	ext{Ingreso Facturado (PRJ-2026-001)} - 	ext{Costos Directos Acumulados (PRJ-2026-001)} = 	ext{Margen Bruto Real del Proyecto}$$

### Caso B: Fabricación de Equipos en Serie (ej. 5 Housings de Cámara V2)
1. **Lista de Materiales (BOM):** En el módulo de Inventario/Producción de Softland se define la receta estándar del *Housing de Cámara* (aluminio, tóricos, cristal templado, conectores, tornillería).
2. **Orden de Fabricación (OF):** Se abre una OF por 5 unidades.
3. **Consumo y Carga de Costos:**
   - Softland rebaja de la cuenta `1.1.03.001 Materias Primas` el valor exacto del BOM consumido.
   - Se adiciona la cuota de Mano de Obra Directa (`5.1.01.003`) y CIF (`5.1.01.004`).
4. **Valorización de Producto Terminado:**
   $$	ext{Costo Total OF} = 	ext{Materia Prima Consumida} + 	ext{Mano de Obra Directa} + 	ext{CIF}$$
   $$	ext{Costo Unitario} = rac{	ext{Costo Total OF}}{5 	ext{ unidades}}$$
5. **Ingreso a Bodega:** Cada Housing ingresa a la cuenta `1.1.03.002 Subconjuntos` con su costo unitario exacto calculado de manera automatizada.
