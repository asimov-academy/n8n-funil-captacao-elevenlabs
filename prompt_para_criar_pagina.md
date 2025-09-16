## Instruções

Quero que você gere **um único arquivo HTML** com CSS e JS embutidos (sem dependências externas) para uma **página de inscrição** ultra simples.

## Objetivo

Criar uma landing minimalista com **apenas 3 campos** e envio para webhook.

## Variáveis (troque se quiser)

- `{{TITULO}}`: Inscreva-se para o curso
- `{{SUBCOPY}}`: Deixe seu **nome**, **e-mail** e **WhatsApp** para receber o acesso e os materiais.
- `{{CTA}}`: Garantir minha vaga
- `{{WEBHOOK_URL}}`: https://n8n.srv977866.hstgr.cloud/webhook/form

## Requisitos funcionais

1. **Campos**: `nome` (texto), `email` (email), `whatsapp` (tel). Todos obrigatórios.
2. **Máscara WhatsApp (BR)** durante digitação:
    - Formatar como `(11) 9XXXX-XXXX` quando houver 11 dígitos; aceitar 10 ou 11 dígitos.
    - **Antes de submeter**, enviar **apenas dígitos** no campo `whatsapp`.
3. **Validações mínimas**:
    - Nome ≥ 2 caracteres.
    - E-mail com regex simples `/.+@.+\\..+/`.
    - WhatsApp com 10–11 dígitos.
4. **Honeypot**: campo invisível `website_field`; se preenchido, não submeter.
5. **Submit sem sair da página**: usar `target="webhookFrame"` (iframe oculto).
    - Desabilitar botão e trocar texto para “Enviando…”.
    - Ao carregar o iframe: mostrar alerta de **sucesso**, limpar formulário, reabilitar botão e restaurar texto.
    - Timeout de segurança de 6s para reabilitar o botão caso o load não dispare.
6. **Alertas**: caixas de sucesso/erro com `role="status"`/`role="alert"` e `aria-live`.
7. **Acessibilidade**: `label for` + `id` correspondentes, títulos claros, foco no alerta após sucesso.
8. **Sem libs/frameworks**. Tudo em **um arquivo**. Sem Analytics.
9. **Compatibilidade mobile (iOS)**: inputs com `font-size ≥ 16px` para evitar zoom; layout centrado, **max-width 560px**, dark theme simples; tipografia de sistema.
10. **Metadados**: `<meta charset="utf-8">`, `<meta name="viewport" content="width=device-width, initial-scale=1">`.
11. **Cópia genérica** usando `{{TITULO}}` e `{{SUBCOPY}}`.
12. **Botão CTA** com texto `{{CTA}}`.
13. **Action do form** apontando para `{{WEBHOOK_URL}}` e método `POST`.

## Entrega

- Responda **somente** com o **arquivo HTML completo**, iniciando em `<!doctype html>` e sem comentários ou explicações fora do código.
- Não inclua nada além do código do arquivo.

Use estes valores padrão (substitua pelos placeholders no HTML):

`{{TITULO}} = Inscreva-se para o curso`

`{{SUBCOPY}} = Deixe seu nome, e-mail e WhatsApp para receber o acesso e os materiais.`

`{{CTA}} = Garantir minha vaga`

`{{WEBHOOK_URL}} = https://n8n.srv977866.hstgr.cloud/webhook/form`
