# Bomba Certa v8.2 — Melhor Escolha Inteligente

## Nova funcionalidade principal
A página inicial passa a calcular automaticamente o **Melhor posto para si**.

A decisão já não usa apenas o menor preço por litro. Considera:
- preço do combustível;
- distância ao posto;
- litros que o utilizador pretende abastecer;
- consumo médio do automóvel;
- custo estimado da deslocação de ida e volta.

## Fórmula
Para cada posto:

`custo_abastecimento = litros × preço_litro`

`custo_deslocação = distância_ida_volta × consumo/100 × preço_litro`

`custo_total = custo_abastecimento + custo_deslocação`

Ganha o posto com menor `custo_total`.

## Poupança
A app compara a melhor escolha com o posto disponível mais próximo e apresenta a poupança estimada quando a deslocação a outro posto realmente compensa.

## Personalização
O utilizador pode ajustar:
- litros a abastecer (predefinição: 50 L);
- consumo médio do carro (predefinição: 6,5 L/100 km).

As preferências ficam guardadas localmente no dispositivo.

## UX
- cartão premium imediatamente antes do mapa;
- no telemóvel aparece cedo no fluxo;
- botão direto “Ver rota”;
- explicação transparente de porque aquele posto foi escolhido;
- indicação clara de que o custo de deslocação é uma estimativa.

## Nota técnica
Nesta versão a distância usada é a distância aproximada disponível na pesquisa. Uma evolução futura pode trocar esta estimativa pela distância rodoviária real da rota para tornar o cálculo ainda mais preciso.
