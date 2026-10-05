# Bomba Certa v11.1 — Média Nacional Inteligente

## Interface mais discreta
O bloco grande foi substituído por uma linha compacta:

`Média PT 2,221 €/L · Subida provável · conf. 74%`

Ao tocar na linha são mostrados os três cenários:
- subir;
- manter;
- descer.

## Mais robusta
A leitura usa três níveis:
1. consulta em tempo real da Edge Function DGEG;
2. último valor oficial bem-sucedido guardado localmente;
3. snapshot oficial DGEG de 24/09/2026 como fallback, claramente identificado como “último oficial”.

A aplicação nunca inventa um preço atual.

## Tendência
A estimativa pondera:
- variações dos últimos dias;
- maior peso nos dias recentes;
- volatilidade;
- consistência da direção;
- nível de confiança.

Não é uma previsão oficial da DGEG.
