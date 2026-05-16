# SGE-Java-Robin-Diaz---Luis-Garcia
graph TD
    A([Inicio]) --> B[Inicializar Variables:<br/>totalEstudiantes = 0<br/>banderaSalir = false]
    B --> C{¿banderaSalir es falsa?}
    
    C -- Sí --> D[/Mostrar Menú/]
    D --> E[/Leer Opción/]
    E --> F{Opción elegida}
    
    F -- 1 --> G[Llamar a agregarEstudiante]
    G --> H[/Leer ID y Nombre/]
    H --> I[Añadir a lista y totalEstudiantes++]
    I --> C
    
    F -- 2 --> J[Llamar a mostrarLista]
    J --> K{¿Lista vacía?}
    K -- Sí --> L[/Mostrar: Lista vacía/]
    K -- No --> M[/Recorrer lista e imprimir/]
    L --> C
    M --> C
    
    F -- 3 --> N[Llamar a buscarPorID]
    N --> O[/Leer ID de búsqueda/]
    O --> P{¿ID encontrado?}
    P -- Sí --> Q[/Mostrar Nombre/]
    P -- No --> R[/Mostrar: No encontrado/]
    Q --> C
    R --> C
    
    F -- 4 --> S[banderaSalir = true]
    S --> T[/Mostrar: Saliendo del sistema/]
    T --> C
    
    F -- Otro --> U[/Mostrar: Opción no válida/]
    U --> C
    
    C -- No --> V([Fin])

    style A fill:#f9f,stroke:#333,stroke-width:2px
    style V fill:#f9f,stroke:#333,stroke-width:2px
    style F fill:#fff4dd,stroke:#d4a017,stroke-width:2px
