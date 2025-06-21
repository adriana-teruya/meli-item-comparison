# Product Comparison - Plano de Projeto

## 1. Visão Geral
Este projeto visa transformar um protótipo funcional inicial de comparação de produtos em uma solução robusta, escalável e pronta para implementação, integrando-o ao ecossistema existente do Mercado Livre.

O objetivo principal é oferecer aos usuários uma ferramenta de comparação avançada e confiável, que permita uma tomada de decisão de compra mais informada.

**Escopo:**
- Integração com Banco de Dados Real: Substituição do JSON local por banco de dados persistente e escalável.
- Busca Avançada de Produtos: Implementação de filtros, ordenação e pesquisa textual para aprimorar a capacidade de comparação.
- Integração via APIs: Conexão com APIs externas (próprias do Mercado Livre ou de terceiros) para obtenção de dados de produtos em tempo real.
- Arquitetura de Microserviços: Reestruturação do backend para garantir modularidade, escalabilidade e resiliência.
- Integração com Aplicação Principal do Mercado Livre: Adaptação e/ou incorporação da funcionalidade de comparação em fluxos existentes do ecossistema Mercado Livre.
- Testes: Implementação de testes automatizados (unitários, de integração, de ponta a ponta) para garantir a qualidade do software.
- Segurança, Confiabilidade e Escalabilidade: Implementação de melhores práticas para garantir a robustez da solução.
- Implantação em Fases: Estratégia de lançamento gradual para minimizar riscos.
- Monitoramento: Criação de métricas, dashboards para monitoramento e alertas para tratamento de problemas.
- Manutenção: Estabelecimento de um processo de melhoria contínua baseado em feedback e otimização pós-lançamento.

## 2. Estratégia Técnica

### 2.1. Sugestão de Stack Tecnológica
- **Frontend (React)**: Manteremos o React devido à sua flexibilidade, vasta comunidade e compatibilidade com o ecossistema atual.
- **Backend (Microserviços)**:
  - Linguagem de Programação: Java com Spring Boot ou GoLang são as opções preferenciais devido à sua performance, robustez e ecossistema maduro para microsserviços. A escolha final dependerá da expertise predominante na equipe e das necessidades de performance específicas.
  - Banco de Dados: PostgreSQL ou MySQL para dados relacionais dos produtos e MongoDB ou Cassandra para dados não-relacionais, como logs e cache, se necessário, garantindo escalabilidade.
  - Orquestração de Contêineres: Kubernetes para gerenciar os microsserviços, aproveitando a infraestrutura do Mercado Livre via plataforma FURY.
  - Mensageria: Apache Kafka para comunicação assíncrona entre microsserviços, garantindo resiliência e desacoplamento.
  - Cache: Redis para otimização de performance e redução de carga no banco de dados.

### 2.2. Otimização das entregas com utilização de GenAI e Ferramentas Modernas
Acreditamos que a integração de Inteligência Artificial Generativa (GenAI) e IDEs com capacidades Agentic será um diferencial para a eficiência do projeto.

**Desenvolvimento Assistido por GenAI:**
- Geração de Código: Utilização de ferramentas como GitHub Copilot ou similar para auxiliar na geração de boilerplate, testes unitários, documentação básica e sugestões de refatoração, acelerando o desenvolvimento e reduzindo erros.
- Revisão de Código: Ferramentas GenAI podem ser usadas para identificar padrões de código problemáticos, potenciais bugs e melhorias de performance, complementando a revisão humana.
- Diagnóstico de Erros: Análise de logs e tracebacks por GenAI para identificar a causa raiz de problemas mais rapidamente.

**Agentic IDEs e Plataformas de Desenvolvimento:**
- Automação de Tarefas Repetitivas: Scripts e automações em IDEs para configuração de ambientes, execução de testes e implantação local.
- Refatoração Inteligente: Recursos avançados de refatoração que garantem a integridade do código.
- CI/CD: Utilização de plataformas como Jenkins, GitLab CI/CD ou GitHub Actions para automação completa do pipeline de desenvolvimento, desde o commit até a implantação, com integrações inteligentes para feedback rápido.
- FURY Platform: Aproveitar a FURY platform do Mercado Livre para configuração e provisionamento de infraestrutura, ambientes de desenvolvimento e produção, automatizando tarefas de DevOps e padronizando a implantação.

## 3. Planejamento de Recursos e Cronograma

### 3.1. Equipe e Responsabilidades (para um projeto em escala total)
* **Sugestão de time e alocação (em % de capacidade) e cronograma para execução do projeto, considerando o uso de Gen AI, Agentic IDE e Plataforma FURY para otimização das entregas:**

- **1 Líder de Projeto (30%)**: Responsável pela gestão geral do projeto, comunicação, alinhamento técnico e estratégico. 
- **1 Engenheiros de Software Sênior (100%)**: Responsáveis pela arquitetura dos microsserviços, revisão de código e resolução de problemas complexos.
- **2 Engenheiros de Software Pleno (100%)**: Foco no desenvolvimento de funcionalidades, testes e integração.
- **1 Engenheiro Especialista (25%)**: Responsável pela infraestrutura, CI/CD, monitoramento e otimização de performance, atuando como um recurso compartilhado (alocação escalável conforme a demanda).

### 3.2. Milestones e Dependências

**Milestone 1: Preparação e Estrutura (Semanas 1)**
- M1.1: Definição final da arquitetura de microsserviços e tecnologias.
- M1.2: Configuração inicial dos ambientes de desenvolvimento e CI/CD na FURY.
- M1.3: Implementação do esqueleto de um microsserviço e integração com BD.
  - Dependências: Decisão técnica da stack, acesso à plataforma FURY.

**Milestone 2: Backend e Dados (Semanas 2-4)**
- M2.1: Conclusão da integração com banco de dados real.
- M2.2: Desenvolvimento do microsserviço de busca avançada.
- M2.3: Integração com as primeiras APIs reais de produtos (Meli).
- M2.4: Implementação dos primeiros testes de integração e unitários do backend.
  - Dependências: Disponibilidade das APIs do Mercado Livre, dados de produtos.

**Milestone 3: Frontend e Integração (Semanas 5-6)**
- M3.1: Adaptação do frontend para consumir os novos microsserviços.
- M3.2: Implementação das funcionalidades de busca avançada no frontend.
- M3.3: Desenvolvimento da interface de comparação aprimorada.
- M3.4: Implementação dos testes automatizados de frontend (e2e, unitários).
  - Dependências: Backend estável, definição das funcionalidades de integração com a aplicação principal.

**Milestone 4: Refinamento, Segurança e Implantação (Semanas 7-8)**
- M4.1: Auditoria de segurança da funcionalidade e serviços, checagem de fatores regulatórios / legal / compliance (se aplicável), e otimização de performance.
- M4.2: Configuração de monitoramento e alertas (via FURY e ferramentas Meli).
- M4.3: Implantação em ambiente de staging para testes de larga escala e estratégia de implantação em ambiente de produção.
- M4.4: Lançamento da primeira fase em produção (ex: para um grupo restrito de usuários) e acompanhamento pós-implantação.
  - Dependências: Testes Ok, aprovação de segurança, infraestrutura pronta na FURY.

## 4. Considerações Adicionais

- **Documentação**: Manutenção de documentação técnica clara e atualizada para os microsserviços (API docs, diagramas de arquitetura) e para o processo de desenvolvimento como um todo.

- **Comunicação**: Reuniões de alinhamento semanais, uso de ferramentas de comunicação interna (Slack, Google Meet) para agilizar decisões e disseminar informações.

- **Gestão de Conhecimento**: Compartilhamento de conhecimento entre a equipe através de sessões de Pair Programming e workshops.

- **Manutenção**: Dedicação de tempo em sprints futuras para correção de problemas, otimização de performance e implementação de melhorias baseadas nos dados de monitoramento.

- **Melhorias**: Análise de benchmarking e evolução da funcionalidade (ex: inclusão de histórico de preços dos produtos consultados e alerta de preço desejado). 

Este plano de projeto busca garantir uma evolução eficiente e bem-sucedida do protótipo, transformando-o em uma funcionalidade de valor agregado para os usuários do Mercado Livre, com foco em qualidade, performance e sustentabilidade a longo prazo. 