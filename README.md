# Bomba Certa v3.3 — GPS robusto + editor de confiança

## GPS
A navegação deixa de depender da rota interna.

Cada posto passa a ter:
- **GPS** — abre imediatamente a aplicação de navegação do dispositivo;
- **Ver rota** — mantém a rota dentro da Bomba Certa.

Comportamento:
- iPhone/iPad: Apple Maps;
- Android: app de mapas/navegação através do esquema `geo:`;
- computador: Google Maps;
- dentro da rota continuam disponíveis botões para GPS do telemóvel e Google Maps.

## Editor de confiança
A aplicação passa a suportar o campo `trusted_publisher` na tabela `fuel_contributor_stats`.

Quando esse campo está ativo:
- um preço publicado por esse utilizador é aceite imediatamente;
- não precisa de 5, 4, 3 ou 2 confirmações;
- aparece no perfil/ranking como **Editor de confiança**.

O privilégio não é controlado por uma palavra-passe escrita no código. Isso evita expor credenciais no HTML público.

## Segurança
Nunca colocar a palavra-passe de uma conta de administração dentro de `index.html`, JavaScript público ou README.
