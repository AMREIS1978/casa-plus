# Bomba Certa v5.1 — login corrigido

## Diagnóstico
Os logs do Supabase confirmam que a conta administrativa consegue autenticar por email/password com sucesso.

O problema estava na interface: depois de uma autenticação aceite, qualquer falha posterior no arranque da app podia deixar ou voltar a mostrar uma mensagem de credenciais incorretas.

## Correções
- autenticação e arranque da app foram separados;
- assim que o Supabase aceita o login, a sessão é considerada válida;
- o ecrã de login desaparece imediatamente;
- uma falha posterior no carregamento de mapa/perfil/comunidade não volta a ser apresentada como erro de palavra-passe;
- mensagens antigas desaparecem assim que o utilizador volta a escrever;
- se já existir uma sessão válida, a app entra diretamente sem voltar a pedir login.
