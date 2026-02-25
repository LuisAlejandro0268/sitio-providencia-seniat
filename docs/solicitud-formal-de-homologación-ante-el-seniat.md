---
id: homologacion-conexstudios-seniat
sidebar_position: 2
title: Solicitud Formal de Homologación ante el SENIAT
---


## Sistema de Gestión Académica con Módulo de Facturación Fiscal  
### CONEXSTUDIOS  
### Ante el Servicio Nacional Integrado de Administración Aduanera y Tributaria (SENIAT)

---

# INTRODUCCIÓN

El presente Dossier Oficial tiene como finalidad documentar de manera integral el cumplimiento técnico, legal y operativo del Sistema de Gestión Académica con Módulo de Facturación Fiscal desarrollado por CONEXSTUDIOS, conforme a la Providencia Administrativa SNAT/2024/000121.

Este documento demuestra que el sistema:

- Garantiza inalterabilidad absoluta de los registros fiscales.
- Implementa integridad criptográfica verificable.
- Permite trazabilidad total de cada operación.
- Cumple estándares de seguridad informática.
- Genera libros fiscales conforme a normativa del IVA.
- Incorpora protocolo formal de contingencia.
- Permite fiscalización directa por parte del SENIAT.

---

# CAPÍTULO I  
## IDENTIFICACIÓN DEL PROVEEDOR

- Razón Social: CONEXSTUDIOS
- RIF: [Indicar]
- Domicilio Fiscal: [Indicar]
- Representante Legal: [Indicar]
- Objeto Social: Desarrollo de Software y Sistemas Informáticos

La empresa se encuentra solvente en materia de IVA e ISLR y sin sanciones fiscales pendientes.

---

# CAPÍTULO II  
# CUMPLIMIENTO ARTÍCULO POR ARTÍCULO (0 AL 13)

---

## ARTÍCULO 0 – Disposiciones Generales

El sistema ha sido diseñado con enfoque prioritario en control fiscal, garantizando supervisión, auditoría y verificación por parte del SENIAT.

---

## ARTÍCULO 1 – Objeto

El módulo fiscal permite emisión de:

- Facturas
- Notas de Crédito
- Notas de Débito

Con todos los datos exigidos por la normativa del IVA.

---

## ARTÍCULO 2 – Sujetos Obligados

CONEXSTUDIOS solicita autorización formal como proveedor de sistema informático de facturación.

---

## ARTÍCULO 3 – Principios del Sistema

Se garantiza:

- Integridad
- Inalterabilidad
- Seguridad
- Trazabilidad
- Conservación
- Accesibilidad

---

### ESPECIFICACIÓN DEL HASH CRIPTOGRÁFICO (Art. 3 y 7)

El sistema implementa:

- Algoritmo SHA-256
- Encadenamiento hash entre facturas consecutivas

Modelo conceptual:

HASH_N = SHA256(
  NumeroFactura +
  FechaHora +
  RIFCliente +
  Total +
  HASH_N-1
)

Cada factura depende criptográficamente de la anterior.

El hash:
- Se almacena en campo ineditable.
- Se imprime en PDF.
- Se incluye en código QR.
- Es verificable en auditoría.

---

## ARTÍCULO 4 – Diseño Técnico

- Separación lógica entre base académica y base fiscal.
- Restricciones SQL.
- Triggers de bloqueo.
- Prohibición de edición posterior.
- Documentación de arquitectura.

---

## ARTÍCULO 5 – Emisión y Contingencia

### Emisión Ordinaria

Factura incluye:
- Número consecutivo automático.
- Fecha y hora exacta.
- RIF.
- Razón social.
- Base imponible.
- IVA discriminado.
- Total.
- Hash SHA-256.

---

### PROTOCOLO DE CONTINGENCIA

En caso de:
- Falla eléctrica.
- Caída de internet.
- Caída del servidor.

Procedimiento:

1. Uso de facturas pre-impresas autorizadas.
2. Numeración física previamente controlada.
3. Registro manual provisional.
4. Carga obligatoria posterior en el sistema.
5. Marcado como "Factura Emitida en Contingencia".
6. Registro de fecha real y fecha de carga.
7. Prevención de duplicación.

Existe Manual Formal de Contingencia documentado.

---

## ARTÍCULO 6 – Numeración

- Automática.
- Correlativa.
- No editable.
- Sin reinicio.
- Anulaciones registradas sin eliminación.

---

## ARTÍCULO 7 – Seguridad Informática

- HTTPS obligatorio.
- Encriptación de contraseñas.
- Control de sesiones.
- Bloqueo por intentos fallidos.
- Registro de accesos.
- Protección contra inyección SQL.
- Firewalls.
- Registro de acciones administrativas.

---

## ARTÍCULO 8 – Respaldo y Conservación

- Backup diario incremental.
- Backup semanal completo.
- Backup mensual histórico.
- Almacenamiento externo.
- Procedimiento documentado de restauración.
- Retención conforme Código Orgánico Tributario.

---

## ARTÍCULO 9 – Fiscalización y Libros Fiscales

El sistema permite:

- Generación inmediata de reportes.
- Exportación estructurada.
- Entorno de pruebas para auditoría.

---

### LIBRO DE VENTAS AUTOMÁTICO

Generación mensual automática con:

- Número de factura.
- Fecha.
- RIF cliente.
- Base imponible.
- IVA débito fiscal.
- Total por alícuota.

Formatos disponibles:

- TXT estructurado conforme normativa IVA.
- Excel (.xlsx).
- CSV.

El TXT respeta:
- Separadores oficiales.
- Orden de columnas normativo.
- Compatibilidad con sistemas del SENIAT.

Cada generación queda registrada en log.

---

### LIBRO DE COMPRAS (si aplica)

- Facturas recibidas.
- RIF proveedor.
- Crédito fiscal.
- Totales mensuales.

---

## ARTÍCULO 10 – Prohibiciones

El sistema no permite:

- Contabilidad paralela.
- Bases ocultas.
- Eliminación física de registros.
- Edición posterior.
- Reset de numeración.
- Módulos ocultos.

Declaración jurada incluida en anexos.

---

## ARTÍCULO 11 – Procedimiento de Solicitud

Se consignan:

- Escrito formal.
- Manual técnico.
- Manual de usuario.
- Arquitectura documentada.
- Modelo entidad-relación.
- Política de seguridad.
- Procedimiento de respaldo.
- Declaración jurada.
- Solvencia fiscal.

---

## ARTÍCULO 12 – Evaluación Técnica

Se garantiza:

- Ambiente de pruebas disponible.
- Validación de hash.
- Validación de libros TXT.
- Demostración de contingencia.
- Revisión de logs.
- Acceso para auditoría.

---

## ARTÍCULO 13 – Revocatoria

Se implementa:

- Control formal de versiones.
- Registro de cambios.
- Comité interno de cumplimiento.
- Auditoría semestral.
- Notificación de actualizaciones.

---

# CAPÍTULO III  
## ESTRUCTURA DE BASE DE DATOS FISCAL

Incluye:

- Tabla de Facturas.
- Tabla de Notas.
- Tabla de Usuarios.
- Tabla de Auditoría ineditable.
- Campo Hash.
- Campo Hash Anterior.
- Registro IP.
- Timestamp exacto.

---

# CAPÍTULO IV  
## CONTROL INTERNO

CONEXSTUDIOS implementa:

1. Comité de Cumplimiento Fiscal.
2. Auditoría técnica previa a solicitud.
3. Control de versiones firmado digitalmente.
4. Registro de incidencias.
5. Plan de contingencia tecnológica.
6. Contrato que prohíbe manipulación del sistema.

---

# DECLARACIÓN FINAL

CONEXSTUDIOS declara que el sistema cumple íntegramente con la Providencia SNAT/2024/000121, garantizando integridad, inalterabilidad, seguridad y trazabilidad total de la información fiscal.

---

