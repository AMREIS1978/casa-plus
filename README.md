# MyGGas v10.9 — Como Chegar

## Alteração de nome
`Ver rota` foi substituído por **Como chegar**.

É mais intuitivo porque descreve diretamente o que o utilizador pretende fazer.

## Correção funcional
O botão agora:
1. tenta usar a localização já conhecida;
2. se ainda não existir, pede a geolocalização;
3. calcula o percurso dentro da MyGGas com OSRM;
4. apresenta distância e tempo;
5. disponibiliza **Iniciar navegação** no Google Maps;
6. se o cálculo interno falhar, mantém sempre o fallback para Google Maps.

As chaves dos postos também passam a ser codificadas nos botões inline para evitar falhas com caracteres especiais.


## Rebrand MyGGas
A aplicação mantém a mesma base funcional desta versão. Foi alterado apenas o nome para **MyGGas** e aplicada a logomarca fornecida no ecrã de entrada e no cabeçalho, sem alterar a lógica da aplicação.
