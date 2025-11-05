# Agente Científico IA - Custom Skill para Claude

Asistente especializado en investigación académica, metodología cualitativa, análisis crítico del discurso, y redacción científica con prevención de plagio integrada.

## 🎯 ¿Qué hace este Skill?

Transforma a Claude en un co-asesor de investigación experto que:

- ✅ **Analiza discursos** usando frameworks de Fairclough y Van Dijk
- ✅ **Codifica datos cualitativos** automáticamente (abierta → axial → selectiva)
- ✅ **Genera libros de códigos** profesionales con dataset completo
- ✅ **Escribe académicamente** con normas APA 7 estrictas
- ✅ **Previene plagio** con citación rigurosa (página precisa obligatoria)
- ✅ **Integra con MCP** para búsqueda y análisis potenciados
- ✅ **Valida coherencia** de tesis completas
- ✅ **Prepara defensas** identificando vulnerabilidades

## 📦 Instalación

### Opción A: Claude Desktop (Recomendada)

1. **Descargar** esta carpeta completa (`agente-cientifico-ia/`)

2. **Ubicar** en tu carpeta de Skills de Claude:
   ```
   Windows: %APPDATA%\Claude\skills\
   macOS: ~/Library/Application Support/Claude/skills/
   Linux: ~/.config/Claude/skills/
   ```

3. **Reiniciar** Claude Desktop

4. **Activar** el Skill desde el menú de Skills

### Opción B: Comprimir y Compartir

```bash
# Desde la carpeta padre
zip -r agente-cientifico-ia.zip agente-cientifico-ia/

# Compartir el ZIP
# Otros usuarios: descomprimir en carpeta de Skills de Claude
```

## 🔌 Integración con Parallel AI MCP (Opcional pero Recomendada)

Este Skill está optimizado para trabajar con **Parallel AI MCP servers**:

### 1. Instalar MCP Servers

Agregar a tu configuración de Claude (`claude_desktop_config.json`):

```json
{
  "mcpServers": {
    "parallel-search": {
      "command": "npx",
      "args": ["-y", "@parallel-ai/mcp-server-search"],
      "env": {
        "PARALLEL_API_KEY": "tu-api-key-aqui"
      }
    },
    "parallel-task": {
      "command": "npx",
      "args": ["-y", "@parallel-ai/mcp-server-task"],
      "env": {
        "PARALLEL_API_KEY": "tu-api-key-aqui"
      }
    }
  }
}
```

### 2. Obtener API Key de Parallel AI

1. Visita: https://www.parallel.ai/
2. Crea cuenta gratuita
3. Genera API key
4. Reemplaza `"tu-api-key-aqui"` en configuración

### 3. Beneficios con MCP

**SIN MCP:**
- ✅ Todas las capacidades funcionan perfectamente
- ⚠️ Requieres proporcionar PDFs manualmente

**CON MCP:**
- ✅ Búsqueda automática de literatura académica actualizada
- ✅ Validación de hipótesis con evidencia externa
- ✅ Investigación profunda paralela
- ✅ Identificación de gaps en marco teórico

**Nota**: El Skill detecta automáticamente si tienes MCP instalados y se adapta.

## 🚀 Uso Rápido

### Caso 1: Análisis Crítico del Discurso

```
Usuario: "Necesito analizar discursos presidenciales chilenos sobre
inmigración usando el modelo de Van Dijk"

[Sube 10 PDFs de discursos]

Claude (con Skill activado):
1. ✅ Valida que PDFs tengan paginación
2. 🔍 Aplica modelo sociocognitivo de Van Dijk
3. 📊 Codifica según categorías (tópicos, léxico, cuadrado ideológico)
4. 📝 Genera análisis multinivel completo
5. 💾 Exporta libro de códigos + dataset (.xlsx, .csv, .json)
6. ✅ Tabla de trazabilidad con cada evidencia y página exacta
```

### Caso 2: Codificación Cualitativa

```
Usuario: "Codifica estas 15 entrevistas usando análisis temático"

[Sube archivo con transcripciones]

Claude (con Skill):
1. 📖 Lee todas las entrevistas
2. 🏷️ Codificación abierta (genera códigos iniciales)
3. 🗂️ Codificación axial (agrupa en categorías)
4. 🎯 Codificación selectiva (identifica temas centrales)
5. 📊 Detecta saturación teórica
6. 💾 Genera libro de códigos completo
7. 📁 Dataset con 25+ columnas de metadata
8. 📈 Estadísticas de frecuencias y coocurrencias
```

### Caso 3: Escritura de Tesis

```
Usuario: "Escribe el marco teórico sobre gamificación en educación"

[Sube 8 artículos PDF]

Claude (con Skill):
1. ✅ Valida que PDFs tengan info bibliográfica completa
2. 📖 Lee y extrae conceptos clave de cada artículo
3. 🔗 Relaciona perspectivas de diferentes autores
4. ✍️ Redacta combinando múltiples fuentes por párrafo
5. 📄 Cita correctamente APA 7 con páginas exactas
6. 📋 Genera tabla de trazabilidad
7. ✅ Garantiza CERO plagio con parafraseo válido
```

### Caso 4: Preparación Defensa de Tesis

```
Usuario: "Prepárame para la defensa, identifica puntos débiles"

[Sube tesis completa 120 páginas]

Claude (con Skill + MCP):
1. 🔍 Meta-análisis de coherencia global
2. ⚠️ Identifica contradicciones internas
3. 🌐 (MCP) Busca literatura reciente contradictoria
4. 🎯 Predice preguntas probables del jurado
5. 💪 Genera respuestas preparadas con evidencia
6. 📊 Crea material de defensa (slides, FAQ, etc.)
```

## 📚 Estructura del Skill

```
agente-cientifico-ia/
├── SKILL.md                          # Instrucciones principales para Claude
├── README.md                         # Este archivo
├── references/                       # Documentación detallada
│   ├── 01_fairclough-acd-model.md
│   ├── 02_van-dijk-acd-model.md
│   ├── 03_codificacion-cualitativa.md
│   ├── 04_libro-codigos-dataset.md
│   ├── 05_apa-7-citacion-rigurosa.md
│   ├── 06_metodologia-cualitativa.md
│   ├── 07_plantilla-tesis.md
│   ├── 08_integracion-mcp.md
│   ├── 09_construccion-parrafos-academicos.md (NUEVO)
│   └── 10_hipotesis-y-recursos-retoricos.md (NUEVO)
├── examples/                         # Casos de uso completos
│   ├── caso-acd-fairclough-completo.md
│   ├── caso-acd-van-dijk-completo.md
│   ├── caso-generacion-libro-codigos.md
│   └── caso-tesis-completa-workflow.md
└── assets/
    └── templates/                    # Plantillas de exportación
        ├── template_codebook.xlsx
        ├── template_dataset.csv
        └── template_reporte_html.html
```

## ✨ Capacidades Principales

### 1. Análisis Crítico del Discurso

- **Fairclough**: Modelo tridimensional (texto + práctica discursiva + práctica social)
- **Van Dijk**: Modelo sociocognitivo (estructuras + cognición + contexto)
- Codificación automática según categorías ACD
- Identificación de estrategias discursivas e ideológicas
- Output con evidencia textual precisa (página + párrafo + línea)

### 2. Metodología Cualitativa

- Análisis temático (Braun & Clarke)
- Teoría fundamentada (Charmaz, Glaser & Strauss)
- Análisis de contenido (Krippendorff)
- Análisis narrativo (Riessman)
- Análisis fenomenológico interpretativo (Smith)
- Detección automática de saturación teórica

### 3. Sistema de Libro de Códigos

**Genera automáticamente:**

- ✅ Definición operacional de cada código
- ✅ Criterios de inclusión/exclusión
- ✅ Ejemplos representativos
- ✅ Jerarquía de categorías
- ✅ Dataset completo (25+ columnas metadata)
- ✅ Estadísticas de frecuencias
- ✅ Matriz de coocurrencia
- ✅ Curva de saturación
- ✅ Exportación múltiple (Excel, CSV, JSON, HTML, REFI-QDA)

### 4. Prevención de Plagio (Sistema Robusto)

**Regla Absoluta:** TODA cita incluye número de página exacto

- ✅ Citas directas con comillas + (Autor, año, p. XX)
- ✅ Citas indirectas con (Autor, año, p. XX)
- ✅ Validación automática de parafraseo
- ✅ Detección de similitud >70% sin cita
- ✅ Tabla de trazabilidad de fuentes
- ✅ Certificación de originalidad

### 5. Escritura Académica

- Normas APA 7ª edición estrictas (incluye: múltiples autores, citas secundarias, discusión bibliográfica)
- Estructura de tesis completa (11 secciones)
- **Construcción de párrafos TBTW** (Topic-Body-Tokens-Wrap) con 8 patrones de organización
- **Formulación de hipótesis**: 8 tipos (H₀, H₁, causal, correlacional, etc.) con proceso de 5 pasos
- **Recursos retóricos académicos**: Metáforas conceptuales, ejemplos efectivos, analogías
- Micro-mecánicas (flow, coherencia, transiciones old-to-new)
- Argumentación académica (tesis, premisas, contraargumentos)
- Meta-análisis de coherencia

### 6. Integración MCP (Opcional)

- **Search MCP**: Búsqueda académica en tiempo real
- **Task MCP**: Investigación profunda paralela
- Validación con evidencia externa actualizada
- Identificación de literatura contradictoria reciente

## ⚠️ Limitaciones y Ética

### El Skill NO hará:

- ❌ Generar contenido plagiado
- ❌ Inventar datos o fuentes
- ❌ Hacer trabajo completo del estudiante
- ❌ Participar en fraude académico
- ❌ Citar sin número de página (excepto referencias generales)

### El Skill SÍ hará:

- ✅ Asistir en comprensión de metodología
- ✅ Guiar en análisis de datos
- ✅ Revisar y mejorar escritura
- ✅ Validar coherencia y rigor
- ✅ Enseñar mientras asiste

**Filosofía**: Asistir el aprendizaje, no reemplazarlo.

## 📊 Formatos de Exportación

### Libro de Códigos:

1. **Excel (.xlsx)** - Múltiples hojas con estadísticas
2. **CSV UTF-8** - Compatible con R, Python, SPSS
3. **JSON** - Análisis programático
4. **HTML Interactivo** - Presentación visual
5. **REFI-QDA** - NVivo, MAXQDA, Atlas.ti

### Reportes:

- Análisis ACD completo (PDF/DOCX)
- Tabla de trazabilidad de fuentes
- Visualizaciones (frecuencias, coocurrencias)
- Material de defensa de tesis

## 🆘 Solución de Problemas

### El Skill no se activa

1. Verificar que carpeta esté en ubicación correcta
2. Reiniciar Claude Desktop
3. Verificar que `SKILL.md` tenga frontmatter YAML válido

### MCP no funciona

1. Verificar API key de Parallel AI
2. Revisar `claude_desktop_config.json`
3. Reiniciar Claude Desktop
4. **El Skill funciona perfectamente sin MCP** (MCP es opcional)

### Citas sin número de página

- ⚠️ Asegúrate de subir PDFs con paginación visible
- ⚠️ Proporciona metadatos bibliográficos completos
- El Skill solicitará aclaración si falta información

## 📖 Documentación Adicional

- **SKILL.md**: Instrucciones completas para Claude
- **references/**: 8 archivos con metodologías detalladas
- **examples/**: 4 casos de uso completos paso a paso
- **JSON consolidado**: `AgenteCientificoIA_Prompt_Consolidado.json` en carpeta padre

## 🤝 Contribuciones

Este Skill fue desarrollado consolidando:

- 69 archivos metodológicos de investigación cualitativa
- Guías de escritura académica (43 documentos)
- Normas APA 7ª edición
- Modelos ACD de Fairclough y Van Dijk
- Best practices de codificación cualitativa

## 📝 Licencia

Uso académico y educativo. Desarrollado para asistir investigación ética.

## 🔗 Enlaces Útiles

- **Parallel AI MCP**: https://docs.parallel.ai/integrations/mcp/getting-started
- **Claude Skills**: https://support.claude.com/en/articles/12512198-how-to-create-custom-skills
- **APA 7 Style**: https://apastyle.apa.org/
- **Repositorio Skills Anthropic**: https://github.com/anthropics/skills

---

**Versión**: 2.0
**Última actualización**: 2025-10-19
**Idiomas**: Español, Inglés
**Disciplinas**: Todas las áreas académicas

**¿Preguntas? Activa el Skill y pregúntale directamente a Claude.**
