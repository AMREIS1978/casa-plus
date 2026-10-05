# Bomba Certa v10.3 — Comentários + Publicidade

## Número dos comentários
O contador deixou de aparecer como um pequeno balão sobreposto ao ícone.

Agora aparece de forma discreta e alinhada:
**💬 2**

A mesma lógica foi aplicada às partilhas:
**↗ 3**

Fica mais próxima da linguagem visual das redes sociais e não compete com os emojis.

## Botão da publicidade
O botão **Saber mais** passa a funcionar em todos os espaços.

Comportamento:
1. regista o clique;
2. se existir `data-ad-url`, abre o destino da campanha;
3. se a posição ainda não tiver URL configurado, abre um painel elegante que explica que o espaço está ativo e pronto para campanha.

Isto evita botões que parecem não fazer nada.

## Tracking
O clique continua a ser contabilizado no painel Admin independentemente de o anúncio ainda estar em modo placeholder ou já ter destino configurado.
