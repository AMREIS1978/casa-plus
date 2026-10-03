# Bomba Certa v7.0 — erro `supabase.rpc(...).catch is not a function` corrigido

## Causa
O cliente Supabase devolve um objeto PostgREST `thenable` em `supabase.rpc(...)`.
Esse objeto pode ser usado com `await`, mas não deve ser tratado como uma Promise normal com `.catch()`.

A aplicação tinha três chamadas deste género:

`supabase.rpc('ensure_my_fuel_profile').catch(...)`

Isso fazia o JavaScript parar depois de criar/iniciar a conta.

## Correção
Foi criado um wrapper seguro:

`safeEnsureFuelProfile()`

que usa `try/catch` com `await supabase.rpc(...)`.

Foram corrigidas as três ocorrências:
- carregamento inicial da aplicação;
- criação de nova conta;
- carregamento do perfil.

## Resultado
Depois de criar a conta:
1. conta criada;
2. sessão iniciada;
3. perfil garantido;
4. mensagem `Conta criada com sucesso. Parabéns!`;
5. entrada imediata na aplicação.

Nenhuma conta existente foi alterada.
