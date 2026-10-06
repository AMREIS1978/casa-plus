# MyGGas v10.9 — Radar

Nova funcionalidade **MyGGas Radar**, opt-in e totalmente controlada pelo utilizador.

## Funcionamento
- opção Ativar/Desativar no Perfil;
- distância configurável: 120 / 180 / 250 m;
- limite diário configurável: 1 / 2 / 3 / 5 alertas;
- não repete o mesmo posto durante 24 horas;
- só pergunta quando existe preço real disponível;
- mostra posto, combustível, preço e idade da informação;
- “Está correto” atribui +2 pontos;
- “O preço mudou” abre a atualização de preço existente;
- “Fotografar painel” abre diretamente a leitura fotográfica existente;
- “Agora não” fecha o convite;
- no browser/app ativa, acompanha a posição apenas quando o utilizador ativou o Radar.

## Backend
Foi criado o RPC autenticado `confirm_radar_price`, com:
- validação de proximidade até 300 m;
- cooldown de 24 h por utilizador/posto/combustível;
- +2 pontos por confirmação;
- registo privado de auditoria;
- sem acesso `anon`.

## Nota Android
Esta versão não pede localização em background. Isso reduz risco de rejeição na Play Store.
Para alertas com a app totalmente fechada, a fase seguinte deve usar um modo Radar/Viagem nativo iniciado expressamente pelo utilizador.
