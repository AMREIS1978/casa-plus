# Bomba Certa v6.9 — registo final corrigido

## Causa real encontrada
O backend estava a tentar aceder diretamente às tabelas do schema `private`
através do Data API/PostgREST.

O Supabase devolvia `PGRST106 / 406`, por isso acontecia isto:
- o utilizador preenchia corretamente o formulário;
- o Auth chegava mesmo a criar o utilizador;
- o passo seguinte, que ligava username e email de recuperação à conta, falhava;
- o frontend recebia erro e parecia ficar bloqueado.

## Correção aplicada no backend
Foram criadas RPCs `SECURITY DEFINER` para fazer, de forma controlada:
- procurar username;
- procurar email de recuperação;
- registar a associação username + contacto de recuperação.

As Edge Functions deixaram de tentar aceder diretamente ao schema privado.

Estado:
- `public-register`: versão 6
- `public-login`: versão 7

## Compatibilidade
As contas já existentes não foram alteradas.
Continuam a entrar como anteriormente.

## Experiência
O estado do registo aparece agora imediatamente debaixo do botão.

Depois da criação:
`✅ Conta criada com sucesso. Parabéns!`
`A entrar automaticamente na sua conta…`

A aplicação entra logo na conta quando a sessão é criada.
