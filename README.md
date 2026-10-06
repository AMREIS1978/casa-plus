# MyGGas — Radar melhorado + Desafio Diário

## MyGGas LIVE
A função de trânsito LIVE não faz parte desta versão. A app volta a concentrar-se nas funções que já acrescentam valor real.

## Radar melhorado
O Radar foi revisto porque podia falhar postos quando o utilizador passava em andamento.

Melhorias:
- GPS com `maximumAge: 0`;
- raio por defeito: 250 m;
- opção até 300 m;
- deteção não apenas na posição atual, mas também no segmento percorrido entre duas leituras GPS;
- deteta postos mesmo quando não existe preço atual;
- nesses casos convida a atualizar ou fotografar o painel;
- se a lista de postos ainda não estiver carregada, tenta atualizar os postos na zona;
- ao afastar-se mais de 2 km da pesquisa original, atualiza a zona em segundo plano.

## Desafio do Dia
Foi acrescentado um cartão na página principal.

Os desafios rodam diariamente entre:
- Confirma e ganha — confirmar um preço da comunidade: +5 pontos;
- Caçador de preços — atualizar um preço: +8 pontos;
- Olho vivo — reportar o estado de um posto: +6 pontos.

A recompensa só pode ser recebida uma vez por dia e é validada no backend.
