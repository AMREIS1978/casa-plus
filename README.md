# Bomba Certa v6.8 — criação de conta corrigida

## Erro encontrado
O frontend da versão anterior tentava ler `signupUsername`, mas o campo Username não estava presente no formulário HTML.

Resultado:
- o utilizador preenchia nome, email e password;
- ao clicar em `Criar a minha conta`, o JavaScript parava antes de chamar o backend;
- visualmente parecia que o botão ficava bloqueado.

## Correção
O formulário passa a mostrar explicitamente:
1. Nome público
2. Username
3. Email de recuperação
4. Palavra-passe
5. Aceitação da participação responsável

## Fluxo final
Ao clicar em `Criar a minha conta`:
- valida os campos;
- cria a conta;
- mostra `✓ Conta criada com sucesso. Parabéns!`;
- faz login automático;
- entra imediatamente na Bomba Certa;
- mostra um aviso visível no topo durante alguns segundos.

## Compatibilidade
Nenhuma conta existente foi alterada ou eliminada.

As contas antigas continuam compatíveis com username/email.
As novas contas usam username como identificação principal e email como contacto de recuperação.
