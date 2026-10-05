# Bomba Certa v11.0 — Média Nacional + Tendência

## Novo painel nacional
Foi acrescentado ao ecrã Mapa um painel que acompanha o combustível selecionado e mostra:

- preço médio diário oficial DGEG para Portugal Continental;
- data do último valor oficial publicado;
- probabilidade estimada de **subir**;
- probabilidade estimada de **manter**;
- probabilidade estimada de **descer**;
- interpretação automática da evolução mais recente.

## Fonte
DGEG — Preço Médio Diário (Continente).

O preço médio é o valor oficial publicado pela DGEG.  
As probabilidades NÃO são previsões da DGEG: são uma estimativa Bomba Certa baseada exclusivamente na série recente de preços médios oficiais.

## Backend
Nova Edge Function:
`dgeg-national-average`

A função é pública apenas para leitura de informação pública da DGEG e não acede a dados pessoais ou credenciais do utilizador.

Se a fonte DGEG estiver indisponível, a app não inventa valores e apresenta “Indisponível”.
