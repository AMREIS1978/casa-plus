# Bomba Certa v7.5 — atualização comunitária de preços

## Todos os utilizadores autenticados podem atualizar preços

Foi consolidado um fluxo único de publicação através da RPC:

`public.submit_fuel_price(...)`

A função:
- exige sessão autenticada;
- usa automaticamente `auth.uid()`;
- valida o posto;
- valida o combustível;
- valida preços entre 0,50 € e 5,00 €/L;
- cria um novo registo comunitário sem permitir a um utilizador alterar diretamente o registo histórico de outro.

Isto mantém histórico e responsabilidade por cada alteração.

## Alterar qualquer combustível

O modal `Atualizar preço` tem agora um seletor próprio de combustível.
O utilizador pode atualizar diretamente:
- Gasóleo simples
- Gasóleo aditivado / premium
- Gasolina simples 95
- Gasolina 95 aditivada / premium
- Gasolina 98
- Gasolina 98 aditivada / premium
- GPL Auto

## Rodapé de atividade comunitária

Foi acrescentado um rodapé persistente, imediatamente acima da navegação.

Exemplo:

`● Comunidade · João alterou Gasóleo simples em Posto X de 1,729 €/L para 1,699 €/L · há 2 min`

Quando não existe preço anterior:

`Maria alterou Gasolina simples 95 em Posto Y para 1,759 €/L`

O rodapé:
- mostra as últimas 12 alterações;
- roda automaticamente as mensagens;
- atualiza em Realtime quando entra uma nova alteração.

## Privacidade

O feed não expõe email, user_id, password ou contacto de recuperação.
Mostra apenas:
- nome público;
- posto;
- combustível;
- preço;
- momento da atualização.

A consulta é feita por uma RPC `SECURITY DEFINER` que expõe apenas estes campos.
