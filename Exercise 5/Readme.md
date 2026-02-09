# part 0

```mermaid

flowchart TB
    A["User navigates to /spa"] L_A_B_0@--> B["Browser GETs spa.html"]
    B L_B_C_0@--> C["Browser GETs main.css"]
    C L_C_D_0@--> D["Browser GETs spa.js"]
    D L_D_E_0@--> E["Browser executes spa.js"]
    E L_E_F_0@--> F["spa.js fetches data.json"]
    F L_F_G_0@--> G["Server returns JSON"]
    G L_G_H_0@--> H["JS renders notes with DOM"]
    H L_H_I_0@--> I["Page is ready<br>No further reloads needed"]
    A@{ shape: rounded}
    B@{ shape: rounded}
    C@{ shape: rounded}
    D@{ shape: rounded}
    E@{ shape: rounded}
    F@{ shape: rounded}
    G@{ shape: rounded}
    H@{ shape: rounded}
    I@{ shape: rounded}
     B:::Pine
     C:::Pine
     D:::Pine
     E:::Pine
     F:::Pine
     G:::Pine
     H:::Pine
     I:::Pine
    classDef Sky stroke-width:1px, stroke-dasharray:none, stroke:#374D7C, fill:#E2EBFF, color:#374D7C
    classDef Pine stroke-width:1px, stroke-dasharray:none, stroke:#254336, fill:#27654A, color:#FFFFFF
    style A fill:#FF6D00
    style B fill:#2962FF
    style C fill:#AA00FF
    style D stroke:none,fill:#2962FF
    style E fill:#AA00FF
    style G fill:#2962FF
style I stroke:#FFD600,fill:#FF6D00
    linkStyle 0 stroke:#FF6D00,fill:none
    linkStyle 1 stroke:#2962FF,fill:none
    linkStyle 2 stroke:#AA00FF,fill:none
    linkStyle 3 stroke:#2962FF,fill:none
    linkStyle 4 stroke:#AA00FF,fill:none
    linkStyle 5 stroke:#00C853,fill:none
    linkStyle 6 stroke:#2962FF,fill:none
    linkStyle 7 stroke:#00C853,fill:none

    L_A_B_0@{ animation: slow } 
    L_B_C_0@{ animation: fast } 
    L_C_D_0@{ animation: slow } 
    L_D_E_0@{ animation: slow } 
    L_E_F_0@{ animation: slow } 
    L_F_G_0@{ animation: fast } 
    L_G_H_0@{ animation: slow } 
    L_H_I_0@{ animation: slow }
