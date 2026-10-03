# Bomba Certa v4.5 — corrigida e rápida

Esta versão foi reconstruída a partir da última base estável em vez de continuar a acumular alterações na v4.4.

## O que muda

### Abertura
Assim que entra:
- o mapa é criado imediatamente;
- a última localização conhecida é usada, se existir;
- postos guardados aparecem logo;
- a pesquisa real começa em paralelo.

### Pesquisa progressiva
1. cache local;
2. base permanente Bomba Certa;
3. postos da comunidade;
4. DGEG e OpenStreetMap;
5. detalhes dos preços;
6. validações, autor, denúncias e informação social.

A lista inicial já não espera pelas fases 4–6.

### Mapa
Volta ao carregamento estável da versão que funcionava.
Foram retiradas as experiências de carregamento dinâmico da v4.4 que podiam deixar o mapa preso.

### Perfil
No topo, junto a `Sair`, aparece:
- fotografia;
- nível/status imediatamente por baixo.

### Fiabilidade
Se uma fonte externa estiver lenta, os postos já obtidos continuam visíveis e utilizáveis.
