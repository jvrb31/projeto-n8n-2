# 📧 Resumo de Links por Email

Agente autônomo criado com n8n que lê links salvos no Google Sheets, resume o conteúdo com IA e envia o resumo automaticamente por email.

## 🔄 Como funciona

1. **Scheduler** → Executa automaticamente no horário definido
2. **Google Sheets** → Lê a lista de links pendentes
3. **If** → Filtra apenas links não processados
4. **HTTP Request** → Acessa e baixa o conteúdo do link
5. **HTML** → Extrai o texto da página
6. **IA (Gemini)** → Resume o conteúdo automaticamente
7. **Gmail** → Envia o resumo por email
8. **Google Sheets** → Marca o link como processado

## 🛠️ Tecnologias

- [n8n](https://n8n.io) — automação de fluxos
- Google Gemini — modelo de IA
- Google Sheets — gerenciamento de links
- Gmail — envio de resumos

## 👤 Autor

José — projeto desenvolvido para portfólio de automação com IA
