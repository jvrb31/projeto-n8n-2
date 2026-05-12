# 📧 Link Summarizer — Resumo Automático de Links por Email

> Agente autônomo criado com **n8n** que lê links salvos no Google Sheets, resume o conteúdo com IA (Gemini) e envia o resumo automaticamente por email.

---

## 🚀 Demonstração

> 📸 *[Adicione aqui um print ou GIF do workflow rodando no n8n]*

---

## 💡 O Problema que Resolve

Acumular links para ler depois e nunca ler é comum. Este projeto resolve isso automaticamente: você salva o link numa planilha e o agente lê, resume e entrega no seu email no horário que você definir.

---

## 🔄 Como Funciona

```
[Scheduler — horário definido]
          ↓
  Google Sheets (lê links pendentes)
          ↓
       If (filtra não processados)
          ↓
  HTTP Request (acessa o link)
          ↓
  HTML Parser (extrai o texto)
          ↓
  Gemini AI (resume o conteúdo)
          ↓
  Gmail (envia o resumo por email)
          ↓
  Google Sheets (marca como processado ✅)
```

| Etapa | Nó | Função |
|---|---|---|
| 1 | Scheduler | Executa automaticamente no horário definido |
| 2 | Google Sheets | Lê a lista de links pendentes |
| 3 | If | Filtra apenas links não processados |
| 4 | HTTP Request | Faz o download do conteúdo da página |
| 5 | HTML | Extrai texto limpo do HTML |
| 6 | Gemini AI | Gera o resumo automaticamente |
| 7 | Gmail | Envia o resumo formatado por email |
| 8 | Google Sheets | Marca o link como processado |

---

## 🛠️ Tecnologias

| Ferramenta | Uso |
|---|---|
| [n8n](https://n8n.io) | Orquestração do fluxo |
| Google Gemini | Modelo de linguagem para resumo |
| Google Sheets | Gerenciamento da lista de links |
| Gmail | Envio dos resumos |

---

## ▶️ Como Usar

### Pré-requisitos
- Conta no [n8n.io](https://n8n.io) (cloud ou self-hosted)
- Chave de API do Google Gemini (gratuita em [aistudio.google.com](https://aistudio.google.com))
- Conta Google (para Sheets e Gmail)

### Instalação

1. Clone este repositório
```bash
git clone https://github.com/jvrb31/projeto-n8n-2.git
```

2. No n8n, vá em **Workflows → Import from file**
3. Importe o arquivo `link-summarizer-workflow.json`
4. Configure as credenciais:
   - Google Gemini API Key
   - Google Sheets OAuth
   - Gmail OAuth
5. No Google Sheets, crie uma planilha com as colunas:
   - `url` | `processado`
6. Adicione links na coluna `url` com `processado = false`
7. Ative o workflow — ele rodará automaticamente no horário configurado

---

## 📂 Estrutura do Repositório

```
projeto-n8n-2/
├── link-summarizer-workflow.json   # Workflow exportado do n8n
└── README.md
```

---

## 👤 Autor

**José** — [LinkedIn](https://linkedin.com/in/josevitorr00) · [GitHub](https://github.com/jvrb31)

> Projeto desenvolvido para portfólio de automação com IA.

**José** — [LinkedIn](https://linkedin.com/in/SEU-LINKEDIN) · [GitHub](https://github.com/jvrb31)

> Projeto desenvolvido para portfólio de automação com IA.
