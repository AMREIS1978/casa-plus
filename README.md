# Bomba Certa v6.6 — login corrigido de vez

## Problema
O campo de login tinha `maxlength=20` porque tinha sido pensado apenas para usernames.

Ao escrever um email, o browser cortava o texto, por exemplo:
`a.miguel.reis@gmail.`

## Correção
O campo de login:
- deixou de ter limite de 20 caracteres;
- aceita username;
- aceita também email como fallback;
- mantém password normal;
- não altera o modelo de registo: novos utilizadores continuam a escolher username e o email continua associado à recuperação.

## Backend
`public-login` foi atualizado para a versão 5.

Se o texto contém `@`, valida diretamente como email.
Caso contrário, resolve o username através da tabela privada.

Assim:
- utilizadores novos podem entrar com username;
- contas antigas e utilizadores habituados ao email continuam a conseguir entrar;
- não há truncagem do email.
