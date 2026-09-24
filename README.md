# 🧠 Caderno Temático: Automação de Workflows com n8n

Este repositório documenta o processo de criação de um caderno temático de estudos utilizando a IA NotebookLM, desenvolvido como parte de um desafio prático.

## 🎯 Contexto e Objetivos
O tema escolhido para este estudo foi **Automação de Workflows com n8n**. 
O objetivo principal é entender como estruturar fluxos de trabalho automatizados (workflows) para integrar diferentes ferramentas utilizadas no dia a dia de Operações de TI (NOC), como sistemas de monitoramento (ex: Zabbix) e plataformas de gestão de incidentes (ex: Jira). A meta é dominar os conceitos básicos de nós (nodes), gatilhos (triggers) e manipulação de dados em JSON dentro do n8n.

## 📚 Curadoria de Fontes
Para alimentar o NotebookLM e criar uma base de conhecimento sólida, selecionei os seguintes materiais (em formato PDF e texto):
1. **[Documentação Oficial do n8n: Core Concepts]** - PDF extraído da documentação oficial explicando os conceitos de Nodes, Connections e Workflows.
2. **[Guia Prático: Integração via Webhooks]** - Artigo técnico sobre como configurar gatilhos de entrada e saída via HTTP Request.
3. **[Boas Práticas de Segurança e Credenciais no n8n]** - Texto detalhando como gerenciar chaves de API e credenciais de forma segura.

## 🛠️ Engenharia de Prompts e "Cicatrizes" (Troubleshooting)

Durante a interação com o NotebookLM, testei diversas abordagens para extrair as melhores respostas.

* **Tentativa 1 (Ampla):** 
  * *Prompt:* "Resuma tudo sobre o n8n."
  * *Resultado:* A IA gerou um texto muito genérico, parecendo um artigo de blog, sem foco técnico. 
* **Tentativa 2 (Específica, mas incompleta):** 
  * *Prompt:* "Como eu conecto o n8n com um sistema de monitoramento?"
  * *Resultado:* A IA listou os passos, mas não especificou qual nó usar.
  * *Cicatriz/Aprendizado:* Descobri que preciso dar o contexto exato das ferramentas e do formato dos dados para obter respostas aplicáveis.
* **Tentativa 3 (Prompt Otimizado):** 
  * *Prompt:* "Com base nas fontes carregadas, explique passo a passo como configurar um nó de Webhook no n8n para receber alertas no formato JSON de um sistema externo, e liste quais as boas práticas de segurança recomendadas."
  * *Resultado:* Resposta perfeita, detalhando a configuração do Webhook, o tratamento do payload JSON e o uso correto das credenciais.

---

## 📖 Miniguia de Estudo (Entrega Final)

### Resumo Estruturado: Fundamentos do n8n
O n8n é uma ferramenta de automação de fluxo de trabalho baseada em nós (nodes) que permite conectar qualquer aplicativo com uma API. Ao contrário de outras ferramentas do mercado, ele permite automações complexas com tratamento profundo de dados.
* **Como funciona:** Um workflow começa sempre com um *Trigger Node* (Gatilho), que inicia o processo quando um evento ocorre (ex: receber um email, um webhook de alerta, ou um horário agendado).
* **Processamento:** Após o gatilho, os *Action Nodes* executam tarefas específicas (formatar texto, enviar mensagens no Slack, criar tickets no Jira).
* **Dados:** A comunicação entre os nós é feita puramente em formato JSON, o que facilita a filtragem e extração de variáveis específicas.

### 🔤 Glossário
* **Node (Nó):** O bloco de construção básico de um workflow. Cada nó executa uma ação específica ou conecta a um serviço.
* **Trigger (Gatilho):** Um tipo especial de nó que inicia automaticamente um workflow quando um evento específico acontece.
* **Webhook:** Uma forma de receber dados de outros aplicativos em tempo real via requisição HTTP (geralmente POST ou GET).
* **JSON (JavaScript Object Notation):** O formato de texto padrão usado para armazenar e transportar os dados entre os nós no n8n.
* **Credentials (Credenciais):** Área segura do n8n onde você armazena tokens de autenticação, senhas e chaves de API para conectar os nós aos serviços externos.

### 🔄 Prompts Reutilizáveis para Revisão
Sempre que precisar revisar ou aprofundar este tema no NotebookLM, utilize os seguintes prompts:
1. *"Explique o conceito de [INSERIR NOME DO NÓ/CONCEITO] no n8n como se eu fosse um desenvolvedor júnior."*
2. *"Gere um exemplo prático de payload JSON que um Webhook do n8n poderia receber de um sistema de alertas."*
3. *"Crie um questionário de 5 perguntas de múltipla escolha com base nestas fontes para testar meus conhecimentos sobre automação de processos."*
