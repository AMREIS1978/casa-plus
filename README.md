# Bomba Certa v5.9 — Admin exclusivo do proprietário

## Regra
O painel de administração é visível exclusivamente para:

`a.miguel.reis@gmail.com`

## Comportamento
- Admin fica oculto por defeito.
- Só aparece depois de confirmar:
  1. o email autenticado;
  2. `is_app_admin()` no backend.
- Outras contas nunca veem:
  - botão Admin no topo;
  - separador Admin no menu inferior;
  - botão Administração no Perfil.

## Níveis
Foi retirada da interface a opção de promover outros utilizadores para `Administrador`.

Continuam disponíveis:
- Novato
- Explorador
- Guia
- Especialista
- Embaixador
- Editor de confiança

## Backend
Foi confirmado que atualmente `private.app_admins` contém apenas a conta proprietária, com papel `owner`.
