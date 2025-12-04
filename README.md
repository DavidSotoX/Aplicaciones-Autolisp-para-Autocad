# 🧭 Generador de Planimetría para AutoCAD (AutoLISP + ObjectARX)

## 📌 Descripción General
Este proyecto ofrece dos herramientas —una escrita en **AutoLISP** y otra en **C++ con ObjectARX**— que automatizan la generación de **planimetrías** a partir de polilíneas seleccionadas en AutoCAD.

Ambas versiones permiten:
- Extraer coordenadas **X, Y**.
- Exportar:
  - Coordenadas.csv  
  - Planimetria.doc  
- (AutoLISP) Insertar puntos en cada vértice.

Dirigido a topógrafos, ingenieros civiles, arquitectos, profesionales GIS, delineantes y estudiantes que requieren precisión y automatización geométrica.

---

## 📂 Contenido del Proyecto

### 🔷 Módulo en C++ (ObjectARX)
Implementa el comando `GenerarPlanimetria`:
1. Solicita una polilínea.
2. Lee los vértices usando ObjectARX.
3. Exporta los archivos CSV y DOC.

Librerías usadas:
`aced.h`, `acutads.h`, `dbents.h`, `dbapserv.h`.

### 🔶 Script AutoLISP
Comando `GP`:
1. Comprueba si es una polilínea.
2. Obtiene los vértices mediante Visual LISP.
3. Inserta puntos en cada vértice.
4. Exporta CSV y DOC.

---

## 🚀 Características Principales
- Exportación automática de coordenadas (CSV).
- Documento de planimetría (DOC).
- Compatible con polilíneas 2D estándar.
- Extensible para cálculos adicionales.
- Compatible con AutoCAD Full.

---

## 🛠️ Tecnologías Utilizadas

### ObjectARX (C++)
- Clases: `AcDbPolyline`, `AcGePoint3d`, `AcDbEntity`.
- Selección con `acedEntSel`.

### AutoLISP + Visual LISP API
- Funciones: `entget`, `entsel`, `vlax-get-property`, `vla-addpoint`.
- Escritura de archivos: `open`, `write-line`, `close`.

---

## 📥 Instalación

### 🔷 Instalación del módulo ObjectARX (C++)
1. Compilar con Visual Studio (2019+ recomendado).
2. Usar ObjectARX SDK correspondiente a tu versión de AutoCAD.
3. Cargar en AutoCAD ejecutando:

