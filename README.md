# Bomba Certa v6.5 — login por username corrigido

## Causa
O login por username estava a resolver corretamente o utilizador, mas a validação da password no backend estava a usar o cliente administrativo.

Isso podia devolver `invalid_credentials` mesmo quando o username estava corretamente associado à conta.

## Correção
A função `public-login` foi atualizada para:
1. resolver `username -> user_id` numa tabela privada;
2. obter internamente o email associado;
3. validar a password com um cliente Auth normal;
4. devolver a sessão ao browser;
5. o browser grava essa sessão e entra na aplicação.

O email continua escondido no login e serve apenas para recuperação.

## Estado
`public-login` encontra-se ativo na versão 4 do backend.
