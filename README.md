# Bomba Certa v10.1 — Perfil + Publicidade Analytics

## Cabeçalho
A barra inferior mantém-se fixa no telemóvel.

Ao lado da fotografia passam a aparecer:
- nome público;
- categoria/nível.

O conjunto é compacto e responsivo, incluindo ecrãs pequenos.

## Publicidade
Todas as áreas principais têm espaço publicitário:
- Mapa/Postos;
- Abastecimentos;
- Viagem;
- Análise;
- Perfil;
- Administração.

No Mapa existe ainda uma segunda posição lateral/feed em desktop.

## Medição
Foi criado tracking real no Supabase:
- impressão;
- clique;
- página/posição do anúncio;
- data/hora;
- utilizador quando autenticado.

Uma impressão só é registada quando pelo menos 50% do anúncio fica visível durante cerca de 650 ms.

## Painel Admin
Novo quadro Publicidade com:
- visualizações totais;
- cliques totais;
- CTR global;
- vistas/cliques hoje;
- resultados por posição;
- CTR por posição.

Backend:
- `public.app_ad_events`
- `public.record_ad_event(...)`
- `public.admin_ad_analytics()`

RLS está ativo. Visitantes/utilizadores podem apenas inserir eventos válidos; apenas administrador pode consultar os registos agregados.
