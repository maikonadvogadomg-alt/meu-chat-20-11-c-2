# 🧬 Receita para recriar: Meu Chat

_Gerada sem IA, lendo 70 arquivo(s). Serve para remontar este app como HTML modular — com qualquer IA, um arquivo por vez._

## 1. O que é

- **Nome:** Meu Chat
- **Partes de código:** 57 (16 tela, 40 logica, 0 servidor, 0 dados, 1 estilo)
- **Tem servidor (rotas /api):** não — dá para ser só HTML
- **Peças de fora (bibliotecas):** nenhuma

## 2. Estrutura modular proposta

```
index.html            ← a página; chama os módulos NA ORDEM
css/app.css           ← o visual
js/00-core.js         ← a "locomotiva": cria window.APP (registrar, guardar, avisar)
js/10-base.js         ← Meu Chat — 00-base.js: peças comuns (MC) (era js/00-base.js)
js/15-banco.js        ← Meu Chat — 10-banco.js: onde tudo fica guardado (IndexedDB do aparelho (era js/10-banco.js)
js/20-online.js       ← Meu Chat — 11-online.js · ☁️ MODO ONLINE (IGUAL À REPLIT) (19/11) Ante (era js/11-online.js)
js/25-nuvem.js        ← Meu Chat — 12-nuvem.js · ☁️ NUVEM (Supabase) — 17/11 - O chat continua (era js/12-nuvem.js)
js/30-entrada.js      ← Meu Chat — 14-entrada.js · 🔑 TELA DE LOGIN NA ENTRADA (17/11) Igual à (era js/14-entrada.js)
js/35-provedores.js   ← Meu Chat — 20-provedores.js: conversar com as IAs (Gemini, Groq, OpenR (era js/20-provedores.js)
js/40-memoria.js      ← Meu Chat — 30-memoria.js: 🧠 a memória que vai junto em TODA conversa. (era js/30-memoria.js)
js/45-contextos.js    ← Meu Chat — 33-contextos.js: 📌 CONTEXTOS — "cartões" de assunto que vo (era js/33-contextos.js)
js/50-guia.js         ← 🧭 Painel do Guia (16/11): o que é cada app do Maikon, a versão atual  (era js/34-guia.js)
js/55-jeito.js        ← Meu Chat — 35-jeito.js: 🎭 O JEITO DE CADA IA. Para não ter "mudança d (era js/35-jeito.js)
js/60-gasto.js        ← Meu Chat — 36-gasto.js · 💰 QUANTO GASTOU (17/11) Igual ao da Monica:  (era js/36-gasto.js)
js/65-arquivos.js     ← Meu Chat — 37-arquivos.js · 📎 ARQUIVOS, 📦 ZIP e 🔤 ACENTOS (17/11) - (era js/37-arquivos.js)
js/70-codigos.js      ← Meu Chat — 38-codigos.js · 🧪 MEUS CÓDIGOS (17/11) Igual ao playground (era js/38-codigos.js)
js/75-qr.js           ← Meu Chat — 39-qr.js · 🔳 LER QR CODE (17/11) Aponta a câmera (ou escol (era js/39-qr.js)
js/80-voz.js          ← Meu Chat — 40-voz.js: 🎤 falar (ditado) e 🔊 ouvir a resposta. 🔊 DOIS (era js/40-voz.js)
js/85-pronto.js       ← Meu Chat — 41-pronto.js · 🔔 AVISO DE "RESPOSTA PRONTA" (18/11) Para o (era js/41-pronto.js)
js/90-testar.js       ← Meu Chat — 42-testar.js · 🧪 TESTAR O CÓDIGO AQUI DENTRO (a "sandbox") (era js/42-testar.js)
js/91-links.js        ← Meu Chat — 43-links.js · 🔗 LINKS E NAVEGADOR INTERNO (18/11) Um "cola (era js/43-links.js)
js/92-docs.js         ← Meu Chat — 44-docs.js · 📄 DOCUMENTAÇÃO DOS PROJETOS (18/11) Cada proj (era js/44-docs.js)
js/93-mesa.js         ← Meu Chat — 45-mesa.js · 🧰 MESA DO LADO (18/11) — para tela grande (co (era js/45-mesa.js)
js/94-internet.js     ← Meu Chat — 50-internet.js: 🌐 pesquisar e 🔗 ler links. - Gemini e Cla (era js/50-internet.js)
js/95-previa.js       ← Meu Chat — 60-previa.js: 👁 ver o código funcionando, na hora. - HTML: (era js/60-previa.js)
js/96-texto.js        ← Meu Chat — 70-texto.js: mostra a resposta da IA bonitinha (negrito, li (era js/70-texto.js)
js/97-chat.js         ← Meu Chat — 80-chat.js: a conversa (mensagens, fotos, mandar, parar, li (era js/80-chat.js)
js/98-config.js       ← Meu Chat — 85-config.js: ⚙️ chaves das IAs, modelo, busca, voz, instru (era js/85-config.js)
js/98-cofre.js        ← Meu Chat — 87-cofre.js: 🔐 Cofre de chaves. Mostra cada chave guardada (era js/87-cofre.js)
js/98-backup.js       ← Meu Chat — 90-backup.js: 💾 backup de tudo (conversas + memória + ajus (era js/90-backup.js)
js/98-restaurar.js    ← Meu Chat — 91-restaurar.js · ♻️ RESTAURAR QUALQUER BACKUP (18/11) O ⤒  (era js/91-restaurar.js)
js/98-ponte-lab.js    ← 🔬 Ponte com o Laboratório: quando o Meu Chat está DENTRO do Laboratór (era js/95-ponte-lab.js)
js/98-janela-pc.js    ← 🖥 JANELA DO PC (18/11) — igual ao Mini SK para PC: um botão para a ja (era js/janela-pc.js)
js/98-cofre-arquivo.js← 🔐 Arquivo de chaves do Maikon — o MESMO formato no Mini SK, no Meu Ch (era js/lib/cofre-arquivo.js)
js/98-ferramentas-lista.js← lista das ferramentas sem IA (20/11) — usada pela 🧰 Mesa (era js/lib/ferramentas-lista.js)
js/98-guia-maikon.js  ← 🧭 Guia das ferramentas do Maikon — o MESMO texto em todos os apps (Mi (era js/lib/guia-maikon.js)
js/98-guia-versoes.js ← 🧭 Guia das VERSÕES — o que é cada app do Maikon, qual a versão atual, (era js/lib/guia-versoes.js)
js/98-nuvem-neon.js   ← 🐘 Nuvem pelo NEON (17/11) — usada pelo Meu Chat e pelo SK Jurídico HT (era js/lib/nuvem-neon.js)
js/98-playground-replit.js← logica (era js/lib/playground-replit.js)
js/98-reconhecer.js   ← ♻️ RECONHECER (18/11) — a mesma peça no Meu Chat, no SK Jurídico HTML  (era js/lib/reconhecer.js)
js/98-nuvem-embutida.js← ☁️ SUPABASE EMBUTIDO (17/11) Estas duas informações são PÚBLICAS de pr (era js/nuvem-embutida.js)
js/98-voz-francisco.js← !/usr/bin/env python3 -*- coding: utf-8 -*- (era voz-francisco.py)
js/98-analisador-v2.js← Analisador Local de Projetos — V2 — Analisador Local de Projetos — V2 (era ferramentas/analisador-v2.html)
js/98-analisador.js   ← Analisador de Projetos — 🔍 Analisador (era ferramentas/analisador.html)
js/98-caca-sql.js     ← 🔍 Caça Esquema SQL — 🔍 Caça Esquema SQL (era ferramentas/caca-sql.html)
js/98-cofre-config.js ← ⚖️ Cofre de Configurações — 🔐 Cofre de Configurações (era ferramentas/cofre-config.html)
js/98-colecionador-codigo.js← Colecionador de Código — 📦 Colecionador de Código (era ferramentas/colecionador-codigo.html)
js/98-comandos-termux.js← 📦 Banco de Comandos Termux — 📦 Banco de Comandos Termux (era ferramentas/comandos-termux.html)
js/98-conversor-imagem.js← Conversor de Imagem Econômico — 🖼️ Conversor de Imagem Econômico (era ferramentas/conversor-imagem.html)
js/98-detector-api.js ← Detector e Corretor de API — 🔍 Detector de Problemas de API (era ferramentas/detector-api.html)
js/98-divisor-html.js ← Divisor de HTML — ✂️ Divisor de HTML Gigante (era ferramentas/divisor-html.html)
js/98-juntador.js     ← Juntador de Projetos HTML — 🔧 Juntador de Projetos HTML (era ferramentas/juntador.html)
js/98-leitor-universal.js← 📂 Leitor Universal de Arquivos — Leitor Universal de Arquivos (era ferramentas/leitor-universal.html)
js/98-monica-guia.js  ← API Monica — Guia Visual — 🤖 API Monica — Guia Visual (era ferramentas/monica-guia.html)
js/98-monica-passo.js ← Guia Monica API - Passo a Passo — 🔑 Guia Monica API (era ferramentas/monica-passo.html)
js/98-montador-modulos.js← 🧩 Montador de Módulos — PWA Jurídico — 🧩 Montador de Módulos PWA JUR (era ferramentas/montador-modulos.html)
js/98-procurar-substituir.js← Procurar e Substituir — 🔍 Procurar e Substituir (era ferramentas/procurar-substituir.html)
js/98-inicio.js       ← Meu Chat (era index.html)
js/99-app.js          ← o último: monta a tela com o que embarcou
```

## 3. As partes, uma por uma

| # | Era | Vira | Tipo | O que faz | Usa |
|---|---|---|---|---|---|
| 1 | `js/00-base.js` | `js/10-base.js` | logica | Meu Chat — 00-base.js: peças comuns (MC) | — |
| 2 | `js/10-banco.js` | `js/15-banco.js` | logica | Meu Chat — 10-banco.js: onde tudo fica guardado (IndexedDB do aparelho — não some ao fecha | — |
| 3 | `js/11-online.js` | `js/20-online.js` | logica | Meu Chat — 11-online.js · ☁️ MODO ONLINE (IGUAL À REPLIT) (19/11) Antes: cada aparelho gua | — |
| 4 | `js/12-nuvem.js` | `js/25-nuvem.js` | logica | Meu Chat — 12-nuvem.js · ☁️ NUVEM (Supabase) — 17/11 - O chat continua funcionando SEM int | — |
| 5 | `js/14-entrada.js` | `js/30-entrada.js` | logica | Meu Chat — 14-entrada.js · 🔑 TELA DE LOGIN NA ENTRADA (17/11) Igual à Replit: abriu o Meu | — |
| 6 | `js/20-provedores.js` | `js/35-provedores.js` | logica | Meu Chat — 20-provedores.js: conversar com as IAs (Gemini, Groq, OpenRouter, OpenAI, DeepS | — |
| 7 | `js/30-memoria.js` | `js/40-memoria.js` | logica | Meu Chat — 30-memoria.js: 🧠 a memória que vai junto em TODA conversa. A IA guarda sozinha | — |
| 8 | `js/33-contextos.js` | `js/45-contextos.js` | logica | Meu Chat — 33-contextos.js: 📌 CONTEXTOS — "cartões" de assunto que você LIGA e DESLIGA. D | — |
| 9 | `js/34-guia.js` | `js/50-guia.js` | logica | 🧭 Painel do Guia (16/11): o que é cada app do Maikon, a versão atual e COMO USAR, passo a | — |
| 10 | `js/35-jeito.js` | `js/55-jeito.js` | logica | Meu Chat — 35-jeito.js: 🎭 O JEITO DE CADA IA. Para não ter "mudança drástica" quando troc | — |
| 11 | `js/36-gasto.js` | `js/60-gasto.js` | logica | Meu Chat — 36-gasto.js · 💰 QUANTO GASTOU (17/11) Igual ao da Monica: embaixo de cada resp | — |
| 12 | `js/37-arquivos.js` | `js/65-arquivos.js` | logica | Meu Chat — 37-arquivos.js · 📎 ARQUIVOS, 📦 ZIP e 🔤 ACENTOS (17/11) - 🔤 Lê qualquer text | — |
| 13 | `js/38-codigos.js` | `js/70-codigos.js` | logica | Meu Chat — 38-codigos.js · 🧪 MEUS CÓDIGOS (17/11) Igual ao playground do jurídico origina | — |
| 14 | `js/39-qr.js` | `js/75-qr.js` | logica | Meu Chat — 39-qr.js · 🔳 LER QR CODE (17/11) Aponta a câmera (ou escolhe um print) e o tex | — |
| 15 | `js/40-voz.js` | `js/80-voz.js` | logica | Meu Chat — 40-voz.js: 🎤 falar (ditado) e 🔊 ouvir a resposta. 🔊 DOIS "motores" de voz (⚙ | — |
| 16 | `js/41-pronto.js` | `js/85-pronto.js` | logica | Meu Chat — 41-pronto.js · 🔔 AVISO DE "RESPOSTA PRONTA" (18/11) Para o Ollama (ou qualquer | — |
| 17 | `js/42-testar.js` | `js/90-testar.js` | logica | Meu Chat — 42-testar.js · 🧪 TESTAR O CÓDIGO AQUI DENTRO (a "sandbox") (18/11) Sandbox = u | — |
| 18 | `js/43-links.js` | `js/91-links.js` | logica | Meu Chat — 43-links.js · 🔗 LINKS E NAVEGADOR INTERNO (18/11) Um "colador de links" aqui d | — |
| 19 | `js/44-docs.js` | `js/92-docs.js` | logica | Meu Chat — 44-docs.js · 📄 DOCUMENTAÇÃO DOS PROJETOS (18/11) Cada projeto tem um README.md | — |
| 20 | `js/45-mesa.js` | `js/93-mesa.js` | logica | Meu Chat — 45-mesa.js · 🧰 MESA DO LADO (18/11) — para tela grande (computador, .exe, tabl | — |
| 21 | `js/50-internet.js` | `js/94-internet.js` | logica | Meu Chat — 50-internet.js: 🌐 pesquisar e 🔗 ler links. - Gemini e Claude pesquisam sozinh | — |
| 22 | `js/60-previa.js` | `js/95-previa.js` | logica | Meu Chat — 60-previa.js: 👁 ver o código funcionando, na hora. - HTML: abre a página como  | — |
| 23 | `js/70-texto.js` | `js/96-texto.js` | logica | Meu Chat — 70-texto.js: mostra a resposta da IA bonitinha (negrito, listas, links, blocos  | — |
| 24 | `js/80-chat.js` | `js/97-chat.js` | logica | Meu Chat — 80-chat.js: a conversa (mensagens, fotos, mandar, parar, lista de conversas). C | — |
| 25 | `js/85-config.js` | `js/98-config.js` | logica | Meu Chat — 85-config.js: ⚙️ chaves das IAs, modelo, busca, voz, instruções, tema | — |
| 26 | `js/87-cofre.js` | `js/98-cofre.js` | logica | Meu Chat — 87-cofre.js: 🔐 Cofre de chaves. Mostra cada chave guardada (👁 ver, 📋 copiar) | — |
| 27 | `js/90-backup.js` | `js/98-backup.js` | logica | Meu Chat — 90-backup.js: 💾 backup de tudo (conversas + memória + ajustes) e restaurar SEM | — |
| 28 | `js/91-restaurar.js` | `js/98-restaurar.js` | logica | Meu Chat — 91-restaurar.js · ♻️ RESTAURAR QUALQUER BACKUP (18/11) O ⤒ Restaurar agora ente | — |
| 29 | `js/95-ponte-lab.js` | `js/98-ponte-lab.js` | logica | 🔬 Ponte com o Laboratório: quando o Meu Chat está DENTRO do Laboratório (aba 🤖 IA), o La | — |
| 30 | `js/99-app.js` | css/app.css | logica | Meu Chat — 99-app.js: liga tudo quando abre | — |
| 31 | `js/janela-pc.js` | `js/98-janela-pc.js` | logica | 🖥 JANELA DO PC (18/11) — igual ao Mini SK para PC: um botão para a janela ir de 📱 cara d | — |
| 32 | `js/lib/cofre-arquivo.js` | `js/98-cofre-arquivo.js` | logica | 🔐 Arquivo de chaves do Maikon — o MESMO formato no Mini SK, no Meu Chat e no que vier dep | — |
| 33 | `js/lib/ferramentas-lista.js` | `js/98-ferramentas-lista.js` | logica | lista das ferramentas sem IA (20/11) — usada pela 🧰 Mesa | — |
| 34 | `js/lib/guia-maikon.js` | `js/98-guia-maikon.js` | logica | 🧭 Guia das ferramentas do Maikon — o MESMO texto em todos os apps (Mini SK, Meu Chat…). A | — |
| 35 | `js/lib/guia-versoes.js` | `js/98-guia-versoes.js` | logica | 🧭 Guia das VERSÕES — o que é cada app do Maikon, qual a versão atual, e COMO USAR (passo  | — |
| 36 | `js/lib/nuvem-neon.js` | `js/98-nuvem-neon.js` | logica | 🐘 Nuvem pelo NEON (17/11) — usada pelo Meu Chat e pelo SK Jurídico HTML. Você cola o ende | — |
| 37 | `js/lib/playground-replit.js` | `js/98-playground-replit.js` | logica | ESC, App, completo, limparDoc | — |
| 38 | `js/lib/reconhecer.js` | `js/98-reconhecer.js` | logica | ♻️ RECONHECER (18/11) — a mesma peça no Meu Chat, no SK Jurídico HTML e no 🗄 Banco. Receb | — |
| 39 | `js/nuvem-embutida.js` | `js/98-nuvem-embutida.js` | logica | ☁️ SUPABASE EMBUTIDO (17/11) Estas duas informações são PÚBLICAS de propósito (todo site q | — |
| 40 | `voz-francisco.py` | `js/98-voz-francisco.js` | logica | !/usr/bin/env python3 -*- coding: utf-8 -*- | — |
| 41 | `ferramentas/analisador-v2.html` | `js/98-analisador-v2.js` | tela | Analisador Local de Projetos — V2 — Analisador Local de Projetos — V2 | — |
| 42 | `ferramentas/analisador.html` | `js/98-analisador.js` | tela | Analisador de Projetos — 🔍 Analisador | — |
| 43 | `ferramentas/caca-sql.html` | `js/98-caca-sql.js` | tela | 🔍 Caça Esquema SQL — 🔍 Caça Esquema SQL | — |
| 44 | `ferramentas/cofre-config.html` | `js/98-cofre-config.js` | tela | ⚖️ Cofre de Configurações — 🔐 Cofre de Configurações | — |
| 45 | `ferramentas/colecionador-codigo.html` | `js/98-colecionador-codigo.js` | tela | Colecionador de Código — 📦 Colecionador de Código | — |
| 46 | `ferramentas/comandos-termux.html` | `js/98-comandos-termux.js` | tela | 📦 Banco de Comandos Termux — 📦 Banco de Comandos Termux | — |
| 47 | `ferramentas/conversor-imagem.html` | `js/98-conversor-imagem.js` | tela | Conversor de Imagem Econômico — 🖼️ Conversor de Imagem Econômico | — |
| 48 | `ferramentas/detector-api.html` | `js/98-detector-api.js` | tela | Detector e Corretor de API — 🔍 Detector de Problemas de API | — |
| 49 | `ferramentas/divisor-html.html` | `js/98-divisor-html.js` | tela | Divisor de HTML — ✂️ Divisor de HTML Gigante | — |
| 50 | `ferramentas/juntador.html` | `js/98-juntador.js` | tela | Juntador de Projetos HTML — 🔧 Juntador de Projetos HTML | — |
| 51 | `ferramentas/leitor-universal.html` | `js/98-leitor-universal.js` | tela | 📂 Leitor Universal de Arquivos — Leitor Universal de Arquivos | — |
| 52 | `ferramentas/monica-guia.html` | `js/98-monica-guia.js` | tela | API Monica — Guia Visual — 🤖 API Monica — Guia Visual | — |
| 53 | `ferramentas/monica-passo.html` | `js/98-monica-passo.js` | tela | Guia Monica API - Passo a Passo — 🔑 Guia Monica API | — |
| 54 | `ferramentas/montador-modulos.html` | `js/98-montador-modulos.js` | tela | 🧩 Montador de Módulos — PWA Jurídico — 🧩 Montador de Módulos PWA JURÍDICO — MAIKON CALDE | — |
| 55 | `ferramentas/procurar-substituir.html` | `js/98-procurar-substituir.js` | tela | Procurar e Substituir — 🔍 Procurar e Substituir | — |
| 56 | `css/app.css` | css/app.css | estilo | — | — |
| 57 | `index.html` | `js/98-inicio.js` | tela | Meu Chat | manifest.json, icon-192.png, app.css, 00-base.js |

## 4. Montar passo a passo (cada bloco é um pedido pronto: 📋 Copiar → colar na IA)

### Passo 0 — combinar as regras com a IA

```text
Vamos recriar o app "Meu Chat" como HTML MODULAR, que abre pelo index.html, sem servidor e sem nada da Replit.
Regras: (1) index.html chama os arquivos js/ na ordem, antes do </body>; (2) js/00-core.js cria window.APP com APP.registrar(modulo), APP.guardar(chave, valor) em IndexedDB/localStorage e APP.avisar(texto); (3) cada arquivo js/NN-nome.js cuida de UM assunto, começa com (function (APP) { e termina com })(window.APP); (4) js/99-app.js vem por último e monta a tela com os módulos registrados; (5) textos em português do Brasil.
Vou pedir UM arquivo por vez. Responda só com o arquivo completo, sem cortar nada. Primeiro: crie index.html, css/app.css e js/00-core.js.
```

### Passo 1 — `js/10-base.js` (era `js/00-base.js`, 43 linhas)

```text
Crie js/10-base.js. Ele faz: Meu Chat — 00-base.js: peças comuns (MC).
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 2 — `js/15-banco.js` (era `js/10-banco.js`, 26 linhas)

```text
Crie js/15-banco.js. Ele faz: Meu Chat — 10-banco.js: onde tudo fica guardado (IndexedDB do aparelho — não some ao fechar).
No app original ele tinha estas funções/partes: abrir, req, loja.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 3 — `js/20-online.js` (era `js/11-online.js`, 104 linhas)

```text
Crie js/20-online.js. Ele faz: Meu Chat — 11-online.js · ☁️ MODO ONLINE (IGUAL À REPLIT) (19/11) Antes: cada aparelho guardava uma CÓPIA de todas as conversas (o app crescia e a nuvem gastava baixando tudo). AGORA, com a conta do Supabase ligada: • a lista de conversas vem da nuvem só com o NOME (leve);.
No app original ele tinha estas funções/partes: temFotos, semFotos, ligado, guardarSemInternet, subirPendentes, liberar, ocupa.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 4 — `js/25-nuvem.js` (era `js/12-nuvem.js`, 320 linhas)

```text
Crie js/25-nuvem.js. Ele faz: Meu Chat — 12-nuvem.js · ☁️ NUVEM (Supabase) — 17/11 - O chat continua funcionando SEM internet: tudo fica no aparelho (IndexedDB). - Com a nuvem ligada, ele COPIA para o Supabase e traz de volta em qualquer aparelho (celular, PC, outro celular) entrando com o mesmo e-mail e senha.
No app original ele tinha estas funções/partes: temEmb, cfg, sessao, ehNeon, neonConn, logado, ligada, auth, traduzir, guardarSessao, token, rest, mod, horaUnica, marcar, ganchos, marcarPrefs, prefsViajam.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 5 — `js/30-entrada.js` (era `js/14-entrada.js`, 84 linhas)

```text
Crie js/30-entrada.js. Ele faz: Meu Chat — 14-entrada.js · 🔑 TELA DE LOGIN NA ENTRADA (17/11) Igual à Replit: abriu o Meu Chat em qualquer lugar (celular, PC, PWA, APK) → e-mail + senha → as conversas, a memória, os códigos guardados E as chaves de IA aparecem. Ninguém cola endereço. 19/11: aparece sempre que você ainda não entrou (sem precisar embutir): na 1ª vez, ⚙ cola a URL e a chave anon do Supabase ali mesmo e 📋 copia o comando que cria a tabela.
No app original ele tinha estas funções/partes: dentroDeOutroApp, precisa, mostrar, msg, recuperacao.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 6 — `js/35-provedores.js` (era `js/20-provedores.js`, 249 linhas)

```text
Crie js/35-provedores.js. Ele faz: Meu Chat — 20-provedores.js: conversar com as IAs (Gemini, Groq, OpenRouter, OpenAI, DeepSeek, Claude). - Várias chaves; quando uma acaba (limite/cota), passa sozinho para a próxima ("revezar"). - Busca a lista de modelos de verdade na hora de testar a chave (nada de nome velho chumbado). - As chaves ficam SÓ neste aparelho.
No app original ele tinha estas funções/partes: detectar, procurarOllama, chaves, salvarChaves, pontoGemini, listarModelos, pontoLivre, geracao, modeloDe, testarChave, erroLegivel, corsAviso, ehLimite, cabAnthropic, lerSSE, estimar, pedir, parcial.
Ele chamava estes endereços: http://127.0.0.1:11434/api/tags. Em HTML, ligue cada um à função equivalente do módulo certo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 7 — `js/40-memoria.js` (era `js/30-memoria.js`, 77 linhas)

```text
Crie js/40-memoria.js. Ele faz: Meu Chat — 30-memoria.js: 🧠 a memória que vai junto em TODA conversa. A IA guarda sozinha o que for importante escrevendo [[lembrar: …]] no fim da resposta (o app tira isso do texto, guarda e mostra "🧠 guardei"). [[esquecer: …]] apaga.
No app original ele tinha estas funções/partes: texto, salvar, lembrar, esquecer, aplicarMarcas, guiaParaPergunta, tamanhoTexto, sistema, abrir.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 8 — `js/45-contextos.js` (era `js/33-contextos.js`, 178 linhas)

```text
Crie js/45-contextos.js. Ele faz: Meu Chat — 33-contextos.js: 📌 CONTEXTOS — "cartões" de assunto que você LIGA e DESLIGA. Diferente da 🧠 memória (que vale para sempre e vai em tudo): um contexto é o resumo de um assunto ou de uma conversa (por exemplo, o que você vinha fazendo com o Claude), para a IA não começar do zero. Ligado = vai junto em toda conversa. Desligado = fica guardado, sem gastar.
No app original ele tinha estas funções/partes: lista, gravar, semear, esconder, tokens, ligados, texto, pintarChip, pintar, novo, clique.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 9 — `js/50-guia.js` (era `js/34-guia.js`, 39 linhas)

```text
Crie js/50-guia.js. Ele faz: 🧭 Painel do Guia (16/11): o que é cada app do Maikon, a versão atual e COMO USAR, passo a passo. 🔊 lê em voz alta (voz Francisco ou a do aparelho) · 🤖 Perguntar: o chat explica aquele app.
No app original ele tinha estas funções/partes: textoDe, pintar, iniciar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 10 — `js/55-jeito.js` (era `js/35-jeito.js`, 56 linhas)

```text
Crie js/55-jeito.js. Ele faz: Meu Chat — 35-jeito.js: 🎭 O JEITO DE CADA IA. Para não ter "mudança drástica" quando troca de IA: um jeito de conversar que vale para TODAS (parceiro, calmo, honesto) e, se quiser, um jeito só de uma (ex.: o Perplexity como pesquisador jurídico que sempre traz as fontes). Tudo editável em ⚙️ → 🎭 Jeito de cada IA.
No app original ele tinha estas funções/partes: geral, deUma, texto, pintar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 11 — `js/60-gasto.js` (era `js/36-gasto.js`, 105 linhas)

```text
Crie js/60-gasto.js. Ele faz: Meu Chat — 36-gasto.js · 💰 QUANTO GASTOU (17/11) Igual ao da Monica: embaixo de cada resposta aparece quantos "tokens" foram e quanto custou, e o painel 💰 mostra o gasto de hoje, da semana e do mês, por IA. - "Entrada" = tudo que vai junto na pergunta: regras, memória, guia, contextos e o HISTÓRICO da conversa.
No app original ele tinha estas funções/partes: tabela, dolar, geminiPago, preco, custo, mil, reais, texto, dia, registrar, somar, pintar, linhaT, abrir.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 12 — `js/65-arquivos.js` (era `js/37-arquivos.js`, 100 linhas)

```text
Crie js/65-arquivos.js. Ele faz: Meu Chat — 37-arquivos.js · 📎 ARQUIVOS, 📦 ZIP e 🔤 ACENTOS (17/11) - 🔤 Lê qualquer texto com os acentos certos: tenta UTF-8 e, se não for, Windows-1252/Latin-1 (era o "negócio de UTF-8" que fazia outros sites não lerem o arquivo). - 📦 Projeto .zip: abre AQUI DENTRO, mostra a árvore, deixa ver cada arquivo e você marca.
No app original ele tinha estas funções/partes: lerTexto, textoDoArquivo, tokens, mil, item, abrirZip, abrirRepo, api, raw, janela, conta, pintar.
Ele chamava estes endereços: https://api.github.com/repos/. Em HTML, ligue cada um à função equivalente do módulo certo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 13 — `js/70-codigos.js` (era `js/38-codigos.js`, 71 linhas)

```text
Crie js/70-codigos.js. Ele faz: Meu Chat — 38-codigos.js · 🧪 MEUS CÓDIGOS (17/11) Igual ao playground do jurídico original: cada código que a IA fizer tem o botão 💾 Guardar. Ficam aqui, com nome, e vão para a nuvem (com o login, aparecem em qualquer aparelho). Abrir = abre no ▶ playground (ver funcionando e mexer). Nada some sem você confirmar.
No app original ele tinha estas funções/partes: todos, gravar, tituloDe, igual, guardar, pintar, clique, atualizar, abrir, playground.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 14 — `js/75-qr.js` (era `js/39-qr.js`, 69 linhas)

```text
Crie js/75-qr.js. Ele faz: Meu Chat — 39-qr.js · 🔳 LER QR CODE (17/11) Aponta a câmera (ou escolhe um print) e o texto do QR vai para a caixa de mensagem. Entende os QR em sequência do Colecionador ("1 de 5, 2 de 5…"): junta sozinho, em qualquer ordem.
No app original ele tinha estas funções/partes: carregar, descompactar, detector, parar, entregar, juntar, abrir, laco.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 15 — `js/80-voz.js` (era `js/40-voz.js`, 227 linhas)

```text
Crie js/80-voz.js. Ele faz: Meu Chat — 40-voz.js: 🎤 falar (ditado) e 🔊 ouvir a resposta. 🔊 DOIS "motores" de voz (⚙️ → Voz): - 📱 "Voz do aparelho" (o padrão): funciona com QUALQUER IA (Gemini, Groq, Claude, Ollama…), grátis e sem limite. Você escolhe a voz (as ⭐ são as naturais), a velocidade e o tom.
No app original ele tinha estas funções/partes: podeOuvir, ouvir, parar, marcar, paraFala, pedacos, noPC, motor, temAndroid, temNavegador, natural, vozesAparelho, cfgVoz, falarFrase, enfileirar, verificarFim, pararAparelho, fluxo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 16 — `js/85-pronto.js` (era `js/41-pronto.js`, 57 linhas)

```text
Crie js/85-pronto.js. Ele faz: Meu Chat — 41-pronto.js · 🔔 AVISO DE "RESPOSTA PRONTA" (18/11) Para o Ollama (ou qualquer IA lenta): você manda a pergunta, vai mexer em outra coisa, e quando a resposta termina o celular/PC APITA, VIBRA e mostra uma NOTIFICAÇÃO. 🔆 "Tela acesa": enquanto ela escreve, o aparelho não apaga a tela (assim o Android.
No app original ele tinha estas funções/partes: ligado, telaAcesa, pedirPermissao, apito, comecou, terminou.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 17 — `js/90-testar.js` (era `js/42-testar.js`, 75 linhas)

```text
Crie js/90-testar.js. Ele faz: Meu Chat — 42-testar.js · 🧪 TESTAR O CÓDIGO AQUI DENTRO (a "sandbox") (18/11) Sandbox = uma caixa FECHADA onde o código roda sem mexer em nada seu. - JavaScript: roda num "trabalhador" separado, com tempo máximo de 10 segundos (se travar num laço infinito, ele é desligado). Mostra o console.log e os erros.
No app original ele tinha estas funções/partes: ehJS, ehPy, podeTestar, trabalhadorJS, fmt, trabalhadorPy, rodar, testar, vai.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 18 — `js/91-links.js` (era `js/43-links.js`, 75 linhas)

```text
Crie js/91-links.js. Ele faz: Meu Chat — 43-links.js · 🔗 LINKS E NAVEGADOR INTERNO (18/11) Um "colador de links" aqui dentro, que NÃO gasta nada da IA: - guarde os seus links (versões dos apps, repositórios, sites de tribunal…); - 🌐 Abrir aqui: abre o site numa janela dentro do Meu Chat (alguns sites não deixam: aí use ↗ Abrir fora);.
No app original ele tinha estas funções/partes: todos, salvar, normal, pintar, navegador, atual, trazer, guardar, clique, abrir.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 19 — `js/92-docs.js` (era `js/44-docs.js`, 35 linhas)

```text
Crie js/92-docs.js. Ele faz: Meu Chat — 44-docs.js · 📄 DOCUMENTAÇÃO DOS PROJETOS (18/11) Cada projeto tem um README.md completo (o que é, recursos, onde ficam os dados, regras e o MAPA dos arquivos). Aqui você escolhe um e ele entra na conversa SÓ AGORA — não vai em toda mensagem. Serve para a IA (qualquer uma, inclusive o Claude) entender o projeto sem ler o código inteiro.
No app original ele tinha estas funções/partes: ler, abrir.
Ele chamava estes endereços: docs/. Em HTML, ligue cada um à função equivalente do módulo certo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 20 — `js/93-mesa.js` (era `js/45-mesa.js`, 123 linhas)

```text
Crie js/93-mesa.js. Ele faz: Meu Chat — 45-mesa.js · 🧰 MESA DO LADO (18/11) — para tela grande (computador, .exe, tablet deitado) No celular (20/11) a mesa abre por cima, na tela toda; o playground fica guardado; aba 🧰 com as ferramentas sem IA. O chat fica à esquerda, igual. À direita, uma MESA separada que NÃO gasta nada da IA: ▶ Playground  — o código que a IA fez vai para cá (botão ➡ Mesa nos blocos de código): mexa e veja funcionando.
No app original ele tinha estas funções/partes: LARGA, ligada, montar, guardarAtual, trocarAba, aplicar, cheia, alternar, pintarFerr, rodar, receber, pintarLinks, urlBoa, pintarCodigos, clique.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 21 — `js/94-internet.js` (era `js/50-internet.js`, 58 linhas)

```text
Crie js/94-internet.js. Ele faz: Meu Chat — 50-internet.js: 🌐 pesquisar e 🔗 ler links. - Gemini e Claude pesquisam sozinhos (a busca vem embutida neles). - As outras IAs: usa a SUA chave de busca (Serper, Tavily ou Brave), se tiver, e manda os resultados junto. - Link na mensagem: o app lê a página (pelo leitor r.jina.ai, grátis) e manda o texto para a IA.
No app original ele tinha estas funções/partes: buscar, lerLink, preparar.
Ele chamava estes endereços: https://google.serper.dev/search, https://api.tavily.com/search, https://api.search.brave.com/res/v1/web/search?count=8&country=BR&search_lang=pt-br&q=, https://r.jina.ai/. Em HTML, ligue cada um à função equivalente do módulo certo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 22 — `js/95-previa.js` (era `js/60-previa.js`, 88 linhas)

```text
Crie js/95-previa.js. Ele faz: Meu Chat — 60-previa.js: 👁 ver o código funcionando, na hora. - HTML: abre a página como ela é. - TSX / JSX (React): monta com React + Babel + Tailwind (pela internet) e mostra o componente. Os erros aparecem embaixo, em vermelho.
No app original ele tinha estas funções/partes: paginaHTML, paginaReact, falha, req, App, tipoDe, abrir.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 23 — `js/96-texto.js` (era `js/70-texto.js`, 48 linhas)

```text
Crie js/96-texto.js. Ele faz: Meu Chat — 70-texto.js: mostra a resposta da IA bonitinha (negrito, listas, links, blocos de código com 📋 copiar, ⤓ baixar e 👁 ver funcionando).
No app original ele tinha estas funções/partes: inline, render, ligar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 24 — `js/97-chat.js` (era `js/80-chat.js`, 320 linhas)

```text
Crie js/97-chat.js. Ele faz: Meu Chat — 80-chat.js: a conversa (mensagens, fotos, mandar, parar, lista de conversas). Cada conversa fica guardada no aparelho. Vai para a IA: a memória + as últimas mensagens.
No app original ele tinha estas funções/partes: nova, abrirConversa, guardar, reduzir, tokFoto, anexar, pintarAnexos, carregar, juntarFotos, ocrFotos, htmlMsg, dedup, hora, pintar, mandar, responder, depois, comparar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 25 — `js/98-config.js` (era `js/85-config.js`, 115 linhas)

```text
Crie js/98-config.js. Ele faz: Meu Chat — 85-config.js: ⚙️ chaves das IAs, modelo, busca, voz, instruções, tema.
No app original ele tinha estas funções/partes: opcoesVoz, pintar, clique, mudou, aplicarTema, abrir.
Ele chamava estes endereços: voz-francisco.py. Em HTML, ligue cada um à função equivalente do módulo certo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 26 — `js/98-cofre.js` (era `js/87-cofre.js`, 96 linhas)

```text
Crie js/98-cofre.js. Ele faz: Meu Chat — 87-cofre.js: 🔐 Cofre de chaves. Mostra cada chave guardada (👁 ver, 📋 copiar) e leva SÓ as chaves para outro app/aparelho num arquivo trancado com senha — o mesmo arquivo do Mini SK (js/lib/cofre-arquivo.js).
No app original ele tinha estas funções/partes: todas, pintar, status, conteudo, baixar, trazer, selarTexto, trazerTexto.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 27 — `js/98-backup.js` (era `js/90-backup.js`, 44 linhas)

```text
Crie js/98-backup.js. Ele faz: Meu Chat — 90-backup.js: 💾 backup de tudo (conversas + memória + ajustes) e restaurar SEM APAGAR NADA.
No app original ele tinha estas funções/partes: gerar, baixar, restaurar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 28 — `js/98-restaurar.js` (era `js/91-restaurar.js`, 53 linhas)

```text
Crie js/98-restaurar.js. Ele faz: Meu Chat — 91-restaurar.js · ♻️ RESTAURAR QUALQUER BACKUP (18/11) O ⤒ Restaurar agora entende QUALQUER arquivo dos seus apps: backup do Meu Chat, do SK Jurídico, o ⬇ backup do 🗄 Banco/Neon (tabela mc_itens), o banco antigo do SK Jurídico 1.7… Reconhece sozinho, mostra o que achou, traz o que é do Meu Chat (junta, não apaga).
No app original ele tinha estas funções/partes: ler, trazerMeuChat, janela, abrirArquivo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 29 — `js/98-ponte-lab.js` (era `js/95-ponte-lab.js`, 20 linhas)

```text
Crie js/98-ponte-lab.js. Ele faz: 🔬 Ponte com o Laboratório: quando o Meu Chat está DENTRO do Laboratório (aba 🤖 IA), o Laboratório pode mandar texto para a caixa de escrever (o plano do projeto, a memória, a comparação A × B). Só aceita mensagens da própria página (mesmo endereço).
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 30 — `js/98-janela-pc.js` (era `js/janela-pc.js`, 20 linhas)

```text
Crie js/98-janela-pc.js. Ele faz: 🖥 JANELA DO PC (18/11) — igual ao Mini SK para PC: um botão para a janela ir de 📱 cara de celular → 📟 média → 🖥 tela cheia, e voltar. Só aparece no programa .exe.
No app original ele tinha estas funções/partes: ler, por, botao.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 31 — `js/98-cofre-arquivo.js` (era `js/lib/cofre-arquivo.js`, 61 linhas)

```text
Crie js/98-cofre-arquivo.js. Ele faz: 🔐 Arquivo de chaves do Maikon — o MESMO formato no Mini SK, no Meu Chat e no que vier depois. Guarda SÓ as chaves (IA, GitHub, Expo, pesquisa e "Minhas chaves"), trancadas com uma senha sua (AES-GCM 256 + PBKDF2 com 250 mil voltas — sem a senha, o arquivo não abre). Assim dá para levar as chaves de um app/aparelho para outro sem passar pelo WhatsApp.
No app original ele tinha estas funções/partes: b64, deB64, chaveDaSenha, normal, selar, abrir, contar, mascara.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 32 — `js/98-ferramentas-lista.js` (era `js/lib/ferramentas-lista.js`, 3 linhas)

```text
Crie js/98-ferramentas-lista.js. Ele faz: lista das ferramentas sem IA (20/11) — usada pela 🧰 Mesa.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 33 — `js/98-guia-maikon.js` (era `js/lib/guia-maikon.js`, 118 linhas)

```text
Crie js/98-guia-maikon.js. Ele faz: 🧭 Guia das ferramentas do Maikon — o MESMO texto em todos os apps (Mini SK, Meu Chat…). A IA de cada app lê isto sozinha: assim ela já sabe o que ele tem, para que serve cada coisa, e quando é melhor mandar para outra ferramenta ou "levar para o Claude". Para atualizar: troque este arquivo nos apps (o Claude manda a versão nova junto).
No app original ele tinha estas funções/partes: resumoParaClaude, esconder.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 34 — `js/98-guia-versoes.js` (era `js/lib/guia-versoes.js`, 179 linhas)

```text
Crie js/98-guia-versoes.js. Ele faz: 🧭 Guia das VERSÕES — o que é cada app do Maikon, qual a versão atual, e COMO USAR (passo a passo). Uma fonte só: o painel 🧭 do Meu Chat mostra isto para ele ler, e a IA recebe o mesmo texto (junto do guia-maikon.js) para saber explicar. Atualizado pelo Claude a cada versão nova.
No app original ele tinha estas funções/partes: texto.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 35 — `js/98-nuvem-neon.js` (era `js/lib/nuvem-neon.js`, 75 linhas)

```text
Crie js/98-nuvem-neon.js. Ele faz: 🐘 Nuvem pelo NEON (17/11) — usada pelo Meu Chat e pelo SK Jurídico HTML. Você cola o endereço do banco (a "connection string" postgresql://…) e pronto: o app cria a tabela SOZINHO (não precisa rodar nada em inglês no site do Neon). ⚠ Esse endereço tem a SENHA do banco: fica só no seu aparelho (como uma chave de IA),.
No app original ele tinha estas funções/partes: traduzir, preparar, upsert, listar, conv, consulta.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 36 — `js/98-playground-replit.js` (era `js/lib/playground-replit.js`, 198 linhas)

```text
Crie js/98-playground-replit.js. Ele é uma parte de logica do app.
No app original ele tinha estas funções/partes: ESC, App, completo, limparDoc, detectar, preJSX, docHTML, docReact, documento, doZip, pasta, junta, achar, abrir, aviso, guardarLocal, abas, info.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 37 — `js/98-reconhecer.js` (era `js/lib/reconhecer.js`, 108 linhas)

```text
Crie js/98-reconhecer.js. Ele faz: ♻️ RECONHECER (18/11) — a mesma peça no Meu Chat, no SK Jurídico HTML e no 🗄 Banco. Recebe QUALQUER coisa que veio dos seus apps e diz sozinho O QUE É e PARA ONDE VAI: - backup do Meu Chat (.json) · backup do SK Jurídico HTML / Assistente Jurídico (.json) - o "⬇ backup" do 🗄 Banco (todas as tabelas) ou o próprio banco lido direto (Neon).
No app original ele tinha estas funções/partes: vazio, quando, txtHtml, colunas, parse, deTabelas, detectar, formatoMarkdown.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 38 — `js/98-nuvem-embutida.js` (era `js/nuvem-embutida.js`, 11 linhas)

```text
Crie js/98-nuvem-embutida.js. Ele faz: ☁️ SUPABASE EMBUTIDO (17/11) Estas duas informações são PÚBLICAS de propósito (todo site que usa Supabase tem elas dentro). Quem protege os seus dados é o LOGIN (e-mail e senha) e a regra "cada um vê o seu" da tabela. Com elas aqui dentro, em qualquer aparelho o app abre a tela de login: e-mail + senha e pronto.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 39 — `js/98-voz-francisco.js` (era `voz-francisco.py`, 134 linhas)

```text
Crie js/98-voz-francisco.js. Ele faz: !/usr/bin/env python3 -*- coding: utf-8 -*-.
No app original ele tinha estas funções/partes: _listar, _falar, Voz, _cabecalhos, do_OPTIONS, _json, _pedido, do_GET, do_POST, _tratar, log_message.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 40 — `js/98-analisador-v2.js` (era `ferramentas/analisador-v2.html`, 1480 linhas)

```text
Crie js/98-analisador-v2.js. Ele faz: Analisador Local de Projetos — V2 — Analisador Local de Projetos — V2.
No app original ele tinha estas funções/partes: extension, normalize, setStatus, formatBytes, importFiles, renderFileList, openFile, updateEditorInfo, scheduleSave, saveProject, restoreProject, pasteCode, newFile, downloadCurrent, downloadBlob, createElement, heading, card.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 41 — `js/98-analisador.js` (era `ferramentas/analisador.html`, 1019 linhas)

```text
Crie js/98-analisador.js. Ele faz: Analisador de Projetos — 🔍 Analisador.
No app original ele tinha estas funções/partes: setupEventListeners, mudarPagina, carregarPagina, renderUpload, renderAnalise, renderPreview, renderEstrutura, renderExportar, analisarProjeto, gerarEstrutura, visualizar, remover, copiarEstrutura, exportarZip, exportarJSON, abrirModalNomeProjeto, confirmarNomeProjeto, abrirModal.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 42 — `js/98-caca-sql.js` (era `ferramentas/caca-sql.html`, 335 linhas)

```text
Crie js/98-caca-sql.js. Ele faz: 🔍 Caça Esquema SQL — 🔍 Caça Esquema SQL.
No app original ele tinha estas funções/partes: processarZip, criarBloco, copiar, escapar, escaparHTML, mostrarStatus.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 43 — `js/98-cofre-config.js` (era `ferramentas/cofre-config.html`, 634 linhas)

```text
Crie js/98-cofre-config.js. Ele faz: ⚖️ Cofre de Configurações — 🔐 Cofre de Configurações.
No app original ele tinha estas funções/partes: init, salvar, render, renderTabs, renderItems, renderStats, setAba, salvarAba, deletarAba, openModal, closeModal, preencherSelectAbas, salvarItem, editarItem, deletarItem, toggleOcultar, copiarValor, copiarExport.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 44 — `js/98-colecionador-codigo.js` (era `ferramentas/colecionador-codigo.html`, 586 linhas)

```text
Crie js/98-colecionador-codigo.js. Ele faz: Colecionador de Código — 📦 Colecionador de Código.
No app original ele tinha estas funções/partes: adicionarArquivos, renderLista, remover, setModo, setP, lerArquivo, analisar, gerarCompleto, gerarRapido, gerarFuncoes, gerarMapa, extrairFuncoes, extrairEventos, extrairAPIs, extrairVariaveis, extrairSeletores, tentarDescreverFuncao, copiar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 45 — `js/98-comandos-termux.js` (era `ferramentas/comandos-termux.html`, 305 linhas)

```text
Crie js/98-comandos-termux.js. Ele faz: 📦 Banco de Comandos Termux — 📦 Banco de Comandos Termux.
No app original ele tinha estas funções/partes: copiar, filtrar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 46 — `js/98-conversor-imagem.js` (era `ferramentas/conversor-imagem.html`, 474 linhas)

```text
Crie js/98-conversor-imagem.js. Ele faz: Conversor de Imagem Econômico — 🖼️ Conversor de Imagem Econômico.
No app original ele tinha estas funções/partes: carregarImagem, setModo, processar, fazerOCR, fazerComprimir, setProgresso, copiarTexto, baixarImagem, limpar, formatBytes.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 47 — `js/98-detector-api.js` (era `ferramentas/detector-api.html`, 657 linhas)

```text
Crie js/98-detector-api.js. Ele faz: Detector e Corretor de API — 🔍 Detector de Problemas de API.
No app original ele tinha estas funções/partes: analisarCodigo, mostrarResultados, corrigirUm, corrigirTudo, copiarResultado, analisarNovamente, limparTudo, escapeRegex, escapeHtml.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 48 — `js/98-divisor-html.js` (era `ferramentas/divisor-html.html`, 716 linhas)

```text
Crie js/98-divisor-html.js. Ele faz: Divisor de HTML — ✂️ Divisor de HTML Gigante.
No app original ele tinha estas funções/partes: estimarPartes, setModo, setProgresso, dividir, dividirAuto, dividirSoCSS, dividirSoJS, dividirSecoes, dividirLinhas, dividirHTMLporSecoes, gerarIndex, mostrarResultado, verPreview, baixarUma, baixarTodas, baixarZip, gerarCabecalho, getIconeTipo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 49 — `js/98-juntador.js` (era `ferramentas/juntador.html`, 455 linhas)

```text
Crie js/98-juntador.js. Ele faz: Juntador de Projetos HTML — 🔧 Juntador de Projetos HTML.
No app original ele tinha estas funções/partes: adicionarArquivos, renderLista, remover, getIcone, getTipo, lerArquivo, addLog, juntar, baixar, copiarCodigo, limparTudo, formatBytes.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 50 — `js/98-leitor-universal.js` (era `ferramentas/leitor-universal.html`, 1262 linhas)

```text
Crie js/98-leitor-universal.js. Ele faz: 📂 Leitor Universal de Arquivos — Leitor Universal de Arquivos.
No app original ele tinha estas funções/partes: processFile, detectFormat, renderAll, renderAIStudio, renderMsg, renderChatGPT, renderMessages, renderGenericJSON, renderText, renderRaw, showTab, toggleConv, resetApp, esc, escJS, fmtDate, formatBytes, infoBox.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 51 — `js/98-monica-guia.js` (era `ferramentas/monica-guia.html`, 343 linhas)

```text
Crie js/98-monica-guia.js. Ele faz: API Monica — Guia Visual — 🤖 API Monica — Guia Visual.
No app original ele tinha estas funções/partes: renderModelos, selecionarModelo, filtrar, atualizarSelectCalc, calcular, fmt, fmtBRL.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 52 — `js/98-monica-passo.js` (era `ferramentas/monica-passo.html`, 691 linhas)

```text
Crie js/98-monica-passo.js. Ele faz: Guia Monica API - Passo a Passo — 🔑 Guia Monica API.
No app original ele tinha estas funções/partes: trocarAba.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 53 — `js/98-montador-modulos.js` (era `ferramentas/montador-modulos.html`, 635 linhas)

```text
Crie js/98-montador-modulos.js. Ele faz: 🧩 Montador de Módulos — PWA Jurídico — 🧩 Montador de Módulos PWA JURÍDICO — MAIKON CALDEIRA.
No app original ele tinha estas funções/partes: getModules, setModules, getSelected, setSelected, showSection, showToast, saveModule, clearForm, renderModules, filterModules, deleteModule, copyModule, viewModule, editModule, renderBuildChecklist, toggleSelect, selectAll, deselectAll.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 54 — `js/98-procurar-substituir.js` (era `ferramentas/procurar-substituir.html`, 708 linhas)

```text
Crie js/98-procurar-substituir.js. Ele faz: Procurar e Substituir — 🔍 Procurar e Substituir.
No app original ele tinha estas funções/partes: trocarAba, preencherAtalho, contarOcorrencias, fazerSubstituicao, copiarResultado, copiarMulti, usarComoEntrada, limparTudo, adicionarPar, removerPar, fazerMultiplo, limparMultiplo, atualizarHistorico, limparHistorico, escapeRegex.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 55 — `js/98-inicio.js` (era `index.html`, 158 linhas)

```text
Crie js/98-inicio.js. Ele faz: Meu Chat.
Ele usa o que já foi criado em: js/10-base.js, js/15-banco.js, js/20-online.js, js/98-nuvem-embutida.js, js/98-nuvem-neon.js, js/25-nuvem.js, js/30-entrada.js, js/35-provedores.js, js/40-memoria.js, js/45-contextos.js, js/50-guia.js, js/55-jeito.js, js/60-gasto.js, js/65-arquivos.js, js/98-playground-replit.js, js/70-codigos.js, js/75-qr.js, js/85-pronto.js, js/90-testar.js, js/91-links.js, js/92-docs.js, js/98-ferramentas-lista.js, js/93-mesa.js, js/80-voz.js, js/94-internet.js, js/95-previa.js, js/96-texto.js, js/97-chat.js, js/98-cofre-arquivo.js, js/98-guia-versoes.js, js/98-guia-maikon.js, js/98-config.js, js/98-cofre.js, js/98-reconhecer.js, js/98-backup.js, js/98-restaurar.js, js/98-ponte-lab.js, js/98-janela-pc.js (pelo APP).
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 56 — `js/99-app.js` e conferir

```text
Crie js/99-app.js: ele olha APP.modulos e monta o menu/abas com um botão para cada módulo. Depois, me mande o index.html atualizado com todos os <script src="js/…"> na ordem certa: js/00-core.js, js/10-base.js, js/15-banco.js, js/20-online.js, js/25-nuvem.js, js/30-entrada.js, js/35-provedores.js, js/40-memoria.js, js/45-contextos.js, js/50-guia.js, js/55-jeito.js, js/60-gasto.js, js/65-arquivos.js, js/70-codigos.js, js/75-qr.js, js/80-voz.js, js/85-pronto.js, js/90-testar.js, js/91-links.js, js/92-docs.js, js/93-mesa.js, js/94-internet.js, js/95-previa.js, js/96-texto.js, js/97-chat.js, js/98-config.js, js/98-cofre.js, js/98-backup.js, js/98-restaurar.js, js/98-ponte-lab.js, js/98-janela-pc.js, js/98-cofre-arquivo.js, js/98-ferramentas-lista.js, js/98-guia-maikon.js, js/98-guia-versoes.js, js/98-nuvem-neon.js, js/98-playground-replit.js, js/98-reconhecer.js, js/98-nuvem-embutida.js, js/98-voz-francisco.js, js/98-analisador-v2.js, js/98-analisador.js, js/98-caca-sql.js, js/98-cofre-config.js, js/98-colecionador-codigo.js, js/98-comandos-termux.js, js/98-conversor-imagem.js, js/98-detector-api.js, js/98-divisor-html.js, js/98-juntador.js, js/98-leitor-universal.js, js/98-monica-guia.js, js/98-monica-passo.js, js/98-montador-modulos.js, js/98-procurar-substituir.js, js/98-inicio.js, js/99-app.js.
```

## 5. Conferir no final

- [ ] Abrir o index.html na prévia: aparece a tela sem erro (▤ console vazio)?
- [ ] Cada botão abre a sua parte?
- [ ] Fechar e abrir de novo: os dados continuam?
- [ ] Nada com "replit", "REPL_", "@workspace" no código (🏗️ Preparar confere).
- [ ] 📱 PWA → deixar instalável; 📦 APK ou 🖥️ .exe.
