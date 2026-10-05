# Bomba Certa v10.2 — Localização + Criar Posto + Publicidade

## A sua localização
O marcador do utilizador deixa de ser igual aos postos.

Novo marcador:
- azul;
- pulsante;
- com orientação visual própria;
- prioridade visual superior aos postos;
- popup próprio “A sua localização”.

Assim o utilizador distingue imediatamente:
**eu** vs. **posto de combustível**.

## Criar posto
Foi corrigida a lógica de abertura do modal.

Existe agora uma única função:
`window.openAddStation()`

É usada tanto por:
- `+ Posto`;
- `Adicionar posto` na coluna lateral.

A janela:
- abre acima do mapa e navegação;
- limpa dados antigos;
- pré-preenche latitude/longitude quando já existe localização;
- envia visitantes para criação de conta;
- apresenta feedback caso a geolocalização falhe.

## Publicidade
Todas as páginas continuam a ter publicidade e as páginas longas passam a ter um segundo espaço no rodapé:
- Postos/Mapa;
- Abastecimentos;
- Viagem;
- Análise;
- Perfil;
- Administração.

Todos os novos espaços usam o mesmo tracking de:
- impressão real;
- clique;
- CTR;
- página/posição.

Esses dados aparecem no painel de Administração > Publicidade.
