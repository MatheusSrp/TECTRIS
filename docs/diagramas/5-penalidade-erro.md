```mermaid
stateDiagram-v2

[*] --> Resposta_Incorreta

Resposta_Incorreta --> Perda_Pontos

Perda_Pontos --> Bloco_Penalidade : penalidade adicional
Perda_Pontos --> Fluxo_Normal : sem penalidade extra

Bloco_Penalidade --> Impacto_Jogo
Impacto_Jogo --> Feedback

Fluxo_Normal --> Feedback

Feedback --> Atualizar_Estado_Jogo

Atualizar_Estado_Jogo --> [*]
```