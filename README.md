# Bomba Certa v10.8 — Rodapé + Perfil

## Rodapé dinâmico
A barra “Comunidade em direto” passa a ocupar **100% da largura do ecrã**, sem margens laterais.

- alinhamento vertical centrado;
- etiqueta e ticker na mesma linha;
- largura `100vw`;
- sem cantos arredondados laterais;
- adaptação específica para telemóvel;
- mantém-se fixa acima da barra de navegação.

## Perfil
Foram acrescentadas duas ações:

### Sair
Termina a sessão diretamente a partir do Perfil.

### Apagar perfil
Abre uma confirmação explícita e exige escrever `APAGAR`.

A eliminação real é feita no backend pela Edge Function:
`delete-my-account`

A conta proprietária/admin fica protegida contra autoeliminação.

A eliminação remove a conta Auth e os dados associados por cascata, e tenta remover também a fotografia do bucket `avatars`.
