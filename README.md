# Bomba Certa v5.7 — Admin como antes

## Alteração principal
Na conta proprietária, o painel Admin volta a aparecer imediatamente, sem esperar pela verificação assíncrona.

A conta:
`a.miguel.reis@gmail.com`

passa a mostrar logo:
- `⚙️ Admin` no topo;
- `Admin` no menu inferior;
- `⚙️ Administração` no Perfil;
- nível `Administrador`.

## Segurança
A visibilidade é imediata apenas para melhorar a experiência da conta proprietária.

As ações administrativas continuam protegidas no backend por:
- `is_app_admin()`;
- RLS;
- RPCs administrativas;
- tabela privada `private.app_admins`.

Ou seja, mostrar o botão não concede permissões a quem não as tenha no backend.
