# Bomba Certa v7.8 — correção da reversão para o preço DGEG

## Problema identificado
O preço comunitário era corretamente gravado, mas a pesquisa de postos trabalha em vários fluxos assíncronos.

Depois de o preço comunitário aparecer, um dos fluxos de atualização DGEG podia executar `renderBasicStations()` novamente.
Esse renderer dava prioridade a:

`officialPrice ?? displayPrice`

Por isso o ecrã podia regressar temporariamente — ou ficar — no preço oficial anterior.

O caso R STAR confirmou o problema:
existiam registos comunitários mais recentes, mas a interface mostrava novamente o valor DGEG.

## Correção
A prioridade visual passa a ser sempre:

`displayPrice ?? officialPrice`

Depois de `renderStations()` resolver o preço comunitário mais recente, esse valor não volta a ser substituído por um valor oficial antigo durante a mesma pesquisa.

Além disso:
- o ramo rápido de pesquisa termina também com `renderStations()`;
- o preço comunitário resolvido é guardado no cache local;
- o mapa usa a mesma prioridade;
- o badge passa a manter `Comunidade` quando esse é o preço em vigor;
- um refresh da página já não deve reintroduzir o DGEG antigo antes da atualização comunitária.

## Regra funcional
Um preço comunitário mais recente é o preço apresentado à comunidade até:
- surgir uma atualização comunitária posterior;
- ou a lógica de validação futura determinar que esse preço deve deixar de ser considerado válido.
