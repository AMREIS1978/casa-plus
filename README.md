# Bomba Certa v8.3 — Visitante + Critério Transparente

## Critério da Melhor Escolha
A app passa a explicar o cálculo dentro do próprio cartão:
1. preço por litro;
2. custo do abastecimento = preço × litros;
3. custo estimado da deslocação de ida e volta;
4. ganha o posto com menor custo total.

A poupança fica explicitamente identificada como:
**Poupa vs. posto mais próximo**.

## Modo Visitante
Novo botão no login:
**Continuar como visitante**.

O visitante pode consultar postos, preços oficiais, mapa, rota, vários combustíveis e a Melhor Escolha sem criar conta.

Para alterar preços, validar informação, guardar abastecimentos ou reportar um posto é necessário criar conta.

## Segurança
O backend foi ajustado para leitura anónima apenas dos dados públicos necessários:
- `fuel_official_prices`;
- `fuel_station_registry`.

Mantêm-se protegidos os dados de utilizadores, contribuições, validações, abastecimentos e administração.
