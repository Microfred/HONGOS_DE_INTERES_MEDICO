# 🧫 Hongos de Interés Médico - Análisis Filogenómico

## 📌 Introducción  
Este repositorio contiene un **catálogo bioinformático de hongos clínicamente relevantes** y sus relaciones evolutivas mediante reconstrucción filogenómica. El proyecto integra:  

- 🦠 **Lista estandarizaday actualizada** de especies fúngicas patógenas (levaduras, hongos filamentosos, dimórficos)  
- 🧬 **Análisis genómico comparativo** basado en genes marcadores y genomas completos  
- 🌳 **Filogenias robustas** (ML/Bayesianas) para estudiar patrones de virulencia y resistencia  

## 🎯 Objetivos  
1. Crear un recurso abierto para investigación médica en micología  
2. Identificar clados con propiedades clínicas compartidas (ej: resistencia a antifúngicos)  
3. Validar taxonomías actuales con datos genómicos  

## 📂 Estructura del Proyecto :
```
repo/
├── data/
│ ├── clinical_fungi_list.csv # Lista curada de especies
│ └── genomes/ # Secuencias en formato FASTA
├── notebooks/
│ └── phylogenomic_analysis.ipynb # Pipeline de análisis
└── results/
├── trees/ # Archivos Newick/FigTree
└── annotations/ # Genes de virulencia/resistencia
```


## 🔍 Métodos Clave  
- **Herramientas**: `OrthoFinder` (ortólogos), `IQ-TREE` (filogenia), `GTDB-Tk` (taxonomía)  
- **Marcadores**: Genes BUSCO + proteínas ribosomales  
- **Visualización**: `ggtree` (R) o `ETE3` (Python) `figtree` (Gráfico) `itol` (on-line)

## 📚 Referencias  
- [WHO Fungal Priority Pathogens List (2022)](https://www.who.int/publications/i/item/9789240060241)  
- GTDB Database para taxonomía microbiana  

---

✨ **¡Contribuciones bienvenidas!**  
¿Quieres añadir especies o mejorar el pipeline? Abre un *issue* o envía un *PR*.  

*OJO* estamos en construcción. julio 2025.

### 🟠 Levaduras patógenas
| Nombre científico            | Enfermedades asociadas                     | Notas clave                              |
|------------------------------|--------------------------------------------|------------------------------------------|
| *Candida albicans*           | Candidiasis mucocutánea/sistémica         | #1 en infecciones nosocomiales           |
| *Candida auris*              | Candidiasis invasiva                       | Multirresistente, emergente global       |
| *Candida glabrata*           | Candidiasis urogenital                     | Resistencia a fluconazol                 |
| *Cryptococcus neoformans*    | Meningitis, neumonía                       | Capsulado, targeting SNC en VIH+         |
| *Malassezia furfur*          | Pitiriasis versicolor, dermatitis         | Levadura lipofílica de la piel           |

### 🟢 Hongos dimórficos
| Nombre científico            | Enfermedad principal               | Distribución geográfica          |
|------------------------------|------------------------------------|-----------------------------------|
| *Histoplasma capsulatum*      | Histoplasmosis                     | Valles fluviales (Américas)      |
| *Coccidioides immitis*        | Fiebre del Valle                   | Suroeste de EE.UU., México       |
| *Blastomyces dermatitidis*    | Blastomicosis                      | Grandes Lagos (EE.UU./Canadá)    |
| *Paracoccidioides brasiliensis*| Paracoccidioidomicosis            | América Latina                   |

### 🔵 Mohos patógenos
| Nombre científico            | Enfermedad                         | Población de riesgo              |
|------------------------------|------------------------------------|-----------------------------------|
| *Aspergillus fumigatus*       | Aspergilosis pulmonar invasiva     | Neutropénicos, trasplantados     |
| *Rhizopus arrhizus*           | Mucormicosis rinosinusal           | Diabéticos no controlados        |
| *Fusarium solani*             | Queratitis, infecciones diseminadas| Quemados, inmunodeprimidos       |
| *Lomentospora prolificans*    | Micosis osteoarticular             | Resistente a voriconazol         |

### 🟣 Dermatofitos
| Nombre científico            | Infección típica           | Localización anatómica       |
|------------------------------|----------------------------|------------------------------|
| *Trichophyton rubrum*        | Tiña pedis/ungueal         | Pies, uñas                   |
| *Microsporum canis*          | Tiña capitis               | Cuero cabelludo (niños)      |
| *Epidermophyton floccosum*   | Tiña cruris                | Región inguinal              |

### 🟡 Oportunistas emergentes
| Nombre científico            | Enfermedad asociada        | Característica única         |
|------------------------------|----------------------------|------------------------------|
| *Pneumocystis jirovecii*     | Neumonía intersticial      | Profilaxis en VIH+           |
| *Talaromyces marneffei*      | Micosis diseminada         | Endémico en Tailandia/Vietnam|
| *Scedosporium apiospermum*   | Neumonía necrotizante      | Resistente a polienos        |
