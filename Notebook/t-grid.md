# T-Grid Ceiling

##

## T-Grid Ceiling construction workflow

```mermaid
flowchart TD
    %% Row 1: Left to Right
    subgraph Row1 [Phase 1: Setting Out]
        direction LR
        A[Reference line setting out] --> B[Common Hanger Installation] --> C[Baseline Hanger Rod Prefabrication & Installation]
    end

    %% Connection down to Row 2
    C --> D

    %% Row 2: Left to Right
    subgraph Row2 [Phase 2: Main Frame]
        direction LR
        D[Suspension rod installation] --> E[Main frame fabrication & assembly] --> F[Main frame installation & levelling]
    end

    %% Connection down to Row 3
    F --> G

    %% Row 3: Left to Right
    subgraph Row3 [Phase 3: Final Panel]
        direction LR
        G[Main frame positioning and corner edge close-up] --> H[Install up blank panel]
    end

    %% Hides the border lines of the subgraphs for a clean look
    style Row1 fill:none,stroke:none
    style Row2 fill:none,stroke:none
    style Row3 fill:none,stroke:none
```

```mermaid
flowchart TD
    %% Row 1 (Left to Right)
    A[Reference line setting out] --> B[Common Hanger Installation]
    B --> C[Baseline Hanger Rod Prefab/Install]
    
    %% Connect Row 1 to Row 2
    C --> D[Suspension rod installation]
    
    %% Row 2 (Right to Left visual flow)
    D --> E[Main frame fabrication & assembly]
    E --> F[Main frame installation & levelling]
    
    %% Connect Row 2 to Row 3
    F --> G[Main frame positioning & corner close-up]
    
    %% Row 3 (Left to Right visual flow)
    G --> H[Install up blank panel]
    H --> I[Next Process / Finish]

    %% CRITICAL: Invisible vertical links to lock into a 3x3 grid layout
    A ~~~ F ~~~ G
    B ~~~ E ~~~ H
    C ~~~ D ~~~ I
```
```mermaid
flowchart TD
    %% Row 1
    A1[Node 1,1] --> A2[Node 1,2]
    A2 --> A3[Node 1,3]

    %% Row 2
    B1[Node 2,1] --> B2[Node 2,2]
    B2 --> B3[Node 2,3]

    %% Row 3
    C1[Node 3,1] --> C2[Node 3,2]
    C2 --> C3[Node 3,3]

    %% Vertical Connections
    A1 --> B1
    B1 --> C1
    
    A2 --> B2
    B2 --> C2
    
    A3 --> B3
    B3 --> C3
```
