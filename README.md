# CASA+ v0.3 — OCR + dados reais

Versão ligada ao Supabase real `casa-plus`.

## Novo nesta versão
- upload por ficheiro ou fotografia da câmara;
- OCR gratuito executado no navegador com Tesseract.js;
- leitura de imagens e PDFs (até 3 páginas);
- deteção de entidade, NIF, data, total e linhas de produtos;
- ecrã de revisão antes de guardar;
- criação automática de entidades e produtos;
- histórico de preços por produto;
- criação automática da despesa associada à fatura;
- categorização básica por tipo de entidade;
- gráficos reais de despesas por categoria e evolução de 6 meses;
- assistente rápido baseado apenas nos dados da conta;
- tudo continua a 0 enquanto não existirem dados reais.

## Privacidade
Os documentos são guardados no bucket privado `invoices` do Supabase.
A leitura OCR desta versão é feita no próprio navegador; não é necessário serviço OCR pago.

## Deploy
Branch: `main`
Hostinger: auto-deploy ativo.
