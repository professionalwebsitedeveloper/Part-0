# part 0

```mermaid

flowchart TB
    A["User submits form"] L_A_B_0@--> B["Browser sends POST to /new_note"]
    B L_B_C_0@-- becomes --> C["s2b"]
    C L_C_D_0@--> D["The browser follows the redirect and GETs /notes"]
    D L_D_E_0@--> E["HTML returned by server"]
    E L_E_F_0@--> F["CSS is retrieved by the browser"]
    F L_F_G_0@--> G["JavaScript is retrieved by the browser"]
    G L_G_H_0@--> H["Browser GETs /data.json, runs JS"]
    H L_H_I_0@--> I["The server responds with JSON containing the new note"]
    I L_I_J_0@--> J["Browser displays notes"]

    style A fill:#00C853
    style B fill:#FF6D00
    style C fill:#FF6D00
    style D fill:#FF6D00
    style E fill:#FF6D00
    style F fill:#FF6D00
    style G fill:#FF6D00
    style H fill:#FF6D00
    style I fill:#FF6D00
    style J fill:#00C853
    linkStyle 0 stroke:#FF6D00,fill:none
    linkStyle 1 stroke:#FF6D00
    linkStyle 2 stroke:#FF6D00,fill:none
    linkStyle 3 stroke:#FF6D00,fill:none
    linkStyle 4 stroke:#FF6D00,fill:none
    linkStyle 5 stroke:#FF6D00,fill:none
    linkStyle 6 stroke:#FF6D00,fill:none
    linkStyle 7 stroke:#FF6D00,fill:none
    linkStyle 8 stroke:#FF6D00,fill:none

    L_A_B_0@{ animation: fast } 
    L_B_C_0@{ animation: fast } 
    L_C_D_0@{ animation: fast } 
    L_D_E_0@{ animation: fast } 
    L_E_F_0@{ animation: fast } 
    L_F_G_0@{ animation: fast } 
    L_G_H_0@{ animation: fast } 
    L_H_I_0@{ animation: fast } 
    L_I_J_0@{ animation: fast }
