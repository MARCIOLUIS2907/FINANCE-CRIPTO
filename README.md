# FINANCE-CRIPTO

Painel de controle de operações de Bitcoin: saldo, custo médio, FIFO, lucro realizado, gráficos e importação.

Exportado do Perchance (Crypto Trade Dashboard — Bitcoin).

## Uso

- Abra `index.html` no navegador, ou publique com GitHub Pages (Settings → Pages → Deploy from branch → `main` / root).
- Nenhum build necessário — HTML + CSS + JS puro, CDNs carregados sob demanda:
  Chart.js, SheetJS, Tesseract.js, html2canvas.

## Funcionalidades

- `main.pjs` — só `$meta` (título/descrição/tags). O app é 100% dirigido pelo HTML/JS.
- `index.html` — app completo: CSS premium dark (preto/dourado/verde/vermelho),
- KPIs: card POSIÇÃO TOTAL em destaque (valor em R$ = saldo BTC total × cotação,
- Motor `calcular()` idêntico ao `src/lib/trade.ts` original: custo médio ponderado
- 4 operações iniciais com os totais conferidos (saldo 0,00225874437 BTC,
- Cotação Binance BTC/BRL ao vivo (30s, com cache) + campo manual que prevalece;
- Abas Resumo / Operações (filtros: local, tipo, origem da compra, destino da
- Registrar operação (nova + edição, corretora padrão/outra, origem/destino,
- Transferência entre corretoras/wallets: tipo TRANSFERÊNCIA (origem → destino,
- Importar CSV/XLSX (SheetJS via CDN, lazy; CSV parse próprio de fallback; prévia
- Importar por imagem (compressão + Tesseract.js OCR via CDN, lazy; heurística
- Exportar CSV, backup/restauração JSON (inclui saldos iniciais), voltar às 4 iniciais; persistência em
- Saldo inicial / ajuste por corretora (Configurações): corrige o caso de BTC que já
- Aba Relatórios: resultado realizado por mês (vendas, custo, lucro e acumulado —
- Imprimir/PDF (`window.print`, CSS A4 paisagem, controles ocultos) e Capturar PNG
- Gráficos com Chart.js via CDN (lazy, só ao abrir a aba): saldo BTC, cotação x
- pt-BR, responsivo (testado 390px e 1920px), print CSS dedicado.
- Chart.js 4.4.7 (jsdelivr), SheetJS 0.20.3 (cdn.sheetjs.com),
- Todo o estado vive no `<script>` do `index.html` (seções: engine, state,
- Cuidado com a engine Perchance: colchetes `[…]` em texto/atributos HTML fora de

## Dados

Tudo fica no `localStorage` do navegador (`crypto-trade-99pay-v1`).
Use Backup JSON em Configurações para levar os dados entre aparelhos.
