# Bomba Certa v7.4 — utilizador pode alterar o próprio nome

## Erro encontrado
O botão `Alterar nome` existia visualmente, mas não tinha qualquer evento JavaScript associado.
O mesmo acontecia com o botão `Cancelar`.

A função backend já existia e estava correta:
`public.update_my_display_name(p_name text)`

Foi confirmado que:
- é `SECURITY DEFINER`;
- utilizadores autenticados têm permissão de `EXECUTE`.

## Correção
Agora:
1. O utilizador abre `Perfil`.
2. Carrega em `✏️ Alterar nome`.
3. Surge o campo com o nome atual já preenchido.
4. Escreve o novo nome.
5. Carrega em `Guardar nome` ou Enter.
6. O nome é gravado através de `update_my_display_name`.
7. O perfil, cabeçalho e ranking são atualizados.
8. `Cancelar` ou Escape fecha a edição sem alterar nada.

Nenhuma conta ou dado existente foi alterado.
