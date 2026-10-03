# CASA+ v0.5 — despesas + combustíveis em tempo real

## Novo
- apagar receitas ou despesas diretamente nos movimentos;
- localização voluntária através do navegador;
- pesquisa ativa de postos de combustível próximos com OpenStreetMap/Overpass;
- mapa interativo;
- filtros por combustível e raio;
- preços colaborativos reportados por utilizadores autenticados;
- atualização em tempo real via Supabase Realtime;
- indicação da idade do preço reportado;
- ordenação pelos preços mais baratos quando existem dados da comunidade;
- interface em português de Portugal.

## Privacidade
A localização é pedida pelo navegador apenas quando o utilizador carrega em “Localizar e procurar”.
A CASA+ não guarda a localização atual do utilizador. Os relatórios de preço guardam a localização do posto, não a posição pessoal do utilizador.

## Fonte oficial DGEG
O portal português de preços de combustíveis indica que a informação pode ser usada livremente, mas proíbe utilização comercial. Por esse motivo a v0.5 não incorpora automaticamente preços DGEG numa aplicação potencialmente comercial.

## Deploy
Substituir `index.html` e `README.md` na branch `main`.
