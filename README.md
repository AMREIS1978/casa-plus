# Bomba Certa v9.0 — Paragens Otimizadas

## Problema corrigido
A versão anterior podia criar uma segunda paragem de poucos litros porque tratava a reserva como uma quantidade que tinha de existir também à chegada ao destino.

Isso estava errado para o comportamento pretendido.

## Nova regra
A reserva passa a servir apenas como **gatilho para procurar uma paragem**.

A app:
1. verifica primeiro se a autonomia atual chega ao destino;
2. se chegar, cria 0 paragens;
3. quando entra na reserva, procura o melhor posto alcançável;
4. nesse posto calcula se um abastecimento permite concluir toda a viagem;
5. se permitir, abastece logo o necessário e termina o plano;
6. se ainda forem necessárias mais etapas, maximiza a autonomia para reduzir o número de paragens.

## Eliminação de micro-paragens
Se a última paragem for inferior a 8 L, a app tenta primeiro transferir essa quantidade para a paragem anterior, desde que exista capacidade no depósito.

Assim evita situações como:
- primeira paragem: 38 L;
- segunda paragem: 3 L;

quando seria possível reforçar a primeira e eliminar a segunda.

Se não houver capacidade física para absorver esses litros na paragem anterior, a pequena paragem mantém-se e é identificada como **matematicamente indispensável** — nunca é escondida nem inventada.

## Critério
O objetivo prioritário passa a ser:
**menor número real de paragens compatível com a autonomia do veículo**.

O preço e o desvio escolhem o melhor posto apenas depois de garantido esse objetivo.
