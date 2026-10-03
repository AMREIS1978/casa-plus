# Bomba Certa v6.0 — Admin e alteração de nomes corrigidos

## Painel Admin
A conta `a.miguel.reis@gmail.com` volta a ver o painel imediatamente após autenticação.

A visibilidade do painel deixa de depender de uma resposta assíncrona que podia falhar momentaneamente. As ações administrativas continuam protegidas no backend.

## Alterar nome
Foram corrigidos os dois cenários:
- o utilizador altera o próprio nome no Perfil;
- a conta proprietária altera o nome de qualquer utilizador no painel Admin.

Foi criada e verificada no backend a função:
`admin_set_user_name(uuid, text)`

Ela:
- exige permissões administrativas;
- atualiza o nome no perfil público;
- sincroniza o nome nos metadados Auth;
- não mexe em pontos, nível ou permissões.

Também permanece disponível:
`update_my_display_name(text)` para o próprio utilizador.
