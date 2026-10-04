# Bomba Certa v9.1 — Mapa sempre ajustado

## Problema corrigido
Em desktop, quando a lista de postos era maior do que o mapa, ao fazer scroll ficava uma grande área vazia por baixo da coluna do mapa.

## Nova lógica
- Em desktop, o cartão do mapa fica **sticky** e acompanha o scroll da lista.
- A altura do mapa adapta-se à altura disponível do ecrã.
- Em ecrãs mais baixos, o mapa reduz automaticamente.
- O painel de rota, quando aberto, continua acessível sem empurrar o mapa para fora do ecrã.
- Em tablet e telemóvel o mapa volta ao fluxo normal para não ocupar permanentemente o ecrã.

## Leaflet
Foi acrescentado um `ResizeObserver` ao mapa para chamar `invalidateSize()` sempre que a dimensão visual muda. Isto evita tiles cortados ou áreas cinzentas quando o mapa adapta a altura.
