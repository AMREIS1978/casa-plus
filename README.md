# Bomba Certa v6.4 — login simples e estável

## Registo
A pessoa escolhe:
- Nome público
- Username único
- Palavra-passe
- Email de recuperação

## Login
O login é feito apenas com:
- Username
- Palavra-passe

O email não é usado no login.

## Email
O email é apenas para recuperação da conta.
Nesta versão deixou de haver bloqueio por domínio MX ou por listas de emails temporários: basta ter formato válido.

Isto evita condicionantes desnecessárias no registo.

## Segurança
- username é único;
- associação username → conta fica em tabela privada;
- password continua a ser validada pelo Supabase Auth;
- o browser não precisa de conhecer o email interno para autenticar;
- o painel Admin continua exclusivo da conta proprietária.

## Registo concluído
Depois de criar a conta, aparece claramente:

`✓ Conta criada com sucesso. A entrar automaticamente na sua conta…`

e a sessão é iniciada logo de seguida.
