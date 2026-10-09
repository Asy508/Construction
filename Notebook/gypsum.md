# Light Steel Keel Gypsum Board Partition Wall

1. Regulatory & design requirement
2. Introduction
3. Construction process

## Regulatory

1. **GB50210-2018** => Standard construction quality acceptance of building decoration

## Material

1. Gypsum board
2. Horizontal stud
3. Support clip/bridging clip

## Process

```mermaid
flowchart TD
    %% Row 1: Left to Right
    A[Layout marking & module division] --> B[Fixed keel along top & ground]
    B --> C[Fixed frame keel]
    C --> D[Install vertical keel]
    
    %% Transition down to Row 2
    D --> E[Install doors & windows frames]
    
    %% Row 2: Right to Left (Forced visually by connecting E -> F -> G -> H)
    E --> F[Install additional keel]
    F --> G[Install support keel]
    G --> H[Concealed wiring pipes]
    
    %% Transition down to Row 3
    H --> I[Install the side cover panel]
    
    %% Row 3: Left to Right
    I --> J[Filled with acoustic insulation]
    J --> K[Install other side cover panel]
    K --> L[Seam and corner protection]

    %% Invisible alignment links to force the structural snake layout
    A ~~~ H
    B ~~~ G
    C ~~~ F
    H ~~~ I
    G ~~~ J
    F ~~~ K
    E ~~~ L
```


