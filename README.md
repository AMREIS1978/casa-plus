# Bomba Certa v3.7 — gestão completa de utilizadores

## Criar utilizadores
Na secção Administração passa a ser possível criar novas contas diretamente com:
- email;
- palavra-passe;
- nível inicial.

## Níveis disponíveis
- Novato
- Explorador
- Guia
- Especialista
- Embaixador
- Editor de confiança
- Administrador

## Alterar níveis
O administrador pode também alterar o nível de qualquer utilizador já existente.

Ao atribuir um nível, o backend ajusta automaticamente a reputação mínima correspondente.

## Segurança
A criação de utilizadores é feita numa Supabase Edge Function protegida por JWT e verificação de administrador.

A `service_role` é usada apenas no backend da Edge Function e nunca aparece no HTML público.

## Administradores
Um utilizador com nível Administrador:
- passa a integrar a lista privada de administradores;
- tem acesso à Administração;
- mantém as permissões administrativas já definidas.

A última conta administradora continua protegida contra remoção acidental.
