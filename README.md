# Bomba Certa v4.2 — pesquisa instantânea

## Problema resolvido
Ao tocar em `📍 Procurar perto de mim`, o utilizador deixa de ficar à espera sem perceber o que está a acontecer.

## Novo comportamento
1. O botão muda imediatamente para `A localizar…`.
2. O mapa centra imediatamente na última posição conhecida, quando disponível.
3. Os últimos postos conhecidos aparecem do cache local quase instantaneamente.
4. Se ainda não existirem dados, aparecem cartões skeleton enquanto a pesquisa decorre.
5. Base Bomba Certa + comunidade chegam primeiro.
6. DGEG + OpenStreetMap atualizam depois, em paralelo.
7. Os preços DGEG mais detalhados são enriquecidos apenas depois de já existir conteúdo no ecrã.
8. Quando termina, o botão volta automaticamente a `Procurar perto de mim`.

## Cache
A aplicação guarda temporariamente:
- localização recente: até 30 minutos;
- lista de postos: até 20 minutos, desde que a nova posição esteja a menos de 3 km da posição guardada.

Os dados em cache são mostrados como resposta imediata e depois atualizados em segundo plano.

## Pré-aquecimento
Se o utilizador já tiver concedido permissão de localização, a app começa discretamente a preparar localização e postos logo após entrar, antes de carregar no botão.

## Perceção de velocidade
A prioridade passa a ser:
`reagir imediatamente → mostrar algo útil → atualizar silenciosamente`

em vez de:
`esperar por todas as fontes → só depois mostrar resultados`.
