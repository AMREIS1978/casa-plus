# CASA+ v0.4 — stock, baixas, receitas e gestão de faturas

Versão ligada ao Supabase real `casa-plus`.

## Novo nesta versão
- botão explícito **Dinheiro que entra** para receitas;
- registo manual de receitas e despesas;
- apagar faturas diretamente na lista;
- ao apagar uma fatura, é removida também a despesa criada automaticamente;
- tentativa de remoção do ficheiro original do bucket privado;
- compras lidas por fatura passam a aumentar o stock;
- novo histórico de movimentos de stock;
- **Dar baixa** de produtos com quantidade e motivo;
- baixa rápida `−1`;
- validação para impedir stock negativo;
- indicador de stock mínimo;
- mantém OCR, gráficos, histórico de preços e dados reais da v0.3.

## Regra de dados
Tudo começa a zero e só aparecem valores efetivamente registados.

## Deploy
Substituir `index.html` e `README.md` na branch `main`.
O Hostinger está configurado com implementação automática.
