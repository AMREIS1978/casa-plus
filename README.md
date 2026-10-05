# MyGGas v12.1 — Corporate Stable

Versão reconstruída sobre a última base com autenticação funcional.

## Correção principal
A versão anterior tinha perdido o bloco JavaScript responsável por:
- `authCheck()`
- botão **Entrar**
- login por username/email através de `public-login`
- criação de conta
- modo visitante
- recuperação de acesso

Esta versão volta a incluir integralmente esse fluxo.

## Estrutura
- `index.html`
- `assets/myggas-logo.png`
- `assets/myggas-hero.jpg`

## Mantido
Mapa, postos, preços, social, perfil, apagar perfil, abastecimentos, viagem inteligente,
análise, navegação fixa, “Como chegar” e restantes funcionalidades da base estável.

## MyGGas Market
O painel nacional é compacto e consulta a função `dgeg-national-average`.
