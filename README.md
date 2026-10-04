# Bomba Certa v9.8 — Mobile + Mapa ao Primeiro Toque

## Nome da app no telemóvel
Foi criada uma linha mobile dedicada exclusivamente ao wordmark **Bomba Certa**.

Isto elimina a competição de espaço entre:
- nome da app;
- navegação;
- perfil;
- ações do cabeçalho.

Em PC continua a ser usada a marca original do cabeçalho. Em tablet/telemóvel aparece sempre a nova marca dedicada.

## Mapa
O mapa foi ajustado para interação imediata em dispositivos tácteis:

- `touch-action: none` apenas dentro do mapa;
- foco no primeiro `pointerdown`;
- duplo clique/box zoom desativados em touch;
- scroll wheel desativado em touch;
- marcadores abrem popup também em `touchstart`;
- função única `makeFuelMarker()` garante o mesmo comportamento em todas as renderizações.

Resultado esperado: um único toque num posto abre imediatamente o respetivo popup, sem ser necessário “ativar” primeiro o mapa.
