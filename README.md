# Bomba Certa v3.5 — administração segura

## Conta proprietária
A conta associada ao email configurado no projeto recebeu o papel de **owner/admin** no backend.

## Poderes
O administrador tem acesso de leitura/escrita/eliminação às tabelas principais da Bomba Certa através de políticas RLS específicas de administrador.

Também dispõe de:
- lista das contas registadas;
- email;
- data de criação;
- último acesso;
- nome público;
- pontos;
- eliminação permanente de outras contas.

## Eliminar contas
A eliminação exige duas confirmações:
1. escrever `APAGAR`;
2. confirmar novamente.

Ao eliminar um utilizador, os objetos de Storage que lhe pertenciam são transferidos para o administrador antes da eliminação, evitando bloqueios por propriedade de ficheiros.

A última conta administradora não pode ser eliminada através desta função, evitando que a aplicação fique sem proprietário.

## Segurança
O estatuto de administrador é guardado no backend, numa tabela privada. Não é decidido por email, palavra-passe ou JavaScript do browser.

A palavra-passe nunca é guardada no código público.
