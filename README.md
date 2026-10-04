# Bomba Certa v9.4 — Comunidade Social

## Layout
A página principal passa a ter uma estrutura inspirada nos feeds sociais modernos:

### Desktop
- coluna esquerda: perfil, atalhos e publicidade;
- coluna central: feed de postos;
- coluna direita: mapa sticky.

### Tablet
- feed + mapa;
- a coluna de atalhos desaparece para libertar espaço.

### Telemóvel
- mapa compacto;
- feed em coluna única;
- navegação inferior permanece disponível.

## Reações
Cada posto passa a permitir uma reação por utilizador:

- 👍 Gosto
- ❤️ Adoro
- 🔥 Bom preço
- 👏 Útil
- 😮 Surpresa

Voltar a tocar na mesma reação remove-a. Escolher outra substitui a anterior.

## Comentários
Utilizadores autenticados podem:
- escrever comentários até 400 caracteres;
- usar emojis rápidos;
- publicar com Enter;
- eliminar os próprios comentários.

Os cartões mostram:
- total de reações;
- emojis mais usados;
- número de comentários.

## Partilha
Cada cartão tem **Partilhar**, usando a partilha nativa do telemóvel quando disponível e copiando o posto/link como fallback.

## Backend Supabase
Foram criadas:
- `fuel_station_reactions`
- `fuel_station_comments`

As tabelas têm RLS ativo e não estão diretamente acessíveis a `anon` ou `authenticated`.

A interação é feita por RPC autenticado:
- `station_social_summary`
- `toggle_station_reaction`
- `station_social_comments`
- `add_station_comment`
- `delete_station_comment`

Assim a interface não expõe diretamente os dados internos das tabelas sociais.
