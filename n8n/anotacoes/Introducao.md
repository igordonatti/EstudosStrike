# N8N

## O que é o n8n
O **n8n** é uma ferramenta de automacão de workflows que permite integrar diferentes servicos, APIs e sistemas sem a necessidade de codificacão extensa. Ele é uma solucão **low-code** e **open-source**, facilitando a criacão de fluxos de trabalho automatizados para realizar tarefas repetitivas, integrando plataformas de forma eficiente e personalizada.

- **Automacao de workflows:** Permite criar fluxos de trabalho automaticos conectando servicos como APIs, banco de dados, ferramentas de comunicacao, etc.
- **Node-based:** Cada integracao ou tarefa é representada como um "nó" (node), que pode ser configurado e conectado a outros para criar fluxos complexos.

## Funcionalidades principais
- **Integracao com APIs:** Conecte-se a servicos populares (Google Sheets, Slack, GitHub, etc.) ou APIs customizadas.
- **Execucao condicional:** Crie automacoes que tomam decisoes com base em condicoes especificas.
- **Agendador:** Defina horarios especificos para a execucao dos fluxos.
- **Webhook listener:** Receba dados wia webhooks e dispare automacoes.
- **Execucao de scripts personalizados:** Adicione o codigo JavaScript para criar automacoes mais complexas.
- **Monitoramento e logging:** Veja logs detalhados das execucoes e monitoramento dos workflows.

## Nodes
Based on ther function, n8n classifies nodes into four types:
- **App or Action Nodes: add, remove, and edit data; request and send external data; and trigger events in other systems. 
- **Trigger Nodes**: start a workflow and supply the initial data.
- **Core Nodes**: can ve core or app nodes. Whereas most nodes connect to a specific external service, core nodes provide functionality such as logic, scheduling, or generic API calls. 
- **Cluster Nodes**: are node groups that work together to provide functionality in a workflow.