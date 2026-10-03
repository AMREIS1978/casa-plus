# Bomba Certa v4.8 — criação de contas corrigida

## Diagnóstico
A Edge Function de criação estava ativa e o backend recebia pedidos com sucesso, mas a interface podia não refletir corretamente a criação da conta.

## Correções
Na Administração, antes de criar uma conta a aplicação agora:
1. verifica se existe sessão;
2. renova a sessão se estiver perto de expirar;
3. confirma que o utilizador continua a ser administrador;
4. envia explicitamente o JWT do utilizador + publishable key para a Edge Function;
5. lê sempre a resposta real da função;
6. mostra erros claros;
7. atualiza imediatamente a lista de utilizadores após sucesso.

## Interface
- botão mostra `A criar conta…`;
- fica temporariamente bloqueado para evitar duplo clique;
- opção para ver/esconder a palavra-passe;
- mensagem verde de confirmação;
- tratamento claro de email duplicado, sessão expirada ou falta de permissões.

A `service_role` continua exclusivamente no backend e nunca é exposta no browser.
