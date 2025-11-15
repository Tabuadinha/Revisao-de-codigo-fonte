# Revisao-de-codigo-fonte

-------------------------------------
GRAFO DE FLUXO
-------------------------------------

Nós (N)

N1 Início

N2 Verificação de usuário

N3 Verificação de senha

N4 Sucesso

N5 Erro: senha incorreta

N6 Erro: usuário não encontrado

N7 Fim

Arestas (E)

N1 → N2

N2 → (usuário encontrado) → N3

N2 → (usuário inexistente) → N6

N3 → (senha correta) → N4

N3 → (senha incorreta) → N5

N4 → N7

N5 → N7

N6 → N7

-------------------------------------
COMPLEXIDADE CICLOMÁTICA
-------------------------------------

A complexidade ciclomática é dada pela fórmula:

V(G)=E−N+2

Onde:

E = número de arestas
N = número de nós

No grafo acima:

E = 8
N = 7

V(G)=8−7+2=3
Complexidade ciclomática = 3

-------------------------------------
CAMINHOS BÁSICOS
-------------------------------------

Caminho 1 — Login bem-sucedido

1 → 2 → 3 → 4 → 7
(usuário válido, senha válida)

Caminho 2 — Usuário inexistente

1 → 2 → 6 → 7
(usuário não encontrado)

Caminho 3 — Senha incorreta

1 → 2 → 3 → 5 → 7
(usuário válido, senha inválida)
