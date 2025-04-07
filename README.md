# Workflow n8n: Integração Outlook + Brave API + OpenAI

Este workflow automatiza o processo de busca de informações sobre contatos externos em eventos do Outlook, utilizando a Brave Search API e OpenAI para gerar resumos informativos.

## Funcionalidades

- ⏰ Execução automática a cada 30 minutos
- 📅 Busca eventos do dia no Outlook
- 📧 Filtra contatos externos dos eventos
- 🌐 Busca informações públicas via Brave Search API
- 🧾 Gera resumos utilizando OpenAI
- 📤 Envia e-mails com os resumos para a equipe interna

## Configuração

### 1. Variáveis de Ambiente

Configure as seguintes variáveis de ambiente no n8n:

```bash
BRAVE_API_KEY=sua_chave_api_brave
OPENAI_API_KEY=sua_chave_api_openai
SMTP_FROM=seu_email_remetente
INTERNAL_TEAM_EMAIL=email_equipe_interna
```

### 2. Importação do Workflow

1. Baixe o arquivo `workflow.json` deste repositório
2. No n8n, vá para "Workflows"
3. Clique em "Import from File"
4. Selecione o arquivo `workflow.json`

### 3. Configuração do Microsoft Outlook

1. Configure a autenticação OAuth2 com o Microsoft Outlook no n8n
2. Verifique as permissões necessárias para acesso ao calendário

### 4. Teste o Workflow

1. Execute o workflow manualmente uma vez para verificar se todas as conexões estão funcionando
2. Verifique se os e-mails estão sendo enviados corretamente
3. Ajuste o agendamento (Cron) conforme necessário

## Personalização

- Modifique o filtro de domínios externos no nó "Filter External Contacts"
- Ajuste o prompt do OpenAI para gerar resumos mais específicos
- Personalize o template do e-mail no nó "Send Email"

## Suporte

Para problemas ou sugestões, abra uma issue neste repositório.