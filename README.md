# MyGGas

Repositório oficial do website e aplicação web MyGGas.

## Estrutura

- `/index.html` — website público
- `/app/` — aplicação MyGGas
- `/privacy.html` — Política de Privacidade
- `/cookies.html` — Cookies e Publicidade
- `/terms.html` — Termos de Utilização
- `/delete-account.html` — Eliminação de conta
- `/ads.txt` — preparado para Google AdSense
- `/app-ads.txt` — preparado para Google AdMob
- `/robots.txt`
- `/sitemap.xml`
- `/.htaccess` — configuração para Hostinger/Apache

## Publicação no Hostinger

O conteúdo deste repositório deve ser publicado diretamente em `public_html`.

Não ative publicidade real antes de:
1. obter aprovação do AdSense/AdMob;
2. configurar a CMP/consentimento;
3. substituir os placeholders em `ads.txt` e `app-ads.txt`;
4. inserir os IDs reais de produção.

## Segurança

Nunca coloque no repositório:
- service role keys;
- passwords;
- ficheiros `.env`;
- chaves privadas;
- keystores Android;
- credenciais Hostinger.

A app frontend deve usar apenas chaves públicas/publicáveis.

## Estado

Base pronta para GitHub e posterior deployment para Hostinger.
