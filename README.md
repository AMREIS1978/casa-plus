# Bomba Certa v7.7 — preços visíveis para toda a comunidade em tempo real

## Alteração principal
O canal Realtime passa agora a arrancar imediatamente após o login de qualquer utilizador.

Antes, a subscrição podia ficar dependente de a geolocalização terminar com sucesso.
Agora isso deixa de acontecer.

## Resultado
Quando um utilizador altera um preço:

1. o preço é gravado em `fuel_price_reports`;
2. a tabela está incluída na publicação `supabase_realtime`;
3. todos os utilizadores autenticados com a aplicação aberta recebem o evento;
4. o rodapé `Comunidade em direto` atualiza automaticamente;
5. quem estiver a visualizar esse posto recebe também a atualização da listagem;
6. novos utilizadores que entrem depois veem a alteração porque os dados ficam persistidos na base de dados.

## Segurança
A leitura de `fuel_price_reports` continua limitada a utilizadores autenticados através de RLS.
Cada alteração mantém:
- utilizador responsável;
- posto;
- combustível;
- preço;
- data/hora.

O feed público dentro da comunidade mostra apenas o nome público e a alteração efetuada.
