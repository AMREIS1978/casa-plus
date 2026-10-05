# Bomba Certa v10.6 — Responsive Perfeito

## Correção estrutural
Foi acrescentada uma camada de proteção responsiva para impedir qualquer página, cartão, grelha, mapa, tabela ou painel de ultrapassar a largura real do ecrã.

## Mobile
- todas as páginas passam para uma coluna;
- nenhum contentor pode ultrapassar 100% do viewport;
- tabelas largas fazem scroll dentro do próprio componente;
- combustíveis mantêm scroll horizontal local;
- mapas ajustam a 100% da largura;
- KPIs e grelhas reorganizam-se automaticamente;
- cabeçalho adapta nome + perfil;
- navegação de páginas permanece fixa e sempre visível em baixo;
- safe-area de iPhone respeitada.

## Ecrãs muito pequenos
Abaixo de 330 px, labels e perfil compactam automaticamente para evitar cortes e scroll lateral.
