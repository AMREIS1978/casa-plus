# Bomba Certa v7.6 — rodapé a passar em rotação contínua

## Alteração pedida
O rodapé da comunidade deixou de funcionar por mensagens estáticas a rodar uma a uma.

Agora passa em **formato contínuo de roda-pé**, como uma fita informativa.

## O que mudou
- foi criada uma zona `community-activity-marquee`;
- as mensagens recentes são concatenadas numa única linha;
- o conteúdo é duplicado para permitir scroll contínuo sem quebra;
- a animação é feita em CSS com `@keyframes communityTicker`;
- em telemóvel a velocidade é ligeiramente ajustada.

## Exemplo visual
`João alterou Gasóleo simples em Posto X de 1,729 €/L para 1,699 €/L · há 2 min • Maria alterou GPL Auto em Posto Y para 0,899 €/L · agora mesmo • …`

## Comportamento
- se não existir atividade, o rodapé mostra uma mensagem simples;
- quando entram novas alterações, o conteúdo é reconstruído e volta a arrancar;
- mantém-se imediatamente acima da navegação inferior.
