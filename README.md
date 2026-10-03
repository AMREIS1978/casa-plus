# Bomba Certa v7.3 — Analytics no painel Admin

## Novo resumo administrativo
O painel de Administração apresenta agora:

- Utilizadores registados
- Visualizações da página hoje
- Visualizações totais
- Visualizações acumuladas nos últimos 7 dias
- Distribuição diária das visualizações dos últimos 7 dias

## Como é medida uma visualização
Cada carregamento real da página executa uma RPC segura `record_page_view`.
É gerado um UUID único para esse carregamento, impedindo que a mesma chamada seja
gravada duas vezes por acidente.

Não é necessário o utilizador estar autenticado para a visualização ser contabilizada.
Quando está autenticado, o backend pode associar internamente o evento ao `auth.uid()`.

## Segurança
Os eventos de visualização são guardados em `private.page_view_events`.
O browser não tem acesso direto à tabela.

A escrita é feita apenas por:
`public.record_page_view(...)`

O resumo só pode ser consultado por uma conta que passe:
`public.is_app_admin()`

através de:
`public.admin_dashboard_summary()`

## Nota importante
A contagem de visualizações começa quando esta versão for publicada.
Não é possível reconstruir com rigor visualizações históricas anteriores que nunca
foram registadas pela aplicação.
