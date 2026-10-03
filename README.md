# Bomba Certa v6.7 — registo estável sem invalidar contas existentes

## Arquitetura
As contas existentes não foram alteradas nem recriadas.

Para novas contas:
- o utilizador escolhe `username`;
- escolhe a palavra-passe;
- indica um email de recuperação;
- o username é a identidade de acesso;
- o email de recuperação é guardado separadamente da identidade interna do Supabase.

## Compatibilidade
As contas antigas continuam a entrar:
- com o respetivo username;
- ou com o email já associado, quando aplicável.

As novas contas entram:
- com username;
- e o backend também consegue resolver o email de recuperação para a conta correspondente.

## Registo
O backend `public-register` está na versão 5.
O backend `public-login` está na versão 6.

Depois do registo:
`✓ Conta criada com sucesso. A entrar automaticamente na sua conta…`

Se a entrada automática falhar por qualquer motivo, a aplicação não diz que o registo falhou:
- muda para o ecrã de login;
- preenche o username;
- informa claramente que a conta foi criada;
- pede apenas a palavra-passe para entrar.

## Dados existentes
Foi criada uma tabela privada de contactos de recuperação e as contas já existentes foram preenchidas automaticamente com os respetivos emails atuais.
