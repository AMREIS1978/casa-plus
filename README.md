# Bomba Certa v11.2 — Média Nacional Sempre Visível

Corrige o problema do bloco aparecer sem informação.

## Nova lógica de dados
A app nunca fica dependente de uma única chamada:

1. tenta o preço médio diário oficial;
2. se essa chamada falhar, calcula em tempo real uma **média nacional observada** com os preços dos postos publicados pela API DGEG;
3. se a API nacional também falhar, mostra o último valor oficial DGEG guardado.

Nunca apresenta 0% ou “Indisponível” quando existe informação oficial anterior.

## Transparência
- “DGEG” = média diária oficial quando disponível;
- “DGEG · média observada” = média aritmética calculada dos preços nacionais dos postos DGEG;
- “DGEG · último oficial” = último valor oficial conhecido.

A tendência/probabilidade continua identificada como estimativa Bomba Certa, não previsão oficial.
