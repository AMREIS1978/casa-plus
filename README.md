# Bomba Certa v5.6 — painel de administração restaurado

## Diagnóstico
A conta principal continua registada no backend como:
- papel: `owner`
- acesso administrativo: ativo

O painel tinha desaparecido por causa da ordem de carregamento do frontend depois das alterações de autenticação.

## Correções
- a app aguarda a identidade autenticada antes de verificar `is_app_admin()`;
- se a primeira verificação falhar por latência, tenta novamente uma vez;
- o painel Admin volta a aparecer no menu inferior;
- foi acrescentado `⚙️ Admin` no topo, junto de `Sair`;
- no Perfil, administradores veem também `⚙️ Administração`;
- o nível da conta proprietária passa a aparecer como `Administrador`, sem ser substituído por `Editor de confiança`;
- ranking, perfil e mapa deixam de controlar ou atrasar a visibilidade do painel administrativo.

As permissões continuam a ser decididas no backend e não pelo email escrito no JavaScript.
