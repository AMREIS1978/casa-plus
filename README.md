# Bomba Certa v5.2 — palavras-passe

## Recuperação no login
Foi acrescentado:
`Esqueci-me da palavra-passe`

O utilizador introduz o email e recebe o link oficial do Supabase Auth para definir uma nova palavra-passe.

## Alterar palavra-passe no perfil
Cada utilizador autenticado pode agora:
1. abrir Perfil;
2. carregar em `Alterar palavra-passe`;
3. introduzir a palavra-passe atual;
4. introduzir e repetir a nova palavra-passe;
5. guardar.

A app volta a autenticar a palavra-passe atual antes de permitir a alteração.

## Recuperação
Quando o utilizador abre o link de recuperação recebido por email, a aplicação abre diretamente a janela para escolher uma nova palavra-passe e entra depois da alteração.

## Segurança
As palavras-passe nunca são guardadas no HTML, JavaScript, localStorage ou tabelas públicas.
