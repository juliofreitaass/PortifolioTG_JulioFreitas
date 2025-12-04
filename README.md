# Portfólio de Projetos Integradores — CST Banco de Dados (FATEC)

## Introdução

Este trabalho apresenta a trajetória de desenvolvimento de projetos integradores ao longo do curso Superior de Tecnologia em Banco de Dados – FATEC, evidenciando a aplicação prática dos conhecimentos adquiridos. Será descrito o perfil do aluno, suas principais competências técnicas em Banco de Dados e áreas afins, e uma síntese dos projetos desenvolvidos em cada semestre do curso. Cada projeto é detalhado com contexto, objetivos, funcionalidades implementadas, tecnologias utilizadas, bem como as contribuições pessoais do aluno em cada caso. O projeto Stratify corresponde ao Trabalho de Graduação (TG) e é descrito de forma mais abrangente por sua importância e complexidade no fechamento do curso. Além disso, inclui-se o Projeto 6 (Pardal), que reforça experiência em Product Ownership e aplicação prática de LGPD como requisito de produto.

## Perfil

Julio Cesar Ferreira de Freitas é um tecnólogo em Banco de Dados em formação, com interesse focado no desenvolvimento Backend e engenharia de dados. Possui perfil analítico, habilidade em resolver problemas complexos de processamento de dados e experiência em liderança técnica de projetos (atuou como Product Owner em projetos acadêmicos). No decorrer do curso, demonstrou capacidade de aplicar conceitos de modelagem de banco de dados, programação e inteligência de negócios na criação de soluções computacionais. O profissional preza por boas práticas de codificação, organização de equipes utilizando metodologias ágeis e melhoria contínua de processos.

## Conhecimentos

O aluno desenvolveu um conjunto sólido de habilidades técnicas e teóricas ao longo do curso, destacando-se em linguagens de programação, bancos de dados, ferramentas de desenvolvimento e metodologias ágeis. A tabela a seguir resume as principais competências:

| Competência | Detalhamento |
|---|---|
| Linguagens de Programação | Java (experiência em APIs RESTful, projetos integradores em Spring Boot), Python (desenvolvimento de aplicações e scripts de automatização), JavaScript (Node.js para serviços backend e uso em configurações de pipelines). |
| Banco de Dados | Modelagem de dados relacional (MER, DER), SQL avançado (procedures, funções), experiência com SGBDs MySQL e PostgreSQL, conhecimento de NoSQL básico. |
| Tecnologias e Ferramentas | Git/GitHub (controle de versão em equipe), Docker (contêinerização de aplicações), APIs REST, JSON, ferramentas de integração contínua. |
| Metodologias Ágeis | Scrum e Kanban (atuações como desenvolvedor e Product Owner, gestão de backlog, sprints, reuniões diárias e retrospectivas para garantir entregas contínuas). |
| Outros Conhecimentos | IoT (Internet das Coisas) e protocolos básicos (atuou em projeto de IoT geográfico), conceitos de Big Data e ETL (pipeline de dados automatizado), elaboração de relatórios e dashboards analíticos. |

---

## Projeto 1: Avaliação 360

**Empresa/Cliente:** Setor de Recursos Humanos de uma empresa fictícia (caso de uso acadêmico).

**Problema:** A organização necessitava de uma ferramenta para realizar avaliações de desempenho 360° de seus colaboradores de forma eficiente. O método de feedback 360 graus proporciona uma visão completa do desempenho, coletando avaliações de líderes, pares e subordinados (referência: rh360graus.com.br). Antes do projeto, esse processo era moroso e realizado manualmente, dificultando a consolidação dos dados e o retorno aos colaboradores.

**Objetivo:** Desenvolver uma aplicação web que automatize o processo de avaliação 360° de desempenho. A solução deveria permitir que cada colaborador fosse avaliado por múltiplas pessoas (superiores, colegas e subordinados), consolidando essas percepções em relatórios claros. Buscou-se facilitar o registro de feedbacks anônimos, cálculo de métricas de desempenho e identificação de pontos fortes e a melhorar de cada funcionário. Ao final, a ferramenta visou agilizar o ciclo de avaliação de pessoal, fornecendo aos gestores informações ricas para tomadas de decisão sobre treinamento, promoção e melhorias organizacionais.

**Funcionalidades:** Dentre as principais funcionalidades implementadas destacam-se:

- Cadastro de colaboradores e definição das relações hierárquicas (quem avalia quem).
- Distribuição e preenchimento de formulários de avaliação qualitativa e quantitativa (competências, comportamento, resultados).
- Consolidação automática dos feedbacks recebidos em uma visão 360 graus para cada avaliado, incluindo cálculo de médias de notas, agregação de comentários e identificação de discrepâncias.
- Geração de dashboards e relatórios gráficos interativos para gestores visualizarem o desempenho individual e da equipe. Esses painéis apresentam, por exemplo, comparativos de autoavaliação vs. avaliação por pares, histogramas de notas e tendências gerais.
- Controle de acesso com diferentes perfis (avaliador, avaliado, administrador de RH) garantindo confidencialidade dos feedbacks e acesso apenas às informações pertinentes a cada usuário.

**Tecnologias:** O projeto foi desenvolvido principalmente em Python, aproveitando frameworks web para agilizar a construção da aplicação (por exemplo, Django, para estrutura MVC, e bibliotecas de gráficos para os dashboards). Utilizou-se JavaScript no front-end para tornar as interfaces interativas e responsivas. O banco de dados relacional (MySQL) armazena as informações de funcionários, vínculos de avaliação e resultados. Controle de versão foi feito no GitHub (organização wiz-fatec).

**Link:** Repositório GitHub – `wiz-fatec/avaliacao-360`.

**Contribuições Pessoais:** Atuando como Desenvolvedor Backend, Julio Freitas foi responsável por implementar funcionalidades críticas do lado do servidor. Ele desenvolveu a lógica de consolidação dos dados de avaliação, garantindo o cálculo correto de métricas (médias ponderadas de notas, percentuais) e a anonimização dos feedbacks antes da visualização pelos avaliados. Além disso, contribuiu significativamente na criação do dashboard administrativo, programando gráficos e relatórios gerenciais. Julio também integrou o sistema de autenticação e controle de permissões, assegurando que cada gestor pudesse ver relatórios apenas de sua equipe. Seu trabalho envolveu interação constante com o banco de dados (consultas SQL otimizadas para extrair agregados de avaliação) e integração com o front-end para exibir os resultados de forma amigável. Ademais, participou dos testes funcionais, validando que o fluxo de avaliação 360° estava consistente com os requisitos do projeto.

---

## Projeto 2: TG Manager

**Empresa/Cliente:** Coordenação do curso de Banco de Dados da FATEC (uso interno acadêmico).

**Problema:** A coordenação enfrentava dificuldades para compilar e acompanhar os resultados das avaliações dos Trabalhos de Graduação (TG) dos alunos. As notas e feedbacks dos projetos finais eram coletados via formulários separados, tornando complexo o gerenciamento das entregas parciais e a identificação de alunos aptos à defesa. Havia necessidade de organizar essas informações de modo centralizado, facilitando a atribuição de notas pelos professores orientadores e avaliadores, além de gerar relatórios para tomada de decisão sobre aprovações.

**Objetivo:** Desenvolver uma API e aplicação backend que importe os dados de avaliações de TG a partir de um arquivo CSV e auxilie na gestão do processo de Trabalho de Graduação. A solução objetiva facilitar a visualização dos dados de avaliação e permitir a inclusão de notas e feedbacks pelos professores de forma estruturada. Espera-se também automatizar o agendamento das etapas de entrega e apresentação do TG, definindo quantas entregas parciais haverá e calculando médias de notas conforme essas etapas. Por fim, a ferramenta deve gerar relatórios consolidados para a coordenação, indicando, por exemplo, quais alunos estão aptos a defender o TG e quais informações devem ser repassadas à banca examinadora.

**Funcionalidades:** A aplicação TG Manager contempla diversas funcionalidades alinhadas aos objetivos propostos:

- **Importação de CSV:** Upload de um arquivo “.csv” contendo as respostas de formulários preenchidos pelos alunos sobre seus TGs, populando automaticamente o sistema com esses dados brutos.
- **Gerenciamento de Entregas:** Configuração do número de entregas parciais que compõem o TG e agendamento das datas correspondentes, permitindo controlar prazos e etapas do projeto.
- **Atribuição de Notas e Feedbacks:** Interface para que professores insiram nota e feedback qualitativo para cada aluno em cada entrega/apresentação realizada.
- **Cálculo de Médias:** Cálculo automático da média final de cada aluno com base nas notas das várias entregas definidas, seguindo regra de negócio (média aritmética ou ponderada).
- **Relatórios Automatizados:** Relatório individual do aluno, relatório geral da turma e relatório de alunos aptos à defesa, incluindo dados como orientador e média final.

**Tecnologias:** Implementado em Java com Spring Boot (API REST), persistência em PostgreSQL, arquitetura em camadas (controllers/services/repositories), parsing de CSV com bibliotecas Java, testes unitários e de integração. Repositório sob organização wiz-fatec (api-2BD).

**Link:** Repositório GitHub – `wiz-fatec/api-2BD` (TG Manager).

**Contribuições Pessoais:** Como Desenvolvedor Backend, Julio Freitas implementou o módulo de importação de CSV (leitura, validações, tratamento de erros e persistência). Também criou endpoints para cadastro de entregas e registro de notas/feedbacks, além das regras de negócio para cálculo de média e identificação de aprovados. Participou da lógica de geração dos relatórios e apoiou qualidade do código (tratamento de exceções, ajustes e estabilidade), interagindo com o time em revisões e melhorias no modelo/consultas.

---

## Projeto 3: Dom Rock Pipeline Configurator

**Empresa/Cliente:** Dom Rock Enterprise (parceira acadêmica) – empresa da área de Big Data e Inteligência Artificial.

**Problema:** A criação e manutenção de pipelines de dados (ETL/ELT) costuma exigir esforço manual, especialistas e tempo. A demanda simulada do projeto foi reduzir atrito, permitindo configurar pipelines de forma visual, rápida e padronizada, diminuindo o tempo entre dado bruto e geração de valor.

**Objetivo:** Desenvolver uma aplicação web para configurar pipelines de dados da plataforma Dom Rock, permitindo definir fontes, transformações e destinos por UI (arrastar-e-soltar), gerando configurações para execução automatizada, alinhado à abordagem Setup & Run.

**Funcionalidades:**

- Catálogo de fontes e destinos (CSV, banco, APIs; Data Lake/BI).
- Editor visual de pipeline (componentes encadeados por etapas).
- Biblioteca de transformações (filtros, agregações, joins, limpeza).
- Validação e geração de configuração/deploy automatizado.
- Monitoramento de execução (status, volume, logs).

**Tecnologias:** Front-end em Vue.js; back-end em Node.js (Express); armazenamento das configurações em MongoDB; Docker para ambiente; GitHub para versionamento e issues.

**Link:** Repositório GitHub – `wiz-fatec/dom-rock-pipeline-configurator`.

**Contribuições Pessoais:** Julio Freitas atuou como Product Owner, traduzindo necessidades em backlog, priorizando entregas por sprint e definindo user stories/aceites. Participou das decisões técnicas (stack e arquitetura) e validou a usabilidade do configurador. Realizou merges, reviews e conduziu alinhamentos com “cliente” (simulado), garantindo foco em valor e entrega demonstrável.

---

## Projeto 4: GEO-IOT

**Empresa/Cliente:** Projeto interno acadêmico em parceria com laboratório de IoT – FATEC Manolito (interdisciplinar).

**Problema:** Monitorar sensores distribuídos geograficamente exige coleta, integração e visualização dos dados em tempo real, com localização em mapa e histórico. Sem uma plataforma, acompanhar posição, status e leituras se torna inviável.

**Objetivo:** Criar aplicação web para cadastro de dispositivos IoT com coordenadas, visualização em mapa e atualização em tempo real das leituras, com alertas e histórico analítico.

**Funcionalidades:**

- Cadastro de dispositivos com latitude/longitude e exibição em mapa.
- Recepção de dados em tempo real via MQTT/HTTP e persistência com timestamp.
- Painel geográfico: clique no dispositivo → últimos dados e status.
- Alertas por limites (mudança de cor/realce e notificação).
- Histórico e relatórios por dispositivo (tabela/gráfico por período).

**Technologias:** Front-end em Vue.js + Mapbox/Leaflet; back-end Node.js (Express) + websockets; broker MQTT e sensores simulados em Python; MongoDB com suporte geoespacial; Docker para ambiente com múltiplos serviços.

**Link:** Repositório GitHub – `manolito-fatec/geo-iot-2024-1`.

**Contribuições Pessoais:** Julio Freitas atuou como Product Owner, definindo escopo, priorizando funcionalidades de maior valor demonstrável e coordenando integração entre mapa, backend, broker MQTT e sensores simulados. Conduziu ritos ágeis, removeu impedimentos, testou o sistema ponta a ponta como usuário final e apoiou documentação de execução para apresentação.

---

## Projeto 5: Stratify (Trabalho de Graduação – TG)

**Empresa/Cliente:** Projeto autoral (Trabalho de Graduação) – foco em inteligência de dados para tomada de decisão empresarial.

**Problema:** Organizações acumulam dados, mas ainda sofrem para transformar isso em segmentação útil. A estratificação manual (planilhas/regras ad hoc) é lenta, falha e não captura padrões complexos. A necessidade central foi automatizar segmentação e entregar resultados interpretáveis para negócio.

**Objetivo:** Desenvolver uma API Backend para segmentação/estratificação de dados, integrável a diferentes front-ends/sistemas, com processamento de datasets heterogêneos, execução de algoritmos de clusterização (ex.: K-Means, DBSCAN, hierárquico) e/ou regras de negócio, entrega de métricas e exportações (JSON/CSV), e reprocessamento com novos dados.

**Funcionalidades:**

- Upload de dataset e schema configurável.
- Trigger de estratificação com parâmetros (algoritmo, `k`, regras).
- Monitoramento assíncrono por `process_id` e status.
- Resultados por segmento (tamanho, centroides/descrição, métricas).
- Export da base com coluna de segmento por registro.
- Histórico e comparação de segmentações.
- Segurança (JWT) e isolamento por cliente (multi-tenant).

**Tecnologias:** Python + FastAPI; pandas/numpy/scikit-learn; PostgreSQL (metadados/resultados) + MongoDB (dados brutos); Celery + Redis (tarefas); Apache Spark (opcional p/ volume); Docker/Compose; OpenAPI/Swagger; CI no GitHub.

**Link:** GitHub – `QuantumBitBR/API_5SEM` e `QuantumBitBR/API_5SEM_BACK`.

**Contribuições Pessoais:** Julio Freitas liderou o backend, desenhando arquitetura modular (ingestão/processamento/resultados), implementando algoritmos (K-Means com pré-processamento e métricas como silhouette), criando endpoints REST com paginação e erros claros, configurando processamento assíncrono com Celery/Redis, integrando PostgreSQL/MongoDB com otimizações e implementando JWT e infraestrutura via Docker/Compose. Também estruturou testes e documentação técnica (README e especificação de endpoints).

---

## Projeto 6: Pardal (6º semestre) — Gestão de Tickets + LGPD como Produto

**Empresa/Cliente:** Cliente parceiro do projeto integrador (contexto acadêmico) com operação de suporte/tickets.

**Problema:** O cliente enfrentava controle manual de tickets em base legada, ausência de histórico consolidado e falta de indicadores de performance para apoiar decisões. Além disso, existia risco real de armazenamento indevido de dados pessoais/sensíveis (especialmente em campos de texto livre), exigindo conformidade prática com LGPD.

**Objetivo:** Centralizar e otimizar um sistema de gestão de tickets de suporte, elevando organização, tempo de resposta e visibilidade operacional, ao mesmo tempo em que o produto incorpora LGPD como requisito central (não “checklist”), reduzindo risco de persistir dados pessoais/sensíveis e melhorando governança e transparência do processo.

**Funcionalidades (principais épicos e entregas):**

- **LGPD Modernization (Admin):** identificação e **anonimização automática** de dados pessoais e sensíveis em campos de texto livre (título/descrição/comentários). Uso de **Regex** para dados estruturados (ex.: CPF, e-mail, telefone) e integração com serviço **NLP** para análise semântica de sensíveis (ex.: saúde, religião, opinião política).
- **Insights (Gestão):** componente analítico que gera insights automaticamente (padrões de recorrência, categorias críticas e aderência a SLA), apoiando decisão e eficiência.
- **Dashboards (Gestão):** indicadores (KPIs) como total de tickets, tempo médio de resolução, recorrência e SLA, com filtros por período, agente, empresa, categoria e prioridade.
- **User Management (Admin):** gestão de usuários (criar/editar/desativar e perfis/roles) para controle de acesso.
- **Ticket Search (Operação):** busca avançada com filtros (status, categoria, agente, empresa, prioridade e período) para ganho de produtividade.

**Requisitos não funcionais trabalhados como entregáveis do produto:**

- Documentação de API
- Guia do usuário (User Guide)
- Design de banco
- Uso de banco não relacional (para partes do domínio)
- Conformidade LGPD

**Tecnologias:** Projeto full-stack com stack descrito no repositório:  
Back-end: Java + Spring Boot (Spring Security, Spring Web), Swagger, JWT, JUnit; além de Python e MongoDB; Docker e Vault.  
Front-end: TypeScript, Vue.js, PrimeVue, Axios, Vitest. (Estrutura com submódulos de `ai-server`, `web-server` e `web-client`).

**Link:** https://github.com/manolito-fatec/pardal-2025

**Contribuições Pessoais:** Julio Freitas atuou como **Product Owner**. Além de conduzir backlog/sprints e alinhar critérios de aceitação, teve participação decisiva em transformar **LGPD em funcionalidade de produto** (e não só em documentação): refinou requisitos de anonimização (Regex + NLP), priorizou histórias ligadas a governança de dados, controle de acesso e rastreabilidade, e garantiu que entregáveis como documentação/guia do usuário e requisitos não funcionais estivessem amarrados ao valor para operação e para o cliente. Esse projeto reforçou prática de PO em contexto de produto com segurança e conformidade como eixo central.

---

As informações apresentadas sobre cada projeto foram baseadas nos repositórios de código correspondentes no GitHub e em documentos fornecidos pelas equipes de desenvolvimento. Em especial, conceitos relacionados ao Dom Rock Pipeline foram fundamentados em materiais da plataforma Dom Rock. O Projeto 6 (Pardal) foi descrito a partir das especificações e documentação do repositório correspondente.
