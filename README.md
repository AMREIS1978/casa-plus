# Bomba Certa v8.4 — Cobertura Máxima de Preços

## Objetivo
Reduzir drasticamente os cartões com “Sem preço” e mostrar, em cada posto, todos os combustíveis conhecidos independentemente do combustível selecionado.

## Alterações
- os cartões mostram os 7 combustíveis suportados;
- o combustível escolhido continua destacado;
- a pesquisa DGEG passa a pedir dados multi-combustível;
- a Edge Function `dgeg-nearby-prices` foi atualizada para v3;
- a função usa o detalhe oficial de cada posto DGEG para recolher vários combustíveis numa única pesquisa;
- o cache oficial passa a ser usado também para descobrir preços de outros combustíveis;
- quando um posto OSM/Base Bomba Certa não tem a mesma chave DGEG, o frontend tenta associá-lo por proximidade geográfica e semelhança do nome;
- preços comunitários recentes continuam a prevalecer sobre preços oficiais anteriores;
- a cobertura mostra agora:
  - postos com preço no combustível selecionado;
  - postos com pelo menos um preço conhecido.

## Fontes
Prioridade de qualidade:
1. Comunidade recente Bomba Certa, quando existente;
2. DGEG / Preços dos Combustíveis;
3. cache DGEG já validado;
4. OpenStreetMap apenas para localização/descoberta de postos sem preço.

Não são usados preços inventados nem valores estimados para preencher espaços vazios.
