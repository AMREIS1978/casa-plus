# Bomba Certa v8.6 — Viagem Inteligente

## Acesso
Funcionalidade exclusiva para **Explorador ou superior**.

O acesso não é apenas visual: foi criada no Supabase a função:
`public.can_use_trip_planner()`

Características:
- `SECURITY INVOKER`;
- usa o perfil do próprio utilizador;
- `anon` sem permissão;
- `authenticated` com execução;
- desbloqueia a partir de 50 pontos ou Editor de confiança.

## Planeamento
O utilizador indica:
- origem;
- destino;
- ida e volta / só ida;
- combustível;
- autonomia atual;
- consumo médio;
- capacidade do depósito;
- reserva de segurança;
- estratégia: Equilibrado / Mais barato / Menos paragens.

## Dados
A rota usa OSRM.
A geocodificação usa OpenStreetMap/Nominatim.
Os preços usados no cálculo são reais:
- DGEG;
- Comunidade recente quando existe e pode ser associada ao posto.

Postos sem preço real para o combustível selecionado não entram no cálculo económico.

## Algoritmo
1. Calcula a rota rodoviária.
2. Pesquisa postos DGEG até 8 km do corredor da rota.
3. Associa a posição de cada posto ao percurso.
4. Refina o desvio rodoviário de postos relevantes com OSRM.
5. Respeita autonomia e reserva mínima.
6. Seleciona paragens de acordo com a estratégia.
7. Quando existe um posto mais barato alcançável, recomenda apenas o combustível necessário para lá chegar com reserva; caso contrário, abastece o necessário para avançar com segurança.

## Economia
A economia não é comparada com um valor inventado.

Referência:
**os mesmos litros recomendados × preço mediano dos postos reais encontrados junto à rota**.

Depois é descontado o custo estimado dos desvios.

Mostra:
- preço mediano encontrado;
- custo dos abastecimentos recomendados;
- custo dos desvios;
- economia líquida estimada.

## Responsive
A nova área adapta-se a:
- desktop;
- portátil/tablet;
- telemóvel;
- ecrãs muito pequenos.
