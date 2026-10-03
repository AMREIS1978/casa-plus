# Bomba Certa v4.3 — pesquisa automática ao abrir

## Alteração principal
A aplicação já não espera que o utilizador carregue em `Procurar perto de mim`.

Assim que o utilizador entra:
1. o mapa abre imediatamente;
2. usa a última localização conhecida;
3. mostra logo os últimos postos guardados, se existirem;
4. começa imediatamente a atualizar postos e preços;
5. pede uma localização nova ao navegador em paralelo;
6. corrige a zona automaticamente se a posição tiver mudado.

## Botão
`📍 Procurar perto de mim` passa a servir apenas para:
- forçar nova localização;
- repetir a pesquisa;
- atualizar manualmente.

## Otimização adicional
A lista em cache já não chama o backend antes de aparecer.

Antes:
cache → esperar comunidade/backend → mostrar.

Agora:
cache → mostrar imediatamente → atualizar backend em segundo plano.

Isto elimina um dos maiores atrasos percebidos.

## Timeout de localização
A primeira tentativa usa um timeout curto, porque a interface já tem dados para mostrar em paralelo. Assim a app não fica bloqueada à espera do GPS.
