# Bomba Certa v4.1 — nível no topo + mapa mais rápido

## Mini-perfil no cabeçalho
Ao lado de `Sair`, a fotografia passa a mostrar imediatamente por baixo:
- Novato
- Explorador
- Guia
- Especialista
- Embaixador
- Editor de confiança
- Administrador

Foi escolhida a posição **por baixo da fotografia** porque mantém a imagem limpa e continua legível em telemóvel.

## Mapa mais rápido
Foram feitas várias otimizações:

1. O mapa é criado imediatamente após o login.
2. Se existir uma localização recente no dispositivo, o mapa abre logo nessa zona.
3. Caso não exista, abre imediatamente numa vista geral de Portugal.
4. A base permanente e os postos comunitários são carregados primeiro.
5. DGEG e OpenStreetMap entram depois, em paralelo.
6. Os detalhes de preços DGEG deixam de bloquear a abertura inicial do mapa.
7. Leaflet mantém mais tiles em memória para reduzir redesenhos.

## Scripts pesados
Tesseract OCR e Chart.js deixaram de carregar no arranque:
- Tesseract só é carregado quando o utilizador escolhe/tira uma fotografia.
- Chart.js só é carregado quando são necessários os gráficos.

Isto reduz bastante o peso inicial da aplicação e melhora especialmente a abertura no telemóvel.
