# Bomba Certa v9.7 — Interações estilo Facebook

## Correção funcional
Os botões de Gosto, Comentário e Partilha não respondiam corretamente porque a chave do posto era injetada diretamente nos atributos `onclick` com aspas incompatíveis.

Foi substituída por uma chave codificada segura (`encodeURIComponent`) e todos os handlers descodificam a chave antes de agir.

## Três botões à esquerda
Tal como no exemplo:
- 👍 Reagir
- 💬 Comentar
- ↗ Partilhar

Ficam compactos e alinhados à esquerda.

## Reações
Ao clicar em Gosto abre uma barra flutuante com:
- 👍 Gosto
- ❤️ Adoro
- 🥰 Carinho
- 😆 Riso
- 😮 Surpresa
- 😢 Triste
- 😡 Zangado

A reação escolhida substitui o ícone de Gosto. Repetir a mesma reação remove-a.

## Comentários
O botão abre os comentários do posto e permite:
- escrever;
- inserir emojis;
- publicar com Enter;
- eliminar os próprios comentários.

## Partilha
Usa a partilha nativa do dispositivo quando disponível. Em PC copia o posto e o link para a área de transferência como fallback.

## Backend
O backend Supabase foi atualizado para aceitar as sete reações acima. As RPCs continuam exclusivas para utilizadores autenticados.
