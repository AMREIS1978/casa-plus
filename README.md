# Bomba Certa v8.9 — Paragens só na reserva

## Regra principal
A Viagem Inteligente deixa de sugerir abastecimentos antecipados.

A lógica é:
1. calcular quando a autonomia prevista entra na reserva;
2. procurar um posto real nessa zona;
3. escolher o melhor posto entre os que são alcançáveis durante a reserva;
4. só criar nova paragem quando voltar a entrar na reserva.

Se a autonomia chega ao destino com a reserva definida, a app apresenta **0 paragens**.

## Entrada na reserva
O campo deixou de ser tratado como uma margem de segurança abstrata e passa a significar literalmente:
**“quando faltam aproximadamente X km de autonomia, o carro entra na reserva.”**

Exemplo:
- autonomia atual: 250 km;
- entrada na reserva: 40 km;
- a app começa a procurar a paragem por volta dos 210 km percorridos.

## Fallback de segurança
Se não existir nenhum posto com preço real na zona de reserva, a app pode usar o último posto imediatamente antes da reserva e explica explicitamente que se trata de um fallback de segurança.

## Resultado
Cada paragem mostra:
- autonomia prevista à chegada;
- indicação de RESERVA;
- litros recomendados;
- preço real;
- custo;
- razão da paragem.
