# Libro de Códigos (Codebook) y Dataset Completo

## ¿Qué es un Libro de Códigos?

El **libro de códigos** (codebook) es un documento que define de manera exhaustiva cada código utilizado en un análisis cualitativo. Sirve como:

- ✅ **Diccionario oficial** del sistema de categorización
- ✅ **Herramienta de validación** para asegurar consistencia en codificación
- ✅ **Registro de decisiones metodológicas** (audit trail)
- ✅ **Referencia para inter-codificación** (múltiples investigadores)
- ✅ **Documentación para replicabilidad**

## Estructura de un Libro de Códigos Profesional

Un libro de códigos completo contiene **7 componentes obligatorios** por cada código:

### 1. Nombre del Código (Code Name)
- **Etiqueta corta** y descriptiva
- Preferencia: MAYÚSCULAS o CamelCase para distinguir
- Ejemplo: `ADAPTACION_UNIVERSITARIA`, `SentimientoIncompetencia`

### 2. Definición Operacional (Operational Definition)
- **Qué significa exactamente** el código
- Definición clara y no ambigua
- Ejemplo:
  ```
  ADAPTACION_UNIVERSITARIA: Proceso de ajuste del estudiante a las
  exigencias académicas, sociales y culturales del contexto universitario,
  que implica aprendizaje de códigos institucionales y reorganización de
  identidad académica.
  ```

### 3. Criterios de Inclusión (When to Use)
- **Qué fragmentos deben codificarse** con este código
- Lista de características que debe tener un fragmento
- Ejemplo:
  ```
  Incluir fragmentos que mencionen:
  - Experiencia de desorientación en primeros meses
  - Desconocimiento de procedimientos institucionales
  - Comparación con otros estudiantes más adaptados
  - Aprendizaje de "reglas no escritas" universitarias
  ```

### 4. Criterios de Exclusión (When NOT to Use)
- **Qué NO incluir** (evita confusión con códigos similares)
- Ejemplo:
  ```
  NO incluir:
  - Dificultades académicas por déficit de conocimientos previos
    → usar código BRECHA_ACADEMICA
  - Problemas de adaptación social general
    → usar código INTEGRACION_SOCIAL
  ```

### 5. Ejemplos Representativos (Typical Exemplars)
- **2-3 fragmentos reales** del corpus codificados con este código
- Muestran diversidad de manifestaciones
- Ejemplo:
  ```
  Ejemplo 1 (Entrevista 3, líneas 45-48):
  "Los primeros meses estuve completamente perdido. No sabía dónde
  inscribir ramos, cómo funcionaban los horarios, nada. Todos los
  demás parecían saber perfectamente qué hacer."

  Ejemplo 2 (Entrevista 7, líneas 112-115):
  "Había códigos que yo no manejaba. Por ejemplo, ir a las 'ayudantías',
  hablar con profes en horario de oficina... nadie me había enseñado
  eso, y me di cuenta tarde que era importante."
  ```

### 6. Relación con Otros Códigos (Related Codes)
- **Códigos relacionados** (jerárquicamente o temáticamente)
- Ejemplo:
  ```
  Código padre: EXPERIENCIA_PRIMERA_GENERACION_UNIVERSITARIA
  Códigos hermanos: FALTA_REDES_APOYO, ESTRATEGIAS_SUPERVIVENCIA
  Códigos hijos: DESORIENTACION_INICIAL, APRENDIZAJE_CODIGOS_CULTURALES
  ```

### 7. Notas Metodológicas (Memos)
- **Reflexiones** del investigador durante codificación
- Decisiones tomadas, dudas resueltas
- Ejemplo:
  ```
  MEMO: Inicialmente este código se llamaba "Desorientación", pero
  se expandió a "Adaptación Universitaria" tras detectar que la
  mayoría de fragmentos no solo reflejaban confusión, sino proceso
  activo de aprendizaje de códigos institucionales. Esta reconceptualización
  ocurrió en ronda 2 de codificación, tras analizar 8 entrevistas.
  ```

---

## Dataset Completo: 25+ Columnas de Metadata

Además del libro de códigos, se genera un **dataset** (archivo Excel/CSV) con cada segmento codificado como fila y columnas de metadata:

### Columnas Obligatorias

| Columna | Descripción | Ejemplo |
|---------|-------------|---------|
| `ID_Segmento` | Identificador único | SEG_0001 |
| `Fuente` | Documento de origen | Entrevista_03_Juan.docx |
| `Tipo_Fuente` | Categoría de fuente | Entrevista semiestructurada |
| `Participante_ID` | Anonimizado | P003 |
| `Fecha_Recoleccion` | Cuándo se obtuvo dato | 2024-03-15 |
| `Pagina` | Ubicación en documento | p. 4 |
| `Lineas` | Rango de líneas | 45-48 |
| `Parrafo` | Número de párrafo | 7 |
| `Texto_Original` | Fragmento textual completo | "Los primeros meses estuve..." |
| `Codigo_Primario` | Código principal asignado | ADAPTACION_UNIVERSITARIA |
| `Codigo_Secundario` | Código adicional (si aplica) | DESORIENTACION_INICIAL |
| `Categoria_Axial` | Categoría de nivel superior | EXPERIENCIA_PRIMERA_GENERACION |
| `Tema_Central` | Tema selectivo (si aplica) | CAPITAL_CULTURAL_DESIGUALDAD |
| `Codificador` | Quién codificó | Investigador_A |
| `Fecha_Codificacion` | Cuándo se codificó | 2024-04-10 |
| `Ronda_Codificacion` | Ronda de codificación | Ronda_2 |
| `Confianza` | Nivel de certeza (1-5) | 4 |
| `Notas` | Comentarios del codificador | "Ejemplo paradigmático de adaptación" |

### Columnas de Metadata Adicionales (según tipo de estudio)

**Para estudios con entrevistas**:
- `Rol_Participante` (estudiante, docente, directivo)
- `Genero`
- `Edad`
- `Nivel_Educativo`
- `Anos_Experiencia`

**Para análisis de discurso**:
- `Autor_Discurso`
- `Fecha_Discurso`
- `Contexto_Politico`
- `Audiencia_Target`
- `Medio_Publicacion`

**Para análisis de documentos**:
- `Tipo_Documento` (acta, informe, noticia)
- `Institucion_Emisora`
- `Año_Publicacion`

---

## Estadísticas Generadas Automáticamente

### 1. Frecuencia de Códigos

| Código | Frecuencia | % del Total | N° Fuentes |
|--------|------------|-------------|------------|
| ADAPTACION_UNIVERSITARIA | 47 | 12.3% | 14 |
| BRECHA_ACADEMICA | 38 | 9.9% | 12 |
| FALTA_REDES_APOYO | 35 | 9.1% | 11 |
| ESTRATEGIAS_SUPERVIVENCIA | 29 | 7.6% | 10 |
| **TOTAL** | **382** | **100%** | **15** |

### 2. Matriz de Coocurrencia

Muestra qué códigos aparecen juntos en mismos fragmentos:

|  | ADAPTACION | BRECHA | FALTA_REDES | ESTRATEGIAS |
|--|------------|--------|-------------|-------------|
| **ADAPTACION** | - | 18 | 22 | 15 |
| **BRECHA** | 18 | - | 14 | 8 |
| **FALTA_REDES** | 22 | 14 | - | 19 |
| **ESTRATEGIAS** | 15 | 8 | 19 | - |

**Interpretación**: ADAPTACION y FALTA_REDES coocurren en 22 fragmentos → relación fuerte.

### 3. Curva de Saturación

Gráfico que muestra códigos nuevos por fuente analizada:

```
Fuente 1:  28 códigos nuevos ███████████████████████████████
Fuente 2:  19 códigos nuevos ████████████████████
Fuente 5:  12 códigos nuevos ████████████
Fuente 8:   7 códigos nuevos ███████
Fuente 10:  3 códigos nuevos ███
Fuente 12:  1 código nuevo   █
Fuente 13:  0 códigos nuevos  ✅ SATURACIÓN ALCANZADA
```

### 4. Densidad de Categorías

| Categoría Axial | N° Códigos Hijos | N° Fragmentos | Densidad |
|-----------------|------------------|---------------|----------|
| EXPERIENCIA_1GEN | 6 | 89 | Alta ✅ |
| TRANSICION_EDUCATIVA | 4 | 54 | Media |
| APOYO_INSTITUCIONAL | 3 | 21 | Baja ⚠️ |

**Densidad** = Fragmentos / Códigos. Alta densidad = categoría bien fundamentada.

### 5. Distribución por Fuente

| Participante | N° Segmentos Codificados | Códigos Únicos |
|--------------|-------------------------|----------------|
| P001 | 32 | 18 |
| P003 | 28 | 21 |
| P007 | 41 | 23 |

Permite identificar si algunos participantes son más "ricos" en información.

---

## Formatos de Exportación

### 1. Excel (.xlsx) - Recomendado para Análisis Manual

**Estructura de múltiples hojas**:
- Hoja 1: **Dataset Completo** (todas las columnas)
- Hoja 2: **Libro de Códigos** (definiciones, ejemplos)
- Hoja 3: **Frecuencias** (tabla de conteo)
- Hoja 4: **Matriz Coocurrencia**
- Hoja 5: **Curva Saturación**
- Hoja 6: **Metadata del Proyecto**

### 2. CSV UTF-8 - Para Análisis Estadístico (R, Python, SPSS)

Archivo plano con dataset completo, ideal para:
- Análisis cuantitativo de datos cualitativos (frequency analysis)
- Visualizaciones en R (ggplot2, wordcloud)
- Machine learning sobre códigos

### 3. JSON - Para Análisis Programático

```json
{
  "proyecto": {
    "titulo": "Adaptación Universitaria Primera Generación",
    "investigador": "Dr. X",
    "fecha_inicio": "2024-01-01",
    "fecha_fin": "2024-06-30"
  },
  "codebook": [
    {
      "codigo": "ADAPTACION_UNIVERSITARIA",
      "definicion": "Proceso de ajuste...",
      "inclusion": ["Desorientación", "Aprendizaje códigos"],
      "exclusion": ["Déficit académico"],
      "ejemplos": [
        {"fuente": "E03", "lineas": "45-48", "texto": "Los primeros meses..."}
      ],
      "frecuencia": 47,
      "porcentaje": 12.3
    }
  ],
  "dataset": [
    {
      "id": "SEG_0001",
      "fuente": "E03",
      "participante": "P003",
      "texto": "Los primeros meses...",
      "codigo_primario": "ADAPTACION_UNIVERSITARIA",
      "categoria_axial": "EXPERIENCIA_1GEN"
    }
  ]
}
```

### 4. HTML Interactivo - Para Presentación

Reporte web con:
- Tabla de códigos navegable
- Filtros interactivos (por código, fuente, fecha)
- Visualizaciones (gráficos de frecuencia, red de coocurrencias)
- Búsqueda de texto en fragmentos

### 5. REFI-QDA XML - Para Software Cualitativo (NVivo, MAXQDA, Atlas.ti)

Formato estandarizado para importar códigos y dataset a software de análisis cualitativo.

Estructura XML compatible con:
- NVivo (import as .qda)
- MAXQDA (import project)
- Atlas.ti (import coding scheme)

---

## Tabla de Trazabilidad de Fuentes

Documenta exactitud de evidencia para prevenir plagio y asegurar rigor:

| Afirmación en Texto | Código | Fuente | Ubicación Exacta | Texto Original |
|---------------------|--------|--------|------------------|----------------|
| "Estudiantes de primera generación experimentan desorientación inicial" | ADAPTACION_UNIVERSITARIA | Entrevista 3 | p. 4, líneas 45-48 | "Los primeros meses estuve completamente perdido..." |
| "Falta de redes de apoyo familiar universitarias" | FALTA_REDES_APOYO | Entrevista 7 | p. 6, líneas 112-115 | "Nadie en mi familia había ido a la U..." |

Esta tabla permite **validar cada afirmación analítica** con evidencia textual precisa.

---

## Proceso de Generación Automática (por el Skill)

Cuando el usuario proporciona datos cualitativos, el Skill ejecuta:

### Paso 1: Lectura y Codificación Automática
1. Lee cada fuente (PDF, DOCX, TXT)
2. Segmenta en unidades de análisis (párrafos, turnos de habla)
3. Aplica codificación abierta → axial → selectiva
4. Detecta saturación teórica

### Paso 2: Generación de Libro de Códigos
Para cada código identificado, genera automáticamente:
- Nombre descriptivo
- Definición operacional
- Criterios inclusión/exclusión
- 2-3 ejemplos representativos
- Relaciones jerárquicas
- Memos metodológicos

### Paso 3: Construcción de Dataset
Crea archivo con 25+ columnas:
- Metadata de fuente
- Ubicación precisa (página, líneas)
- Texto original
- Códigos asignados (primario, secundario, axial, selectivo)
- Metadata del proceso (codificador, fecha, confianza)

### Paso 4: Generación de Estadísticas
Calcula automáticamente:
- Frecuencias absolutas y relativas
- Matriz de coocurrencia
- Curva de saturación
- Densidad de categorías
- Distribución por fuente

### Paso 5: Exportación Multi-Formato
Genera simultáneamente:
- Excel con múltiples hojas
- CSV UTF-8
- JSON estructurado
- HTML interactivo
- REFI-QDA XML

### Paso 6: Tabla de Trazabilidad
Crea registro completo de evidencia para cada afirmación analítica.

---

## Validación de Calidad del Libro de Códigos

### Checklist de Calidad ✅

**Criterios obligatorios**:
- [ ] Cada código tiene definición operacional clara
- [ ] Criterios de inclusión/exclusión están especificados
- [ ] Al menos 2 ejemplos por código
- [ ] Relaciones jerárquicas documentadas
- [ ] Memos metodológicos justifican decisiones
- [ ] Frecuencias calculadas
- [ ] Matriz de coocurrencia generada
- [ ] Saturación teórica verificada
- [ ] Dataset exportado en múltiples formatos
- [ ] Tabla de trazabilidad completa

**Criterios avanzados** (recomendados):
- [ ] Acuerdo inter-codificador calculado (Kappa ≥ 0.70)
- [ ] Member checking realizado
- [ ] Audit trail documentado
- [ ] Codificación por pares en muestra

---

## Ejemplo de Libro de Códigos Completo (Fragmento)

```markdown
# LIBRO DE CÓDIGOS: Experiencia Universitaria Primera Generación

**Proyecto**: Adaptación Universitaria en Estudiantes de Primera Generación
**Investigador**: Dr. Juan Pérez
**Periodo**: Enero-Junio 2024
**N° Entrevistas**: 15
**N° Segmentos Codificados**: 382
**N° Códigos Totales**: 28
**Saturación Alcanzada**: Entrevista 13

---

## CÓDIGO 1: ADAPTACION_UNIVERSITARIA

**Definición Operacional**:
Proceso de ajuste del estudiante a exigencias académicas, sociales y
culturales del contexto universitario, que implica aprendizaje de códigos
institucionales y reorganización de identidad académica.

**Criterios de Inclusión**:
- Experiencia de desorientación en primeros meses
- Desconocimiento de procedimientos institucionales
- Comparación con otros estudiantes más adaptados
- Aprendizaje de "reglas no escritas" universitarias

**Criterios de Exclusión**:
- Dificultades académicas por déficit de conocimientos → usar BRECHA_ACADEMICA
- Problemas sociales generales → usar INTEGRACION_SOCIAL

**Ejemplos Representativos**:

Ejemplo 1 (Entrevista 3, p. 4, líneas 45-48):
"Los primeros meses estuve completamente perdido. No sabía dónde inscribir
ramos, cómo funcionaban los horarios, nada. Todos los demás parecían saber
perfectamente qué hacer."

Ejemplo 2 (Entrevista 7, p. 6, líneas 112-115):
"Había códigos que yo no manejaba. Por ejemplo, ir a las 'ayudantías',
hablar con profes en horario de oficina... nadie me había enseñado eso,
y me di cuenta tarde que era importante."

**Relación con Otros Códigos**:
- Código padre: EXPERIENCIA_PRIMERA_GENERACION
- Códigos hermanos: FALTA_REDES_APOYO, BRECHA_ACADEMICA
- Códigos hijos: DESORIENTACION_INICIAL, APRENDIZAJE_CODIGOS_CULTURALES

**Estadísticas**:
- Frecuencia: 47 segmentos (12.3% del total)
- Presente en: 14 de 15 entrevistas (93.3%)
- Coocurrencia principal: FALTA_REDES_APOYO (22 veces)

**Memos**:
[2024-04-10] Inicialmente llamado "Desorientación". Expandido tras detectar
proceso activo de aprendizaje, no solo confusión pasiva. Cambio reflejado
desde Ronda 2.

---

## CÓDIGO 2: FALTA_REDES_APOYO

[... continúa con mismo formato para cada código ...]
```

---

## Referencias Clave

- Saldaña, J. (2021). *The coding manual for qualitative researchers* (4ª ed.). Sage.
- MacQueen, K. M., McLellan, E., Kay, K., & Milstein, B. (1998). Codebook development for team-based qualitative analysis. *CAM Journal*, 10(2), 31-36.
- Campbell, J. L., Quincy, C., Osserman, J., & Pedersen, O. K. (2013). Coding in-depth semistructured interviews: Problems of unitization and intercoder reliability and agreement. *Sociological Methods & Research*, 42(3), 294-320.

---

**Uso en el Skill**: Este módulo se activa automáticamente cuando el usuario proporciona datos cualitativos. El sistema genera libro de códigos profesional + dataset completo con 25+ columnas + estadísticas + exportación multi-formato (Excel, CSV, JSON, HTML, REFI-QDA).
