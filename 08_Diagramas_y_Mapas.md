---
Materia: "Diagramas & Mapas"
Estado: "Listo"
Autores_clave:
  - "Antigravity"
  - "Emmanuel M"
Conceptos_clave:
  - "[[Complejo Industrial]]"
  - "[[Aethelgard Holdings]]"
  - "[[Brea Oxidada]]"
  - "[[La Frecuencia Alfa]]"
tags:
  - "brea-oxidada"
  - "diagramas"
  - "mapas"
  - "conduccion"
---

# 🗺️ 08. Diagramas y Cartografía de la Campaña

Este documento reúne las representaciones esquemáticas en formato **Mermaid** para guiar al Guardián en la visualización geográfica, la estructura arquitectónica del complejo y el flujo deductivo de la campaña.

---

## 🗺️ 1. Mapa Regional de la Cuenca (Valle de la Brea)

Este diagrama simula las rutas y puntos de pesaje, bombeo y subestaciones que conectan la metrópolis con el complejo y los municipios aledaños de la cuenca salina.

```mermaid
graph TD
    %% Estilos de Nodos
    classDef principal fill:#2d3748,stroke:#4a5568,stroke-width:2px,color:#fff;
    classDef intermedio fill:#1a202c,stroke:#718096,stroke-width:1px,color:#cbd5e0,stroke-dasharray: 5 5;
    classDef expansion fill:#2c5282,stroke:#3182ce,stroke-width:2px,color:#fff;
    
    %% Nodos Principales
    Valle["🏭 Complejo Industrial Valle de la Brea"]:::principal
    Metro["🏢 La Metrópolis (Piso 14 Aethelgard)"]:::principal
    Colinas["🌲 Colinas (Refugio Disidentes)"]:::principal
    
    %% Nodos de Expansión
    Salinas["🧂 Salinas de la Brea (Sanatorio San Judas)"]:::expansion
    Puerto["⚓ Puerto Herrumbre (SS Goliad)"]:::expansion
    Colonia["🏡 Colonia Nueva Esperanza (Capilla)"]:::expansion
    
    %% Puntos Intermedios
    Bascula["⚖️ Báscula de Ruta 9"]:::intermedio
    Bombeo["🚰 Estación de Bombeo #4"]:::intermedio
    Subestacion["⚡ Subestación Valle Frío"]:::intermedio

    %% Conexiones Regionales
    Metro -->|Ruta Estatal 4| Valle
    Valle <-->|Ruta 9 / Bascula| Salinas
    Valle <-->|Camino Fluvial / Bombeo| Puerto
    Valle <-->|Línea Eléctrica / Subestacion| Colonia
    Colonia <-->|Senderos Forestales| Colinas
    Colinas <-->|Frecuencias de Radio| Clara_BBS["💻 BBS The Phantom Screen"]:::intermedio
    Clara_BBS <--> Valle
```

---

## 🏢 2. Estructura Arquitectónica del Complejo Valle de la Brea

Este plano simula la distribución física y no euclidiana interna de las instalaciones industriales y sus niveles de hostilidad o interés clave.

```mermaid
graph TD
    %% Estilos de Nodos
    classDef sector fill:#2c3e50,stroke:#34495e,stroke-width:2px,color:#ecf0f1;
    classDef peligro fill:#962d2d,stroke:#c0392b,stroke-width:2px,color:#fff;
    classDef clave fill:#27ae60,stroke:#2ecc71,stroke-width:2px,color:#fff;

    %% Estructura Interna
    Entrada["🚪 Verja Exterior (Cadenas y Patrulla)"]:::sector
    Oficina["🏢 Bloque Administrativo (Oficina y Terminal CRT)"]:::sector
    Taller["🔧 Taller Técnico (Cinta Grabadora y Prototipos)"]:::clave
    Almacen["📦 Almacén 3 (El Laberinto Euclidiano)"]:::peligro
    Sotano["⚙️ Subestación Subterránea (Generadores y Brea)"]:::peligro
    Julia["👥 Nódulo Julia (Voz de la Estática)"]:::clave
    Torre["📡 Torre de Refrigeración Central (Antena Alfa)"]:::peligro

    %% Caminos y Accesos
    Entrada --> Oficina
    Oficina --> Taller
    Oficina --> Almacen
    Almacen -->|Geometría Deformada| Sotano
    Sotano --> Julia
    Sotano -->|Cableado de Fuerza| Torre
    Taller -->|Patente y Origami| Sotano
```

---

## 🔍 3. Mapa Deductivo de Pistas (Flujo de la Investigación)

Este diagrama ilustra la relación causa-efecto de los handouts y cómo guían al grupo de sesión en sesión.

```mermaid
graph LR
    %% Estilos
    classDef sesion fill:#2c3e50,stroke:#34495e,color:#fff;
    classDef pista fill:#d68910,stroke:#ba4a00,color:#fff;

    %% Flujo
    S1["S1: Eco Magnético"]:::sesion
    S2["S2: Geometría de Concreto"]:::sesion
    S3["S3: Cifrado Corporativo"]:::sesion
    S4["S4: Frecuencia Alfa"]:::sesion

    H1["H1: Contrato Aethelgard"]:::pista
    H4["H4: Registro BBS Julia"]:::pista
    H2["H2: Plano en Origami"]:::pista
    H3["H3: Manuscrito Fragmentos"]:::pista
    H5["H5: Autopsia Ajustador"]:::pista

    S1 --> H1 & H4
    H1 & H4 --> S2
    S2 --> H2
    H2 -->|Revela Laboratorio Oculto| S3
    S3 --> H3 & H5
    H3 & H5 -->|Clave del Descifrado final| S4
```
