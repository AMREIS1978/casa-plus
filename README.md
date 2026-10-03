# Bomba Certa v5.5 — maior cobertura de preços

## Problema corrigido
A versão anterior encontrava postos, mas muitos apareciam sem preço porque a pesquisa DGEG estava demasiado dependente do município atual e de chamadas diretas do browser.

## Nova arquitetura

### Cache oficial próprio
Foi criada a tabela:
`fuel_official_prices`

Guarda:
- posto DGEG;
- combustível;
- preço;
- localização;
- data de atualização oficial;
- data da última consulta.

A app consulta este cache logo no início, portanto os últimos preços oficiais conhecidos podem aparecer muito mais depressa.

### Pesquisa DGEG no servidor
Nova Edge Function:
`dgeg-nearby-prices`

A função:
- identifica o distrito;
- pesquisa o distrito e distritos vizinhos;
- para raios maiores alarga progressivamente a cobertura;
- filtra os resultados pela distância real ao utilizador;
- devolve apenas postos dentro do raio escolhido;
- grava os preços encontrados no cache oficial.

Isto é especialmente importante em zonas de fronteira municipal/distrital, como Espinho / Gaia / Feira.

### Fallback
Se a nova pesquisa server-side falhar, a aplicação mantém a pesquisa DGEG antiga como fallback.

## Interface
A pesquisa passa também a mostrar:
`Preços disponíveis em X de Y postos (Z%).`

Assim é imediatamente visível a cobertura de preços conseguida.
