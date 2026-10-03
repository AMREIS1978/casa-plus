# Bomba Certa v6.1 — registo público corrigido

## Problema identificado
Os logs do Supabase mostraram pedidos de registo a falhar com:

`429 email rate limit exceeded`

Ou seja, a criação de contas estava dependente do email de confirmação padrão do Supabase e atingia o limite de envio.

## Solução
Foi criada a Edge Function:

`public-register`

O novo fluxo:
1. valida nome, email e palavra-passe;
2. aplica proteção anti-abuso / rate limit;
3. cria a conta no servidor;
4. marca o email como confirmado;
5. a aplicação inicia sessão imediatamente com o email e palavra-passe escolhidos;
6. cria o perfil Bomba Certa e entra na aplicação.

Assim, o registo público deixa de depender do envio de email de confirmação.

## Segurança
- service role nunca é exposta no browser;
- função tem honeypot;
- limita tentativas por IP e email;
- valida nome/email/password;
- não concede privilégios administrativos;
- o painel Admin continua reservado à conta proprietária.

## Utilização
O utilizador preenche:
- Nome público
- Email
- Palavra-passe
- Confirma participação responsável

Depois carrega em `Criar a minha conta` e entra automaticamente.
