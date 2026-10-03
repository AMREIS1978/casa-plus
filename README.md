# Bomba Certa v4.9 — registo corrigido + comunidade

## Registos corrigidos
Os logs mostravam tentativas de `/signup` tratadas como registos anónimos, que o Auth rejeitava.

A criação pública de conta passa agora por uma Edge Function própria:
- nome público;
- email;
- palavra-passe;
- conta criada e confirmada no backend;
- login automático após a criação;
- limite de registos por ligação para reduzir abuso;
- honeypot anti-bot;
- `service_role` nunca exposta no browser.

## Perfil inicial
O nome escolhido no registo é guardado nos metadados e usado automaticamente no perfil de contribuinte.

## Comunidade e jogo
Nova área na página inicial:
- sequência de dias com atividade;
- contribuições de hoje;
- preços atualizados hoje;
- validações de hoje;
- participantes ativos hoje;
- nível atual;
- missões simples;
- botão para convidar um amigo.

## Primeira missão
Depois do primeiro registo aparece um onboarding curto:
- confirmar um preço de outro condutor; ou
- atualizar o preço de um posto.

## Filosofia
A gamificação incentiva ajuda real entre utilizadores:
- pontos por contribuições úteis;
- progressão por níveis;
- desbloqueios;
- reconhecimento;
- comunidade ativa.

Não existem apostas, prémios monetários aleatórios ou mecânicas escondidas.
