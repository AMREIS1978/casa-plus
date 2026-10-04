# Bomba Certa v8.5 — Preços reais + cálculo corrigido

## O que foi corrigido

### 1. Preços
A aplicação deixa de depender do combustível selecionado para tentar preencher os cartões.

Além da função backend, existe agora um fallback direto à API oficial da DGEG que:
- pesquisa os 7 combustíveis;
- percorre todas as páginas necessárias;
- filtra apenas os postos no raio do utilizador;
- agrega os preços por ID oficial do posto;
- mantém a Comunidade como fonte prioritária quando existe uma atualização comunitária mais recente.

Não são criados valores artificiais.

### 2. Frescura
Cada preço pode indicar:
- DGEG / Comunidade;
- há quanto tempo foi atualizado;
- aviso “desatualizado na fonte” quando tem mais de 21 dias.

Isto evita apresentar um preço antigo como se fosse atual.

### 3. Melhor Escolha
O cálculo foi refeito.

Para cada posto:
- custo no posto = litros × preço por litro;
- custo para chegar = distância até ao posto × consumo médio / 100 × preço por litro;
- custo total = custo no posto + custo para chegar.

Sempre que possível, a distância usada é a distância rodoviária obtida por OSRM, e não a distância em linha reta.

A “vantagem líquida estimada” compara a Melhor Escolha com o posto com preço conhecido mais próximo e mostra separadamente:
- poupança no abastecimento;
- custo extra de deslocação;
- vantagem líquida.

## Importante
Nem todas as estações vendem todos os combustíveis e algumas fontes oficiais podem estar desatualizadas. Nesses casos a aplicação assinala a ausência/frescura em vez de inventar um valor.
