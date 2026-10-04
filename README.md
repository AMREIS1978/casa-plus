# Bomba Certa v10.0 — Cabeçalho Mobile Corrigido

## Correção estrutural
O problema não era apenas o tamanho da palavra Bomba Certa. A navegação principal estava dentro do mesmo `header`, o que permitia sobreposição em determinados browsers/escala de dispositivo.

Nesta versão a estrutura foi alterada:

- o header contém apenas **Bomba Certa + perfil**;
- a navegação é um elemento independente;
- no PC, a navegação fica centrada no topo;
- no telemóvel/tablet, a mesma navegação passa para o fundo;
- o nome da app nunca partilha o mesmo espaço físico com a barra de navegação.

## Mobile
- Bomba Certa sempre visível no topo;
- perfil compacto à direita;
- barra de navegação fixa no fundo;
- saída continua acessível através do perfil;
- safe-area respeitada em iPhone.
