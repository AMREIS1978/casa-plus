# Bomba Certa v6.3 — login por username

## Registo
Cada pessoa escolhe:
- Nome público
- Username único
- Palavra-passe
- Email de recuperação

## Login
O login passa a ser feito apenas com:
- Username
- Palavra-passe

O email deixa de aparecer no ecrã de login.

## Email
O email serve apenas para recuperação da conta.

No registo, continuam a ser aplicadas verificações ao domínio e bloqueio de emails descartáveis.

## Contas já existentes
Foi atribuído automaticamente um username às contas que já existiam.

A conta principal ficou com:
`MiguelReis`

As restantes contas receberam como username a parte do email antes do `@`, com ajuste automático em caso de duplicação.

## Segurança
A associação Username → conta fica numa tabela privada.
O browser nunca recebe o email interno usado pelo Supabase para fazer autenticação por password.
