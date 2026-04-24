# SAP-MM
Guía práctica de MM en SAP con ejemplos reales y casos de prueba
# SAP MRP - Guía práctica

## Objetivo

Explicar el funcionamiento del MRP en SAP a nivel funcional, incluyendo la generación de propuestas y su análisis.

## Flujo del proceso

1. Carga de demanda (forecast / necesidades independientes)
2. Ejecución del MRP (MD02 / MD01)
3. Generación de propuestas:

   * Órdenes previsionales
   * Solicitudes de pedido
4. Análisis en MD04
5. Conversión de propuestas

## Transacciones principales

* MD02: Ejecución de MRP individual
* MD01: Ejecución de MRP masiva
* MD04: Lista de stock/necesidades
* MD05: Lista MRP

## Tablas relevantes

* J_3AREQS: Forecast
* PLAF: Órdenes previsionales
* MDKP / MDTB: Documentos MRP
* MARC: Datos de planificación

## Escenarios de prueba

### Escenario 1: Material con stock suficiente

Resultado esperado: No se generan propuestas

### Escenario 2: Material sin stock

Resultado esperado: Se generan órdenes previsionales o solicitudes de pedido

### Escenario 3: Faltantes con lead time

Resultado esperado: Propuestas ajustadas a fecha de necesidad

### Escenario 4: Sustitutos

Resultado esperado: Consumo del material sustituto según configuración

## Análisis de resultados

Se valida:

* Fechas de las propuestas
* Cantidades generadas
* Tipo de aprovisionamiento

## Problemas comunes

* Datos maestros incorrectos (MARC, MRP type)
* Stock no considerado
* Forecast duplicado o incorrecto

## Próximos pasos

* Incluir capturas de MD04
* Agregar ejemplos reales
* Documentar excepciones MRP
