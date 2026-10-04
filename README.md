# Bomba Certa v8.0 — Interface Premium

Esta versão atualiza o frontend para uma linguagem visual mais moderna, elegante e mobile-first, inspirada no conceito aprovado.

## Principais alterações
- hero e filtros redesenhados;
- mapa e lista em cartões premium;
- navegação inferior flutuante;
- melhor tipografia, espaçamento, sombras e hierarquia;
- cartões de posto mais compactos e legíveis;
- vários preços de combustível por posto, quando existem na base de dados;
- combustível selecionado destacado;
- origem DGEG/Comunidade indicada em cada preço;
- roda-pé comunitário e publicidade mantidos;
- funcionalidades existentes preservadas: rota, atualizar preço, abastecimento, validação, denúncia, perfil, ranking, administração e analytics.

## Vários preços
A app consulta, para os postos já encontrados, preços oficiais em `fuel_official_prices` e preços comunitários recentes em `fuel_price_reports`.

A prioridade mantém-se:
1. preço comunitário recente;
2. preço oficial DGEG;
3. sem preço.

Os cartões mostram até cinco combustíveis em simultâneo e continuam a ordenar pelo combustível selecionado.
