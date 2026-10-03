# Bomba Certa v4.4 — abertura imediata

Principais correções de desempenho:

- Leaflet deixa de bloquear o HTML no arranque.
- O mapa mostra um placeholder imediato e carrega em background.
- A app tenta jsDelivr e usa unpkg como fallback para Leaflet.
- A lista de postos continua funcional mesmo que o mapa demore.
- Chart.js só é carregado quando a secção Estatísticas é aberta.
- Perfil, ranking, administração e histórico já não bloqueiam o ecrã principal.
- DGEG e OpenStreetMap arrancam depois do primeiro desenho do ecrã.
- A última localização pode ser reutilizada durante 24 horas como ponto inicial.
- O cache de postos pode ser reutilizado durante 2 horas e é atualizado em segundo plano.

Objetivo: nunca deixar o utilizador com um ecrã aparentemente parado.
