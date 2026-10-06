# MyGGas Live

Função nova e isolada adicionada à app existente através de um único botão flutuante **LIVE**.

Não foram alteradas as funções nem a navegação existentes.

## MyGGas Live
- alertas próximos da comunidade;
- acidentes;
- trânsito;
- obras;
- perigos;
- estrada fechada;
- inundação;
- veículo parado;
- outros alertas;
- publicação georreferenciada;
- expiração automática dos alertas;
- avisos por voz opcionais;
- atualização automática opcional;
- modos de rota:
  - Chegar primeiro;
  - Fugir à confusão;
  - Ir nas calmas;
  - Poupar uns trocos;
- cálculo de alternativas;
- cruzamento das rotas com alertas ativos da comunidade;
- recomendação de percurso.

## Dados de trânsito
A função comunitária é real e partilhada via Supabase.
OSRM calcula alternativas, mas não fornece congestionamento live de terceiros.
Para velocidades reais de trânsito e ETA dinâmico deverá ser adicionada posteriormente uma API de tráfego (HERE, TomTom, Google Routes ou Mapbox).

## Privacidade
A localização só é solicitada quando o utilizador abre/use o MyGGas Live ou publica um alerta.
