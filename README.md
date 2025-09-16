# Guia dos Arquivos — Funil n8n + ElevenLabs + WhatsApp

Este repositório reúne os **materiais da aula**. Abaixo, uma descrição **breve** de cada arquivo.

---

## `n8n_workflow.json`

Export do **fluxo n8n** usado na aula.
**Como usar:** copie **todo o conteúdo JSON** deste arquivo e **cole** em *n8n → Workflows → Import* (ou no editor, opção *Paste JSON*). O n8n **monta o fluxo automaticamente**. Em seguida, **ative/associe as credenciais** nos nós que exigem credenciais (ex.: Google Sheets, modelo de IA, ElevenLabs, provedor de WhatsApp).

---

## `pagina_web.html`

Arquivo **único** da **página de formulário** utilizada na aula (landing completa pronta para uso).
**Como usar:** altere **apenas a URL de envio do formulário** (action/endpoint) para a **URL da sua automação** (webhook ou endpoint que preferir).

---

## `prompt_do_agente.md`

**Prompt** do **agente de IA** responsável por gerar o **texto personalizado** que será transformado em áudio.

---

## `prompt_para_criar_pagina.md`

**Prompt** para **gerar/iterar a página HTML** via IA, mantendo a estrutura minimalista de inscrição com três campos.
