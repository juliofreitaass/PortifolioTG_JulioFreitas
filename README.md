# Portfólio de Projetos Integradores — CST Banco de Dados (FATEC)

## Introdução

Este trabalho apresenta a trajetória de desenvolvimento de projetos integradores ao longo do curso Superior de Tecnologia em Banco de Dados – FATEC, evidenciando a aplicação prática dos conhecimentos adquiridos. Será descrito o perfil do aluno, suas principais competências técnicas em Banco de Dados e áreas afins, e uma síntese dos projetos desenvolvidos em cada semestre do curso. Cada projeto é detalhado com contexto, objetivos, funcionalidades implementadas, tecnologias utilizadas, bem como as contribuições pessoais do aluno em cada caso. O último projeto – denominado Stratify – corresponde ao Trabalho de Graduação (TG) e será descrito de forma mais abrangente por sua importância e complexidade no fechamento do curso.

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

**Contribuições Pessoais:** Atuando como Desenvolvedor Backend, Julio Freitas foi responsável por implementar funcionalidades críticas do lado do servidor. Ele desenvolveu a lógica de consolidação dos dados de avaliação, garantindo o cálculo correto de métricas (médias ponderadas de notas, percentuais) e a anonimização dos feedbacks antes da visualização pelos avaliados. Além disso, contribuiu significativamente na criação do dashboard administrativo, programando gráficos e relatórios gerenciais (referência: github.com). Julio também integrou o sistema de autenticação e controle de permissões, assegurando que cada gestor pudesse ver relatórios apenas de sua equipe. Seu trabalho envolveu interação constante com o banco de dados (consultas SQL otimizadas para extrair agregados de avaliação) e integração com o front-end para exibir os resultados de forma amigável. Ademais, participou dos testes funcionais, validando que o fluxo de avaliação 360° estava consistente com os requisitos do projeto.

---

## Projeto 2: TG Manager

**Empresa/Cliente:** Coordenação do curso de Banco de Dados da FATEC (uso interno acadêmico).

**Problema:** A coordenação enfrentava dificuldades para compilar e acompanhar os resultados das avaliações dos Trabalhos de Graduação (TG) dos alunos. As notas e feedbacks dos projetos finais eram coletados via formulários separados, tornando complexo o gerenciamento das entregas parciais e a identificação de alunos aptos à defesa. Havia necessidade de organizar essas informações de modo centralizado, facilitando a atribuição de notas pelos professores orientadores e avaliadores, além de gerar relatórios para tomada de decisão sobre aprovações.

**Objetivo:** Desenvolver uma API e aplicação backend que importe os dados de avaliações de TG a partir de um arquivo CSV e auxilie na gestão do processo de Trabalho de Graduação (referência: github.com). A solução objetiva facilitar a visualização dos dados de avaliação e permitir a inclusão de notas e feedbacks pelos professores de forma estruturada (referência: github.com). Espera-se também automatizar o agendamento das etapas de entrega e apresentação do TG, definindo quantas entregas parciais haverá e calculando médias de notas conforme essas etapas. Por fim, a ferramenta deve gerar relatórios consolidados para a coordenação, indicando, por exemplo, quais alunos estão aptos a defender o TG e quais informações devem ser repassadas à banca examinadora.

**Funcionalidades:** A aplicação TG Manager contempla diversas funcionalidades alinhadas aos objetivos propostos:

- **Importação de CSV:** Upload de um arquivo “.csv” contendo as respostas de formulários preenchidos pelos alunos sobre seus TGs, populando automaticamente o sistema com esses dados brutos (referência: github.com).
- **Gerenciamento de Entregas:** Configuração do número de entregas parciais que compõem o TG e agendamento das datas correspondentes, permitindo controlar prazos e etapas do projeto (referência: github.com).
- **Atribuição de Notas e Feedbacks:** Interface para que professores insiram nota e feedback qualitativo para cada aluno em cada entrega/apresentação realizada (referência: github.com). A aplicação armazena esses inputs, possibilitando o acompanhamento da evolução de cada projeto.
- **Cálculo de Médias:** Cálculo automático da média final de cada aluno com base nas notas das várias entregas definidas, seguindo a regra de negócio (por exemplo, média aritmética ou ponderada das notas das etapas) (referência: github.com).
- **Relatórios Automatizados:** Geração de diversos relatórios em formato visual e textual. Dentre eles: relatório individual de cada aluno (compilando todos os feedbacks e notas recebidas), relatório geral de todos os alunos (lista completa com suas médias finais) e um relatório específico listando alunos aptos a defesa – aqueles que atingiram nota mínima para aprovação – incluindo informações de seus orientadores (referências: github.com / github.com). Esses relatórios visam apoiar a coordenação na organização das bancas finais e na comunicação de resultados.

**Tecnologias:** O TG Manager foi implementado em Java (utilizando princípios de API REST). O projeto fez uso do framework Spring Boot para agilizar a criação dos serviços backend, dada sua robustez em aplicações corporativas Java. Para persistência de dados, optou-se por um banco relacional (PostgreSQL) devido à necessidade de consistência e facilidade em manipular dados tabulares vindos do CSV. A leitura e parsing do arquivo CSV foram feitos com bibliotecas Java, convertendo as linhas em registros no banco. A aplicação seguiu arquitetura em camadas (controladores REST, serviços de negócio e repositórios de dados). Testes unitários e de integração foram conduzidos para garantir a correta importação e processamento dos dados. O repositório de código está disponível no GitHub sob a organização wiz-fatec (nome do repositório: api-2BD).

**Link:** Repositório GitHub – `wiz-fatec/api-2BD` (TG Manager) (referência: github.com).

**Contribuições Pessoais:** Atuando novamente como Desenvolvedor Backend, Julio Freitas contribuiu ativamente em diversas partes do TG Manager. Ele foi responsável pela implementação do módulo de importação de CSV, lidando com a leitura dos arquivos de entrada, tratamento de erros de formato e inserção dos dados no banco de forma consistente. Com isso, facilitou o carregamento inicial das avaliações no sistema (referência: github.com). Julio também desenvolveu endpoints RESTful para cadastro de entregas e agendamento das datas, bem como para registrar notas e feedbacks por meio de requisições HTTP seguras. Implementou as regras de negócio de cálculo da média final de cada aluno, garantindo que o sistema identificasse corretamente os alunos aprovados para a defesa. Ademais, colaborou na geração dos relatórios automáticos: participou da lógica de seleção e agregação dos dados necessários para compor os relatórios de cada aluno e gerais, inclusive o relatório de alunos aptos à defesa (referências: github.com / github.com). Durante o desenvolvimento, Julio preocupou-se com a qualidade do código, adicionando logs úteis e tratando exceções para manter a aplicação confiável (há evidências de commits removendo logs inúteis e corrigindo bugs para estabilidade). Ele interagiu de perto com os demais membros da equipe, revisando código e sugerindo melhorias (por exemplo, otimização de consultas SQL e refinamento do modelo de dados para melhor adequação aos relatórios exigidos). Sua contribuição foi fundamental para que a API estivesse consistente com as necessidades da coordenação do curso, agilizando significativamente o processo de avaliação dos TGs.

---

## Projeto 3: Dom Rock Pipeline Configurator

**Empresa/Cliente:** Dom Rock Enterprise (parceira acadêmica) – empresa da área de Big Data e Inteligência Artificial.

**Problema:** Empresas que trabalham com grandes volumes de dados frequentemente enfrentam desafios na configuração e automação de seus pipelines de dados. O processo tradicional de criar pipelines (ETL/ELT) pode demandar especialistas e muito esforço manual, desde a captura de dados até a visualização dos resultados. A Dom Rock identificou a oportunidade de facilitar esse processo por meio de uma ferramenta que permitisse configurar pipelines de dados de forma gráfica e intuitiva, sem necessidade de programação extensa ou intervenção de um engenheiro de dados a cada alteração. O projeto acadêmico visa simular essa demanda real: tornar a montagem de fluxos de dados algo fácil e rápido, diminuindo o tempo entre o dado bruto e a geração de valor de negócio.

**Objetivo:** Desenvolver uma aplicação (interface web) que funcionasse como um configurador de pipelines de dados da plataforma Dom Rock. Em essência, a ferramenta deveria possibilitar que usuários (analistas de negócio, cientistas de dados ou engenheiros de dados) definissem fontes de dados, transformações e destinos de forma visual, gerando por trás as configurações necessárias para execução automatizada do pipeline. Assim, buscou-se agilizar o desenvolvimento de pipelines automatizados conforme a demanda de cada negócio, alinhado à metodologia Setup & Run da Dom Rock (referência: domrock.net). Em termos acadêmicos, o objetivo incluiu aplicar conceitos de integração de dados, Data Lake e orquestração de processos de forma prática.

**Funcionalidades:** O Dom Rock Pipeline Configurator incorporou diversas funcionalidades para atender ao objetivo de simplificar a criação de pipelines de dados:

- **Catálogo de Fontes e Destinos:** Módulo para cadastrar e visualizar fontes de dados (e.g., arquivos CSV, bancos de dados, APIs) e destinos possíveis (como tabelas em Data Lake ou dashboards de BI). Os usuários podiam selecionar a fonte desejada para iniciar um pipeline.
- **Configuração de Pipeline via UI:** Interface gráfica onde o usuário “monta” o fluxo de dados, arrastando componentes que representem etapas como Extração, Transformação e Carga, e encadeando-os na sequência lógica desejada. Para cada etapa, era possível configurar parâmetros (p. ex., consultas SQL na extração, regras de transformação, mapeamento de campos).
- **Componentes Pré-definidos:** Biblioteca de componentes de transformação prontos (filtros, agregações, junções de dados, limpeza de dados, etc.), que podiam ser incluídos no pipeline com poucos cliques.
- **Validação e Deploy Automatizado:** Ao finalizar o desenho do pipeline, a ferramenta valida a consistência (por exemplo, verifica se todas as etapas estão conectadas e configuradas) e então gera um arquivo de configuração ou script executável pela plataforma Dom Rock. O usuário pode então implantar (deploy) esse pipeline com um botão.
- **Visualização de Execução:** Painel de acompanhamento para pipelines implantados, exibindo status (em execução, concluído, falhou), volume de dados processados e possíveis logs de erro.

**Tecnologias:** A solução foi desenvolvida com foco em JavaScript. No front-end, utilizou-se Vue.js para criar a interface de arrastar-e-soltar dos componentes do pipeline. No back-end, optou-se por Node.js com framework Express, implementando APIs que conversavam com serviços simulados da Dom Rock. Também foram empregadas tecnologias como MongoDB para armazenar temporariamente as configurações de pipeline montadas (documentos JSON). O ambiente de desenvolvimento foi conteinerizado com Docker, e todo o versionamento e gerenciamento de issues se deu via GitHub (organização wiz-fatec).

**Link:** Repositório GitHub – `wiz-fatec/dom-rock-pipeline-configurator`.

**Contribuições Pessoais:** Neste projeto, Julio Freitas atuou como Product Owner, liderando a equipe multidisciplinar de desenvolvedores. Ele foi responsável por traduzir as necessidades da Dom Rock em requisitos claros para o time, elaborando o Backlog do Produto e priorizando as entregas em sprints. Julio conduziu reuniões de planejamento, definiu as user stories e garantiu critérios de aceitação claros. Além da gestão, participou das decisões técnicas: influenciou na escolha do stack tecnológico e validou a arquitetura proposta. Durante o desenvolvimento, revisou as funcionalidades entregues, assegurando que a interface fosse intuitiva e cumprisse o propósito de simplificar a criação de pipelines de dados. A expertise de Julio na área de dados foi útil para orientar a implementação de componentes de transformação comuns, alinhados às práticas de ETL. Ele não realizou muitos commits de código diretamente (focando seu papel em gestão), mas efetuou merges de contribuições e cuidou da qualidade geral do projeto. Suas contribuições pessoais incluem também o contato simulado com a “cliente” Dom Rock, providenciando feedbacks rápidos para ajustes de usabilidade. Ao final, foi possível demonstrar um pipeline sendo configurado rapidamente, evidenciando o ganho de agilidade que a ferramenta proporciona, em linha com a abordagem Setup & Run (referência: domrock.net). A entrega foi considerada um sucesso dentro do contexto acadêmico e demonstrou as habilidades de Julio em gerência de projetos ágeis e visão de produto.

---

## Projeto 4: GEO-IOT

**Empresa/Cliente:** Projeto interno acadêmico em parceria com laboratório de IoT (Internet das Coisas) – FATEC Manolito (projeto interdisciplinar).

**Problema:** Em muitas aplicações de IoT, sensores espalhados geograficamente transmitem dados que precisam ser coletados, integrados e visualizados em tempo real. O desafio está em localizar esses dispositivos no mapa e monitorar as leituras de forma centralizada. Sem uma plataforma adequada, seria difícil acompanhar posição e estado de cada dispositivo. O projeto GEO-IOT surgiu para endereçar essa demanda: integrar dados geográficos e de IoT para visualizar dispositivos e suas medições em tempo real. No ambiente acadêmico, o problema se traduz na necessidade de combinar conhecimentos de banco de dados geográficos, interfaces web e protocolos de IoT para criar uma solução funcional.

**Objetivo:** Construir uma aplicação web que permita gerenciar dispositivos IoT com posicionamento geográfico, monitorando suas informações em tempo real. O sistema deveria permitir cadastro de dispositivos (latitude/longitude) e plotagem em mapa interativo, além de receber periodicamente dados desses dispositivos e exibir atualizações ao usuário. Também estava em escopo implementar alertas/indicadores quando algum valor atingir limiar (ex.: temperatura alta disparando alerta visual no mapa).

**Funcionalidades:** O projeto GEO-IOT agregou funcionalidades que integraram geolocalização e IoT de forma eficiente:

- **Cadastro e Geolocalização de Dispositivos:** Registro de dispositivos com coordenadas e exibição em mapa interativo (Google Maps/Leaflet).
- **Recepção de Dados em Tempo Real:** Backend para receber mensagens via protocolos típicos (MQTT/HTTP), armazenando leituras por dispositivo e hora.
- **Dashboard Geográfico:** Mapa integrado a painel de dados; ao clicar, exibe últimos valores e status por cor.
- **Alertas e Notificações:** Configuração de limites e destaque visual quando valores saem do intervalo.
- **Relatórios e Histórico:** Consulta de histórico por período, com visualização em gráfico/tabela.

**Technologias:** Projeto full-stack. Front-end em Vue.js com integração de mapa via Mapbox/Leaflet. Back-end em Node.js (Express), servindo APIs REST e websockets para atualização em tempo real. Dispositivos simulados publicando via MQTT (scripts Python) em um broker; servidor Node subscrevendo e persistindo no banco. Banco de dados: MongoDB (documentos JSON com campos geoespaciais e índices geográficos). Projeto hospedado no GitHub (organização manolito-fatec), com Docker para padronizar ambiente (containers: Node.js, broker MQTT e MongoDB).

**Link:** Repositório GitHub – `manolito-fatec/geo-iot-2024-1`.

**Contribuições Pessoais:** Julio Freitas assumiu a função de Product Owner, coordenando uma equipe com desenvolvimento e IoT/hardware. Elaborou o plano do projeto alinhando objetivos e definiu escopo priorizando entregas de maior valor para demonstração (cadastro geográfico, mapa em tempo real, alertas). Apoiou decisões tecnológicas (uso de MQTT para simulação mais realista). Conduziu ritos ágeis (dailies, reviews), removeu impedimentos e realizou testes exploratórios como usuário final, validando integração entre frontend, backend e sensores simulados. Também colaborou na documentação (setup e execução) para facilitar reprodução e apresentação. Ao final, o GEO-IOT foi demonstrado em operação: sensores reportando dados que apareciam instantaneamente no mapa, evidenciando integração bem-sucedida e capacidade de coordenação em projeto multi-tecnologia (IoT, GIS e tempo real).

---

## Projeto 5: Stratify (Trabalho de Graduação – TG)

**Empresa/Cliente:** Projeto autoral (Trabalho de Graduação) – foco em inteligência de dados para tomada de decisão empresarial.

**Problema:** Organizações modernas acumulam volumes massivos de dados, mas ainda enfrentam o desafio de extrair valor estratégico. Em marketing e negócios, existe demanda por segmentar (estratificar) bases grandes de clientes/produtos/operações em grupos significativos para direcionar ações específicas. Métodos tradicionais podem ser manuais e lentos (planilhas, regras estáticas), suscetíveis a erros e incapazes de capturar correlações complexas. Identificou-se a necessidade de uma ferramenta que automatize a estratificação aplicando técnicas de inteligência de dados (clusterização, estatística e aprendizado de máquina) e apresente resultados compreensíveis para gestores. Em resumo: como transformar dados brutos e heterogêneos em segmentos úteis para decisões?

**Objetivo:** Desenvolver uma API Backend robusta para segmentação de dados, integrável a diferentes front-ends e sistemas corporativos. Objetivos específicos:

- Ingerir e tratar conjuntos de dados heterogêneos (ex.: clientes com idade, renda, histórico de compras, interações etc.).
- Aplicar algoritmos de estratificação (K-Means, DBSCAN, métodos hierárquicos) ou regras de negócio (faixas, condições).
- Fornecer métricas e insights sobre segmentos (quantidade, perfil médio, estatísticas como média/mediana/distribuições).
- Expor resultados via endpoints RESTful seguros, com exportação (JSON/CSV) para integração com BI.
- Automatizar atualização das segmentações quando novos dados forem inseridos (uso contínuo, dataset dinâmico).

Em síntese, o Stratify é um “motor de segmentação de dados”, consolidando conhecimentos de banco de dados, backend e análise de dados adquiridos no curso.

**Funcionalidades:** Sendo uma solução focada em backend (API), as funcionalidades se concentram em processamento e disponibilização de dados estratificados:

- **Upload de Dataset & Schema Configurável:** Endpoint para envio de dataset (CSV/JSON) com metadados de esquema (colunas e tipos). Validação de consistência e tratamento básico de valores ausentes.
- **Trigger de Estratificação:** Endpoint para iniciar estratificação com parâmetros (algoritmo, número de clusters `k`, regras/limiares de segmentação).
- **Monitoramento de Processo:** Retorno de um `process_id` e consulta de status (pendente, processando, concluído, falhou), via endpoint e/ou webhook.
- **Resultado de Segmentação:** Endpoints de consulta dos resultados:
  - Lista de segmentos (id e tamanho).
  - Centroides/descrição do segmento (ou critérios de regras).
  - Métricas por segmento (estatísticas e indicadores).
  - Associação de cada registro a um segmento (inclui exportação com coluna `segmento`).
- **Histórico e Comparação:** Armazenamento de versões e comparação de segmentações (mudanças por novos dados/novos parâmetros).
- **Segurança e Multi-tenant:** Autenticação e isolamento por usuário/empresa.

**Tecnologias:** O Stratify foi desenvolvido com foco em performance e capacidade de lidar com dados consideráveis.

- **Backend:** Python + FastAPI (API REST e regras de negócio).
- **Processamento/ML:** pandas, numpy, scikit-learn.
- **Persistência:** PostgreSQL (metadados/configurações/resultados agregados) + MongoDB (dados brutos/intermediários).
- **Escalabilidade (opcional):** Apache Spark (modo standalone) para datasets grandes.
- **Assíncrono:** Celery + Redis (fila e execução de tarefas).
- **Segurança:** JWT (autenticação).
- **Infra:** Docker + Docker Compose.
- **Doc:** OpenAPI/Swagger do FastAPI.
- **Versionamento/CI:** GitHub (organização QuantumBitBR).

**Link:** Repositórios GitHub – `QuantumBitBR/API_5SEM` (documentação/configuração) e `QuantumBitBR/API_5SEM_BACK` (código fonte do backend Stratify).

**Contribuições Pessoais:** Julio Freitas foi Desenvolvedor Backend líder no projeto Stratify, sendo o principal responsável pelo core do sistema de segmentação de dados. Principais contribuições:

- **Arquitetura do Sistema:** Desenho de arquitetura em camadas (ingestão, processamento e exposição de resultados), com separação modular para facilitar testes e evolução.
- **Implementação de Algoritmos:** Integração do scikit-learn, execução dinâmica de K-Means conforme parâmetros, otimização de pré-processamento (normalização, outliers), uso de K-Means++ e critérios de parada, além de métricas como *silhouette score* para apoiar escolha de `k`.
- **Endpoints RESTful:** Upload de dataset, trigger de segmentação, paginação/filtros na consulta, tratamento robusto de erros e retornos REST adequados.
- **Assíncrono e Escalabilidade:** Configuração do Celery e criação de tarefas assíncronas para execução dos algoritmos, com retorno imediato de `process_id` e endpoints de status; testes de estresse com múltiplas segmentações.
- **Integração com Bancos:** Modelagem no PostgreSQL (usuários, datasets, resultados agregados) e estratégia no MongoDB (dados brutos), otimizando consultas com projeções e seleção de campos.
- **Segurança e Deploy:** JWT, boas práticas (hash de senha, CORS), Docker/Compose e variáveis de ambiente para integração de serviços e reprodução do ambiente.
- **Testes e Documentação:** Testes unitários e integrados (fluxo completo upload → segmentação → consulta), CI no GitHub e documentação (README, exemplos de request/response, relato técnico de decisões e resultados).

Como demonstração de resultado, foram realizados experimentos com dados reais de exemplo (ex.: dataset público de clientes), produzindo segmentos coerentes (ex.: “clientes ocasionais de baixo gasto”, “clientes fiéis de alto valor”), úteis para marketing e estratégia. A API mostrou capacidade de recomputar segmentos após inserção de novos dados, atendendo aos objetivos de automação.

---

## Fonte dos Dados dos Projetos

As informações apresentadas sobre cada projeto foram baseadas nos repositórios de código correspondentes no GitHub e em documentos fornecidos pelas equipes de desenvolvimento. Em especial, detalhes do TG Manager foram extraídos do README oficial do projeto (referência: github.com / github.com), e conceitos relacionados ao Dom Rock Pipeline foram fundamentados em materiais da plataforma Dom Rock (referência: domrock.net). Esses projetos acadêmicos refletem cenários reais, combinando aprendizado teórico e aplicação prática, mostrando a evolução do aluno de tarefas mais simples de desenvolvimento para a integração de soluções complexas e focadas em inteligência de dados no Trabalho de Graduação.
