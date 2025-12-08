# Proposta-de-Experimento-para-TCC

## 1. Identificação básica


### 1.1 Título do experimento

Análise Comparativa de Performance e Qualidade de Software: Anotadores Genômicos Web-based versus Desktop em Genomas Bacterianos

---

### 1.2 ID / código

EXP-TCC-ANNOT-2025-004

---

### 1.3 Versão do documento e histórico de revisão

- **v1.0** (21/11/2025): Criação inicial do documento com identificação básica e contexto
- **v2.0** (22/11/2025): Definiçao de Escopo, Objetivo
- **v2.5** (23/11/2025): Definiçao de Stakeholders/Impacto, Riscos de alto nível, premissas e critérios de sucesso
- **v3.0** (28/11/2025): Modelo conceitual e hipóteses; Variáveis, fatores, tratamentos e objetos de estudo; Desenho experimental
- **v4.0** (02/12/2025): População, sujeitos e amostragem; Instrumentação e protocolo operacional; Plano de análise de dados (pré-execução)

---
    
### 1.4 Datas (criação, última atualização)

- **Data de criação:** 21/11/2025
    
- **Última atualização:** 02/12/2025
    
---

### 1.5 Autores (nome, área, contato)

- **Autor principal:** Vinicius Salles de Oliveira - Graduando em Engenharia de Software - [vinicius.oliveira.1444802@sga.pucminas.br](mailto:vinicius.oliveira.1444802@sga.pucminas.br)
    
- **Orientador:** Prof. Danilo de Quadros Maia Filho - Departamento de Engenharia de Software - [1514571@sga.pucminas.br](mailto:1514571@sga.pucminas.br)
    
---

### 1.6 Responsável principal (PI / dono do experimento)

**Vinicius Salles de Oliveira** - Responsável pela concepção, execução e análise dos resultados do experimento

---

### 1.7 Projeto / produto / iniciativa relacionada

Este experimento está vinculado ao Trabalho de Conclusão de Curso (TCC) do curso de Engenharia de Software da PUC Minas, dentro da disciplina de Estatística e Probabilidade. O estudo visa aplicar conceitos de engenharia de software na avaliação sistemática de ferramentas de bioinformática, demonstrando como princípios de análise de desempenho e qualidade de software podem ser aplicados em domínios interdisciplinares.

---

## 2. Contexto e problema

### 2.1 Descrição do problema / oportunidade

A anotação de genomas bacterianos representa um desafio de engenharia de software aplicada à bioinformática, onde a escolha entre diferentes arquiteturas de software (web-based vs desktop) impacta diretamente a eficiência e qualidade dos resultados.

**Problema observado:**

- Ferramentas web-based (RAST, DFAST) seguem arquitetura cliente-servidor, oferecendo Software as a Service (SaaS), mas introduzem latência de rede e dependência de disponibilidade do servidor
    
- Ferramentas desktop (Prokka) seguem arquitetura standalone, oferecendo melhor controle e performance local, mas exigem gerenciamento de dependências e recursos computacionais próprios
    

**Sintomas identificados do ponto de vista de Engenharia de Software:**

- Falta de métricas objetivas de performance (tempo de resposta, throughput)
    
- Ausência de análise comparativa de qualidade de software (confiabilidade, eficiência, manutenibilidade)
    
- Decisões de arquitetura baseadas em preferências subjetivas ao invés de dados empíricos
    

**Oportunidade:** Aplicar metodologias de engenharia de software para realizar benchmarking sistemático, gerando métricas quantitativas que suportem decisões arquiteturais baseadas em evidências.

---

### 2.2 Contexto organizacional e técnico

**Ambiente organizacional:**

- **Tipo de organização:** Instituição de ensino superior - PUC Minas
    
- **Departamento:** Engenharia de Software
    
- **Contexto acadêmico:** Trabalho de conclusão de curso com aplicação prática de conceitos de engenharia de software em domínio interdisciplinar
    

**Contexto técnico:**

- **Domínio de aplicação:** Sistemas de bioinformática para processamento de dados genômicos
    
**Paradigmas de software avaliados:**
    
- Aplicações web (arquitetura cliente-servidor, RESTful APIs)

- Aplicações desktop (arquitetura monolítica, processamento local)
    
**Infraestrutura de teste:**
    
- Hardware: Processador AMD Ryzen 5 5600, 32GB Memoria RAM DDR4 3200mhz, RTX 4060 TI 8GB 
    
- Software: Windows 11 como SO base
    
- Rede: Conexão de 1Gbps para testes de ferramentas web
    
**Ferramentas sob análise:**
    
- RAST: Implementado em Perl, arquitetura web service
    
- DFAST: Implementado em Python, interface web moderna
    
- Prokka: Implementado em Perl, pipeline de linha de comando
    

**Processo de desenvolvimento:** O experimento seguirá metodologia ágil com sprints semanais para coleta e análise incremental de dados, aplicando conceitos de DevOps para automação dos testes.

---

### 2.3 Trabalhos e evidências prévias (internos e externos)

**Trabalhos Externos Relevantes:**

1.  **Seemann (2014)** - "Prokka: rapid prokaryotic genome annotation"
    - Demonstrou importância da otimização algorítmica para performance
    - Arquitetura modular permitindo extensibilidade

2.  **Aziz et al. (2008)** - "The RAST Server"
    - Exemplo de arquitetura escalável para processamento distribuído
    - Implementação de filas de processamento para gerenciar carga
    
3.  **Tanizawa et al. (2018)** - "DFAST"
    - Design de interface focado em usabilidade
    - API RESTful para integração com outros sistemas

4.  **Estudos de benchmarking em software (similares):**
    - TPC (Transaction Processing Performance Council) para bancos de dados
    - SPEC (Standard Performance Evaluation Corporation) para sistemas
    

**Evidências do contexto de Engenharia de Software:**

- Crescente demanda por engenheiros de software em bioinformática
    
- Necessidade de profissionais que entendam tanto aspectos técnicos quanto do domínio
    
- Importância de métricas objetivas para tomada de decisão em arquitetura de software
    

**Lacuna identificada:**

*   Ausência de benchmarks padronizados para ferramentas de bioinformática
    
*   Falta de análise sob perspectiva de qualidade de software (ISO/IEC 25010)
    
*   Necessidade de metodologia replicável para avaliação de ferramentas similares
    
---

### 2.4 Referencial teórico e empírico essencial

**Conceitos de Engenharia de Software aplicados:**

1.  **Métricas de qualidade de software (ISO/IEC 25010):**
    - **Eficiência de performance:** Tempo de resposta, utilização de recursos
    - **Confiabilidade:** Disponibilidade, tolerância a falhas
    - **Usabilidade:** Facilidade de aprendizado, operabilidade
    - **Manutenibilidade:** Modularidade, reusabilidade
    
2.  **Padrões arquiteturais relevantes:**
    - **Cliente-Servidor:** Separação de responsabilidades, escalabilidade horizontal
    - **Pipeline:** Processamento sequencial de dados, comum em bioinformática
    - **Microserviços vs Monolito:** Trade-offs de complexidade vs controle 

3.  **Engenharia de Performance:**
    - **Latência:** Tempo entre requisição e resposta
    - **Throughput:** Volume de processamento por unidade de tempo
    - **Escalabilidade:** Capacidade de lidar com aumento de carga
    
**Fundamentos teóricos de análise experimental:**

1.  **Design de Experimentos em Software (Wohlin et al., 2012):**
    - Variáveis controladas vs não controladas
    - Replicação e validade estatística
    - Ameaças à validade

2.  **Benchmarking de Software (Sim et al., 2003):**
  - Definição de workloads representativos
  - Métricas padronizadas
  - Reprodutibilidade

3.  **Análise estatística aplicada:**
    - Testes de hipóteses para comparação de médias
    - Análise de variância (ANOVA) para múltiplos tratamentos
    - Intervalos de confiança para estimativas

**Resultados empíricos relevantes para Engenharia de Software:**

- Overhead de comunicação em aplicações web: 10-30% do tempo total (Nielsen, 2010)
    
- Paralelização efetiva limitada a 60-80% em pipelines de bioinformática (Amdahl's Law)
    
- Custo de manutenção representa 60-80% do ciclo de vida do software (Boehm, 1987)
    

**Hipóteses fundamentadas em Engenharia de Software:**

1.  Ferramentas desktop terão menor latência devido à eliminação do overhead de rede
    
2.  Ferramentas web terão melhor manutenibilidade por centralização de atualizações
    
3.  A diferença de performance será mais significativa com aumento da carga (genomas maiores)

1.  Ferramentas desktop serão mais rápidas para genomas individuais (menor overhead de rede)
    
2.  Ferramentas web serão mais consistentes em disponibilidade de atualizações
    
3.  A diferença de performance será mais pronunciada em genomas grandes (>5 Mb)

---

## 3. Objetivos e questões (Goal / Question / Metric)

### 3.1 Objetivo geral (Goal template)

Analisar ferramentas de anotação genômica (web-based vs desktop) com o propósito de comparar em relação a performance, qualidade de anotação e usabilidade do ponto de vista de engenheiros de software e bioinformatas no contexto de projetos de genômica bacteriana em ambiente acadêmico e de pesquisa.

---

### 3.2 Objetivos específicos

**O1:** Avaliar a eficiência de performance das ferramentas em termos de tempo de processamento e utilização de recursos computacionais.

**O2:** Analisar a qualidade e completude das anotações produzidas por cada ferramenta em diferentes tamanhos de genomas bacterianos.

**O3:** Investigar aspectos de usabilidade e facilidade de integração das ferramentas em pipelines de análise existentes.

**O4:** Examinar a confiabilidade e disponibilidade das ferramentas sob diferentes condições de carga e conectividade.

### 3.3 Questões de pesquisa / de negócio

#### Para O1 - Eficiência de Performance:

- **Q1.1:** Qual é a diferença no tempo total de processamento entre ferramentas web-based e desktop?
- **Q1.2:** Como o tamanho do genoma afeta o tempo de processamento em cada tipo de ferramenta?
- **Q1.3:** Qual é o consumo de recursos computacionais (CPU, memória) de cada ferramenta?

#### Para O2 - Qualidade da Anotação:

- **Q2.1:** Qual ferramenta identifica o maior número de elementos genômicos (CDS, RNA)?
- **Q2.2:** Qual é o nível de concordância entre as anotações produzidas pelas diferentes ferramentas?
- **Q2.3:** Como a completude da anotação (medida por BUSCO) varia entre as ferramentas?

#### Para O3 - Usabilidade e Integração:

- **Q3.1:** Qual é o esforço necessário para instalação e configuração de cada ferramenta?
- **Q3.2:** Quão facilmente os resultados podem ser integrados em pipelines downstream?
- **Q3.3:** Qual é a curva de aprendizado para usuários com diferentes níveis de experiência?

#### Para O4 - Confiabilidade e Disponibilidade:

- **Q4.1:** Qual é a taxa de sucesso na conclusão de tarefas de anotação?
- **Q4.2:** Como variações na conectividade afetam ferramentas web-based?
- **Q4.3:** Qual é a frequência de atualizações e manutenção de cada ferramenta?

---

### 3.4 Métricas associadas (GQM)

#### Tabela GQM - Goal Question Metric

| Objetivo                           | Pergunta                                          | Métricas                                                                                     |
| ---------------------------------- | ------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| **O1 - Eficiência de Performance** | Q1.1: Diferença no tempo total de processamento   | M1: Tempo total de execução (minutos)<br>M2: Tempo de overhead de rede (minutos)             |
|                                    | Q1.2: Impacto do tamanho do genoma                | M1: Tempo total de execução (minutos)<br>M3: Taxa de processamento (Mbp/minuto)              |
|                                    | Q1.3: Consumo de recursos computacionais          | M4: Uso de CPU (%)<br>M5: Uso de memória RAM (GB)                                            |
| **O2 - Qualidade da Anotação**     | Q2.1: Número de elementos genômicos identificados | M6: Número de CDS anotadas<br>M7: Número de RNAs anotados                                    |
|                                    | Q2.2: Concordância entre ferramentas              | M8: Índice de concordância Kappa<br>M9: Percentual de sobreposição de genes                  |
|                                    | Q2.3: Completude da anotação                      | M10: Score BUSCO (%)<br>M11: Percentual de genes com função atribuída                        |
| **O3 - Usabilidade e Integração**  | Q3.1: Esforço de instalação e configuração        | M12: Tempo de setup (horas)<br>M13: Número de dependências                                   |
|                                    | Q3.2: Facilidade de integração                    | M14: Número de formatos de saída suportados<br>M15: Compatibilidade com padrões (0-10)       |
|                                    | Q3.3: Curva de aprendizado                        | M16: Tempo para primeira anotação bem-sucedida (minutos)<br>M17: Taxa de erro de usuário (%) |
| **O4 - Confiabilidade**            | Q4.1: Taxa de sucesso                             | M18: Taxa de conclusão bem-sucedida (%)<br>M19: Número de falhas por experimento             |
|                                    | Q4.2: Impacto da conectividade                    | M20: Tempo adicional com conexão lenta (minutos)<br>M21: Taxa de timeout (%)                 |
|                                    | Q4.3: Frequência de atualizações                  | M22: Número de atualizações por ano<br>M23: Tempo desde última atualização (dias)            |

#### Tabela de Descrição das Métricas

| ID  | Métrica                       | Descrição                                                      | Unidade        |
| --- | ----------------------------- | -------------------------------------------------------------- | -------------- |
| M1  | Tempo total de execução       | Tempo decorrido desde o início até a conclusão da anotação     | minutos        |
| M2  | Tempo de overhead de rede     | Tempo gasto em transmissão de dados para ferramentas web       | minutos        |
| M3  | Taxa de processamento         | Velocidade de processamento relativa ao tamanho do genoma      | Mbp/minuto     |
| M4  | Uso de CPU                    | Percentual médio de utilização do processador durante execução | %              |
| M5  | Uso de memória RAM            | Quantidade máxima de memória utilizada durante o processo      | GB             |
| M6  | Número de CDS anotadas        | Total de sequências codificadoras identificadas                | quantidade     |
| M7  | Número de RNAs anotados       | Total de RNAs (tRNA, rRNA, etc.) identificados                 | quantidade     |
| M8  | Índice de concordância Kappa  | Medida estatística de concordância entre anotadores            | 0 a 1          |
| M9  | Percentual de sobreposição    | Proporção de genes identificados por múltiplas ferramentas     | %              |
| M10 | Score BUSCO                   | Completude baseada em genes ortólogos universais               | %              |
| M11 | Genes com função atribuída    | Proporção de genes com anotação funcional                      | %              |
| M12 | Tempo de setup                | Tempo necessário para instalação e configuração inicial        | horas          |
| M13 | Número de dependências        | Quantidade de software/bibliotecas necessárias                 | quantidade     |
| M14 | Formatos de saída             | Número de formatos de arquivo suportados para export           | quantidade     |
| M15 | Compatibilidade com padrões   | Aderência a padrões da indústria (GenBank, GFF3, etc.)         | escala 0-10    |
| M16 | Tempo primeira anotação       | Tempo para usuário novato completar primeira tarefa            | minutos        |
| M17 | Taxa de erro de usuário       | Frequência de erros cometidos por usuários durante uso         | %              |
| M18 | Taxa de conclusão             | Percentual de tarefas completadas com sucesso                  | %              |
| M19 | Número de falhas              | Quantidade de falhas durante os experimentos                   | quantidade     |
| M20 | Tempo adicional conexão lenta | Aumento no tempo com redução de 90% na velocidade              | minutos        |
| M21 | Taxa de timeout               | Frequência de timeouts em ferramentas web                      | %              |
| M22 | Atualizações por ano          | Frequência de releases e updates da ferramenta                 | quantidade/ano |
| M23 | Tempo última atualização      | Dias desde a última versão disponibilizada                     | dias           |

---

## 4. Escopo e contexto do experimento

### 4.1 Escopo funcional / de processo (incluído e excluído)

#### Incluído no escopo:

- Análise de 3 ferramentas principais: RAST (web), DFAST (web) e Prokka (desktop)
- Anotação estrutural de genomas bacterianos completos
- Genomas de 3 categorias de tamanho: pequeno (<2 Mb), médio (2-5 Mb), grande (>5 Mb)
- Métricas quantitativas de performance, qualidade e usabilidade
- Automação da coleta de dados via scripts
- Análise estatística comparativa dos resultados

#### Excluído do escopo:

- Anotação funcional detalhada (vias metabólicas complexas)
- Genomas de archaea, eucariotos ou vírus
- Análise de genomas em draft ou com múltiplos contigs
- Comparação de custos financeiros (todas as ferramentas são gratuitas)
- Modificação ou otimização das ferramentas
- Análise de segurança ou privacidade de dados

---

### 4.2 Contexto do estudo (tipo de organização, projeto, experiência)

#### Tipo de organização:

- Universidade de grande porte (PUC Minas)
- Ambiente acadêmico com foco em pesquisa e ensino
- Infraestrutura compartilhada de TI

#### Tipo de projeto:

- Trabalho de Conclusão de Curso em Engenharia de Software
- Duração: 4 meses (1 semestre acadêmico)
- Natureza: Pesquisa aplicada com componente experimental

#### Perfil de experiência:

- Pesquisador principal: Graduando em Engenharia de Software com conhecimentos básicos em bioinformática
- Orientador: Professor com experiência em estatística e análise de dados
- Usuários-alvo: Estudantes e pesquisadores com variados níveis de experiência técnica

---

### 4.3 Premissas

- **Disponibilidade de infraestrutura:** O hardware especificado (AMD Ryzen 5 5600, 32GB RAM) estará disponível durante todo o período do experimento
- **Estabilidade das ferramentas:** As versões das ferramentas permanecerão estáveis durante o período de coleta
- **Acesso à internet:** Conexão de 1Gbps estará consistentemente disponível para testes web
- **Disponibilidade de dados:** Genomas de referência do NCBI permanecerão acessíveis
- **Servidores web operacionais:** RAST e DFAST manterão disponibilidade mínima de 95%
- **Conhecimento prévio:** O pesquisador possui conhecimentos básicos de linha de comando e biologia molecular

---

### 4.4 Restrições

#### Temporais:

- Prazo máximo: 16 semanas (1 semestre letivo)
- Coleta de dados limitada a horário comercial (8h-18h)

#### Técnicas:

- Hardware limitado a uma workstation
- Sem acesso a cluster computacional para testes em paralelo
- Sistema operacional restrito a Windows 11

#### Orçamentárias:

- Orçamento zero (uso apenas de ferramentas gratuitas)
- Sem possibilidade de contratar serviços cloud adicionais

#### Organizacionais:

- Experimento deve seguir calendário acadêmico
- Necessidade de aprovação do comitê de ética para publicação

---

### 4.5 Limitações previstas

**Validade externa limitada por:**

- **Contexto específico:** Resultados podem não se aplicar a ambientes empresariais com infraestrutura diferente
- **Seleção de genomas:** Foco em bactérias pode não representar outros organismos
- **Versões específicas:** Resultados vinculados às versões atuais das ferramentas
- **Ambiente Windows:** Possíveis diferenças de performance em Linux/Mac
- **Escala limitada:** Teste com número limitado de genomas pode não capturar todos os cenários
- **Perfil de usuário:** Foco em ambiente acadêmico pode não refletir uso industrial

---

## 5. Stakeholders e impacto esperado

### 5.1 Stakeholders principais

1. **Pesquisador Principal (Vinicius Salles de Oliveira)**

   - Interesse direto no sucesso do TCC
   - Responsável pela execução e análise

2. **Orientador (Prof. Danilo Maia)**

   - Interesse na qualidade acadêmica do trabalho
   - Validação metodológica e estatística

3. **Comunidade de Bioinformática da PUC Minas**

   - Potenciais usuários dos resultados
   - Interessados em otimizar seus workflows

4. **Desenvolvedores de Software em Bioinformática**

   - Interesse em métricas de performance
   - Insights para melhorias arquiteturais

5. **Estudantes de Engenharia de Software**

   - Exemplo de aplicação interdisciplinar
   - Metodologia replicável para outros domínios

6. **Coordenação do Curso**
   - Interesse em trabalhos de qualidade
   - Demonstração de competências do egresso

---

### 5.2 Interesses e expectativas dos stakeholders

| Stakeholder                   | Interesses                                                                                               | Expectativas                                                                                       |
| ----------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| **Pesquisador Principal**     | - Conclusão bem-sucedida do TCC<br>- Aprendizado de métodos experimentais<br>- Publicação dos resultados | - Resultados estatisticamente significativos<br>- Documento bem estruturado<br>- Nota satisfatória |
| **Orientador**                | - Qualidade metodológica<br>- Rigor estatístico<br>- Contribuição científica                             | - Seguimento do cronograma<br>- Análises corretas<br>- Escrita clara                               |
| **Comunidade Bioinformática** | - Recomendações práticas<br>- Benchmarks confiáveis<br>- Scripts reutilizáveis                           | - Resultados aplicáveis<br>- Documentação clara<br>- Código disponível                             |
| **Desenvolvedores**           | - Métricas de performance<br>- Identificação de gargalos<br>- Comparações justas                         | - Metodologia replicável<br>- Dados brutos disponíveis<br>- Análise imparcial                      |
| **Estudantes**                | - Exemplo de TCC<br>- Metodologia clara<br>- Interdisciplinaridade                                       | - Documentação didática<br>- Código comentado<br>- Apresentação clara                              |
| **Coordenação**               | - Qualidade do trabalho<br>- Cumprimento de prazos<br>- Inovação                                         | - TCC aprovado<br>- Apresentação profissional<br>- Possível publicação                             |

---

### 5.3 Impactos potenciais no processo / produto

#### Impactos durante a execução:

- **Carga computacional:** Uso intensivo da workstation durante testes (estimado 200 horas de processamento)
- **Tráfego de rede:** Upload/download de ~5GB de dados genômicos
- **Tempo do pesquisador:** 20 horas semanais dedicadas ao projeto
- **Fila em servidores web:** Possível impacto mínimo nas filas do RAST/DFAST

#### Impactos pós-experimento:

- **Otimização de workflows:** Laboratórios podem ajustar escolha de ferramentas
- **Economia de tempo:** Redução estimada de 30% no tempo de decisão sobre ferramentas
- **Padronização:** Possível adoção de ferramenta padrão no departamento
- **Publicações futuras:** Base para artigos e apresentações em conferências
- **Material didático:** Incorporação dos resultados em disciplinas de bioinformática

---

## 6. Riscos de alto nível, premissas e critérios de sucesso

### 6.1 Riscos de alto nível (negócio, técnicos, etc.)

| ID  | Risco                                             | Probabilidade | Impacto    | Mitigação                                                                      |
| --- | ------------------------------------------------- | ------------- | ---------- | ------------------------------------------------------------------------------ |
| R1  | Indisponibilidade dos servidores web (RAST/DFAST) | Média         | Alto       | Agendar testes em múltiplos períodos; ter plano B com ferramentas alternativas |
| R2  | Falha de hardware da workstation                  | Baixa         | Muito Alto | Backup diário dos dados; possibilidade de usar computador pessoal              |
| R3  | Mudanças nas versões das ferramentas              | Média         | Médio      | Documentar versões exatas; containers Docker se possível                       |
| R4  | Atraso no cronograma por complexidade técnica     | Alta          | Alto       | Buffer de 2 semanas; início antecipado da coleta                               |
| R5  | Resultados inconclusivos estatisticamente         | Média         | Alto       | Aumentar tamanho amostral se necessário; consultar estatístico                 |
| R6  | Dificuldades com instalação do Prokka no Windows  | Alta          | Médio      | WSL2 como alternativa; máquina virtual Linux                                   |
| R7  | Sobrecarga de disciplinas do semestre             | Média         | Médio      | Planejamento semanal rigoroso; automação máxima                                |
| R8  | Dados corrompidos ou perda de resultados          | Baixa         | Alto       | Versionamento Git; backup em nuvem; checksums                                  |

---

### 6.2 Critérios de sucesso globais (go / no-go)

#### Critérios GO (prosseguir):

- Coleta bem-sucedida de dados para pelo menos 15 dos 18 genomas planejados  
- Diferenças estatisticamente significativas (p < 0.05) em pelo menos 50% das métricas  
- Todas as três ferramentas funcionais e gerando anotações válidas  
- Reprodutibilidade confirmada com subset de teste  
- Documentação completa permitindo replicação

#### Critérios NO-GO (reavaliar/parar):

- Menos de 12 genomas anotados com sucesso  
- Falha crítica em mais de uma ferramenta  
- Impossibilidade de coletar métricas-chave (tempo, qualidade)  
- Resultados não reprodutíveis em verificação  
- Atraso superior a 4 semanas no cronograma

---

### 6.3 Critérios de parada antecipada (pré-execução)

O experimento deve ser adiado ou cancelado se:

#### Infraestrutura:

- Workstation indisponível por mais de 2 semanas
- Conexão internet instável (<100 Mbps) por período prolongado
- Impossibilidade de instalar ferramentas necessárias

#### Disponibilidade de dados:

- NCBI inacessível por mais de 1 semana
- Mudanças significativas no formato dos genomas de referência
- Restrições legais ao uso dos dados

#### Ferramentas:

- Descontinuação de qualquer uma das 3 ferramentas principais
- Mudanças radicais na interface/API que invalidem o protocolo
- Requisitos de licença/pagamento introduzidos

#### Acadêmico:

- Mudança significativa nos requisitos do TCC
- Indisponibilidade do orientador
- Problemas de saúde do pesquisador

#### Ético/Legal:

- Não aprovação pelo comitê de ética (se aplicável)
- Questões de propriedade intelectual sobre os scripts
- Conflitos com políticas da universidade

---

## 7. Modelo conceitual e hipóteses

### 7.1 Modelo conceitual do experimento

O modelo conceitual deste experimento baseia-se na premissa de que diferentes arquiteturas de software (web-based vs desktop) apresentam trade-offs significativos em termos de performance, qualidade e usabilidade quando aplicadas ao domínio de anotação genômica.

**Modelo proposto:**

```
Arquitetura de Software → Métricas de Qualidade de Software → Decisão de Adoção
   ├── Web-based          ├── Performance (tempo, recursos)
   └── Desktop            ├── Qualidade (completude, acurácia)
                         └── Usabilidade (setup, integração)
```

**Relações esperadas:**

- **Ferramentas Desktop:** Maior velocidade de processamento local, mas maior complexidade de instalação
- **Ferramentas Web:** Menor barreira de entrada, mas dependência de conectividade e disponibilidade
- **Tamanho do genoma:** Fator modulador que amplifica diferenças de performance

---

### 7.2 Hipóteses formais (H0, H1)

#### H1 - Hipóteses sobre Performance

**Hipótese Nula (H₀₁):** Não há diferença significativa no tempo médio de processamento entre ferramentas web-based e desktop.

$$H_{0,1}: \mu_{tempo_{web}} = \mu_{tempo_{desktop}}$$

**Hipótese Alternativa (H₁₁):** Ferramentas desktop apresentam tempo médio de processamento significativamente menor que ferramentas web-based.

$$H_{1,1}: \mu_{tempo_{desktop}} < \mu_{tempo_{web}}$$

#### H2 - Hipóteses sobre Qualidade da Anotação

**Hipótese Nula (H₀₂):** Não há diferença significativa na completude da anotação (score BUSCO) entre os tipos de ferramentas.

$$H_{0,2}: \mu_{BUSCO_{web}} = \mu_{BUSCO_{desktop}}$$

**Hipótese Alternativa (H₁₂):** Existe diferença significativa na completude da anotação entre os tipos de ferramentas.

$$H_{1,2}: \mu_{BUSCO_{web}} \neq \mu_{BUSCO_{desktop}}$$

#### H3 - Hipóteses sobre Interação Tamanho × Arquitetura

**Hipótese Nula (H₀₃):** O efeito do tipo de arquitetura no tempo de processamento não depende do tamanho do genoma.

$$H_{0,3}: \text{Não há interação significativa entre arquitetura e tamanho}$$

**Hipótese Alternativa (H₁₃):** O efeito do tipo de arquitetura no tempo de processamento varia significativamente com o tamanho do genoma.

$$H_{1,3}: \text{Há interação significativa entre arquitetura e tamanho}$$

#### H4 - Hipóteses sobre Confiabilidade

**Hipótese Nula (H₀₄):** Não há diferença na taxa de sucesso entre ferramentas web-based e desktop.

$$H_{0,4}: \pi_{sucesso_{web}} = \pi_{sucesso_{desktop}}$$

**Hipótese Alternativa (H₁₄):** Ferramentas desktop apresentam maior taxa de sucesso que ferramentas web-based.

$$H_{1,4}: \pi_{sucesso_{desktop}} > \pi_{sucesso_{web}}$$

---

### 7.3 Nível de significância e considerações de poder

- **Nível de significância (α):** 0,05 para todos os testes
- **Poder estatístico desejado:** 0,80 (80%)
- **Tamanho do efeito esperado:**
  - Para tempo: d = 0,8 (grande)
  - Para qualidade: d = 0,5 (médio)
- **Correção para múltiplas comparações:** Bonferroni (α ajustado = 0,0125 para 4 hipóteses principais)

**Cálculo de tamanho amostral:** Com base no poder desejado e tamanho do efeito, são necessários pelo menos 18 genomas (6 por categoria de tamanho) para detectar diferenças significativas.

---

## 8. Variáveis, fatores, tratamentos e objetos de estudo

### 8.1 Objetos de estudo

Os objetos de estudo são genomas bacterianos completos obtidos do NCBI RefSeq, selecionados para representar diversidade taxonômica e variação de tamanho:

- 18 genomas bacterianos divididos em três categorias:
  - 6 genomas pequenos (<2 Mb)
  - 6 genomas médios (2-5 Mb)
  - 6 genomas grandes (>5 Mb)

---

### 8.2 Sujeitos / participantes (visão geral)

**Participante único:** O pesquisador principal (Vinicius Salles de Oliveira) executará todos os experimentos para garantir consistência na operação e eliminar variabilidade inter-operador.

**Perfil do operador:**

- Graduando em Engenharia de Software
- Conhecimento básico em bioinformática
- Familiaridade com linha de comando
- Treinamento prévio nas três ferramentas

---

### 8.3 Variáveis independentes (fatores) e seus níveis

#### Tabela de Fatores e Níveis

| Fator             | Descrição                                 | Níveis | Valores                                         |
| ----------------- | ----------------------------------------- | ------ | ----------------------------------------------- |
| Ferramenta        | Software de anotação genômica             | 3      | RAST (web), DFAST (web), Prokka (desktop)       |
| Tamanho do Genoma | Categoria de tamanho do genoma bacteriano | 3      | Pequeno (<2 Mb), Médio (2-5 Mb), Grande (>5 Mb) |

---

### 8.4 Tratamentos (condições experimentais)

#### Tabela de Tratamentos e Combinações

| ID Tratamento | Ferramenta | Tamanho | Arquitetura | Descrição                                  |
| ------------- | ---------- | ------- | ----------- | ------------------------------------------ |
| T1            | RAST       | Pequeno | Web         | Anotação web de genoma <2 Mb via RAST      |
| T2            | RAST       | Médio   | Web         | Anotação web de genoma 2-5 Mb via RAST     |
| T3            | RAST       | Grande  | Web         | Anotação web de genoma >5 Mb via RAST      |
| T4            | DFAST      | Pequeno | Web         | Anotação web de genoma <2 Mb via DFAST     |
| T5            | DFAST      | Médio   | Web         | Anotação web de genoma 2-5 Mb via DFAST    |
| T6            | DFAST      | Grande  | Web         | Anotação web de genoma >5 Mb via DFAST     |
| T7            | Prokka     | Pequeno | Desktop     | Anotação local de genoma <2 Mb via Prokka  |
| T8            | Prokka     | Médio   | Desktop     | Anotação local de genoma 2-5 Mb via Prokka |
| T9            | Prokka     | Grande  | Desktop     | Anotação local de genoma >5 Mb via Prokka  |

**Total:** 9 tratamentos (3 ferramentas × 3 tamanhos)

---

### 8.5 Variáveis dependentes (respostas)

#### Tabela de Variáveis Dependentes

| Variável              | Descrição                                    | Tipo     | Unidade       | Método de Medição         |
| --------------------- | -------------------------------------------- | -------- | ------------- | ------------------------- |
| Tempo Total           | Tempo desde início até conclusão da anotação | Contínua | minutos       | Cronômetro automatizado   |
| Taxa de Processamento | Velocidade relativa ao tamanho               | Contínua | Mbp/min       | Calculada (tamanho/tempo) |
| Uso de CPU            | Utilização média do processador              | Contínua | %             | Monitor de sistema        |
| Uso de RAM            | Memória máxima utilizada                     | Contínua | GB            | Monitor de sistema        |
| Número de CDS         | Total de genes codificadores                 | Discreta | quantidade    | Parser de arquivo GFF     |
| Score BUSCO           | Completude da anotação                       | Contínua | %             | Software BUSCO            |
| Taxa de Sucesso       | Conclusão bem-sucedida                       | Binária  | sucesso/falha | Observação direta         |
| Tempo de Setup        | Tempo para instalação/config                 | Contínua | horas         | Cronômetro manual         |

---

### 8.6 Variáveis de controle / bloqueio

#### Tabela de Variáveis de Controle

| Variável               | Descrição                          | Como será controlada                             |
| ---------------------- | ---------------------------------- | ------------------------------------------------ |
| Hardware               | Especificações do computador       | Mesmo equipamento para todos os testes           |
| Sistema Operacional    | Windows 11                         | Versão idêntica, atualizações pausadas           |
| Conexão de Rede        | Velocidade de internet             | 1 Gbps dedicado, testes em horários consistentes |
| Versão das Ferramentas | Versão específica de cada software | Documentada e fixada no início                   |
| Operador               | Pessoa executando o teste          | Mesmo operador (pesquisador principal)           |
| Ambiente               | Condições físicas                  | Mesma sala, temperatura controlada               |
| Carga do Sistema       | Outros processos rodando           | Sistema dedicado, processos mínimos              |

---

### 8.7 Possíveis variáveis de confusão conhecidas

#### Tabela de Variáveis de Confusão

| Variável                       | Descrição                             | Potencial Impacto              | Estratégia de Mitigação             |
| ------------------------------ | ------------------------------------- | ------------------------------ | ----------------------------------- |
| Carga do Servidor Web          | Variação na fila RAST/DFAST           | Aumento no tempo de resposta   | Testes em múltiplos horários        |
| Complexidade do Genoma         | Diferenças além do tamanho            | Variação na qualidade          | Seleção balanceada por complexidade |
| Atualizações de Banco de Dados | Updates durante experimento           | Mudança nos resultados         | Snapshot dos bancos de dados        |
| Efeito de Aprendizado          | Melhoria com repetição                | Redução artificial do tempo    | Randomização da ordem               |
| Variação de Rede               | Flutuações na conectividade           | Impacto em ferramentas web     | Monitoramento contínuo              |
| Cache                          | Dados em cache após primeira execução | Tempo artificialmente reduzido | Limpeza de cache entre testes       |

---

## 9. Desenho experimental

### 9.1 Tipo de desenho (completamente randomizado, blocos, fatorial, etc.)

**Tipo de desenho:** Fatorial completo 3×3 com medidas repetidas

**Justificativa:**

- Design fatorial permite avaliar efeitos principais (ferramenta, tamanho) e interações
- Medidas repetidas aumentam precisão estatística
- Todos os genomas são processados por todas as ferramentas

**Estrutura:**

- 2 fatores: Ferramenta (3 níveis) × Tamanho (3 níveis)
- 18 unidades experimentais (genomas)
- 54 observações totais (18 genomas × 3 ferramentas)

---

### 9.2 Randomização e alocação

**Esquema de randomização:**

- **Ordem dos genomas:** Randomização completa dentro de cada categoria de tamanho
- **Ordem das ferramentas:** Randomização para cada genoma usando Latin Square
- **Ordem temporal:** Distribuição aleatória ao longo dos dias de coleta

**Implementação:**

```python
# Pseudocódigo
import random
random.seed(42)  # Para reprodutibilidade

# Randomizar ordem de processamento
for categoria in ['pequeno', 'medio', 'grande']:
    genomas = random.shuffle(genomas_categoria)
    for genoma in genomas:
        ferramentas = random.shuffle(['RAST', 'DFAST', 'Prokka'])
        executar_experimento(genoma, ferramentas)
```

---

### 9.3 Balanceamento e contrabalanço

**Estratégias de balanceamento:**

1. **Balanceamento de características dos genomas:**

   - Diversidade taxonômica igual entre categorias
   - Conteúdo GC balanceado
   - Complexidade genômica similar dentro de cada categoria

2. **Contrabalanço temporal:**

   - Alternância entre ferramentas web e desktop
   - Distribuição uniforme ao longo do período
   - Pausas entre execuções para reset de sistema

3. **Controle de ordem:**
   - Matriz Latin Square 3×3 para sequência de ferramentas
   - Previne viés sistemático de ordem

---

### 9.4 Número de grupos e sessões

**Estrutura de grupos:**

- 3 grupos baseados em tamanho de genoma
- 6 genomas por grupo
- 3 sessões por genoma (uma para cada ferramenta)

**Distribuição temporal:**

- 54 sessões totais (18 genomas × 3 ferramentas)
- 3-4 sessões por dia para evitar fadiga
- 15-18 dias de coleta estimados

**Justificativa do tamanho amostral:**

- Poder estatístico de 0.80 para detectar diferenças grandes (d=0.8)
- 6 réplicas por combinação ferramenta×tamanho
- Margem para possíveis falhas ou exclusões

### Resumo do Design Experimental

**Matriz do Experimento:**

| Genoma | Categoria | Sessão 1      | Sessão 2      | Sessão 3      |
| ------ | --------- | ------------- | ------------- | ------------- |
| G1     | Pequeno   | RAST          | Prokka        | DFAST         |
| G2     | Pequeno   | DFAST         | RAST          | Prokka        |
| G3     | Pequeno   | Prokka        | DFAST         | RAST          |
| ...    | ...       | ...           | ...           | ...           |
| G18    | Grande    | (randomizado) | (randomizado) | (randomizado) |

Total: 54 execuções experimentais (18 genomas × 3 ferramentas)

**Análise planejada:**

- ANOVA two-way com medidas repetidas
- Testes post-hoc (Tukey HSD) para comparações múltiplas
- Análise de interação ferramenta × tamanho
- Correlações entre métricas de qualidade e performance

---

## 10. População, sujeitos e amostragem

### 10.1 População-alvo

A população-alvo deste experimento compreende **genomas bacterianos completos** disponíveis em repositórios públicos de bioinformática, especificamente:

**População primária (objetos de estudo):**
- Genomas bacterianos completos depositados no NCBI RefSeq
- Organismos procarióticos com genoma circular ou linear completamente sequenciado
- Representantes de diferentes filos bacterianos com relevância científica ou clínica

**População secundária (contexto de uso):**
- Pesquisadores e estudantes de bioinformática que utilizam ferramentas de anotação genômica
- Laboratórios acadêmicos com infraestrutura computacional típica (desktop/workstation)
- Projetos de genômica bacteriana em instituições de ensino superior

---

### 10.2 Critérios de inclusão de sujeitos

#### Para os genomas (objetos de estudo):

| Critério | Especificação |
|----------|---------------|
| **Status de montagem** | Genoma completo (Complete Genome) |
| **Qualidade** | N50 > 50 kb, sem contigs fragmentados |
| **Formato** | Arquivo FASTA disponível no NCBI RefSeq |
| **Organismo** | Bactéria (domínio Bacteria) |
| **Tamanho** | Entre 0,5 Mb e 12 Mb |
| **Anotação de referência** | Possuir anotação oficial do NCBI para validação |
| **Acessibilidade** | Disponível publicamente sem restrições de uso |

#### Para o operador do experimento:

| Critério | Especificação |
|----------|---------------|
| **Formação** | Graduando ou graduado em área de TI ou Biológicas |
| **Conhecimento técnico** | Familiaridade com linha de comando (terminal) |
| **Disponibilidade** | Mínimo de 20 horas semanais para o experimento |
| **Acesso** | Disponibilidade do hardware especificado |

---

### 10.3 Critérios de exclusão de sujeitos

#### Para os genomas:

| Critério de Exclusão | Justificativa |
|---------------------|---------------|
| Genomas em draft (rascunho) | Qualidade inconsistente pode afetar resultados |
| Genomas de plasmídeos isolados | Não representam genoma completo |
| Genomas de archaea ou eucariotos | Fora do escopo das ferramentas testadas |
| Genomas com contaminação reportada | Dados não confiáveis |
| Genomas menores que 0,5 Mb | Podem ser genomas incompletos ou endossimbiontes |
| Genomas maiores que 12 Mb | Raros em bactérias, possível contaminação |
| Genomas sem anotação de referência | Impossibilidade de validação |

#### Para o operador:

| Critério de Exclusão | Justificativa |
|---------------------|---------------|
| Envolvimento no desenvolvimento das ferramentas | Conflito de interesse |
| Falta de acesso estável à internet | Impossibilidade de testar ferramentas web |
| Incapacidade de completar treinamento prévio | Risco de erros operacionais |

---

### 10.4 Tamanho da amostra planejado (por grupo)

**Tamanho total da amostra:** 18 genomas bacterianos

**Distribuição por grupo:**

| Grupo | Tamanho do Genoma | Quantidade | Justificativa |
|-------|-------------------|------------|---------------|
| Grupo 1 | Pequeno (<2 Mb) | 6 genomas | Representar organismos minimalistas |
| Grupo 2 | Médio (2-5 Mb) | 6 genomas | Faixa mais comum em bactérias |
| Grupo 3 | Grande (>5 Mb) | 6 genomas | Representar organismos complexos |

**Justificativa estatística:**
- **Poder estatístico:** Com 6 réplicas por grupo e α=0,05, obtém-se poder de 0,80 para detectar efeitos grandes (d=0,8)
- **Análise de poder:** Calculado usando G*Power para ANOVA de medidas repetidas
- **Margem de segurança:** 18 genomas permitem até 3 exclusões mantendo poder adequado
- **Viabilidade:** Quantidade executável no prazo de 16 semanas

**Total de observações:** 54 (18 genomas × 3 ferramentas)

---

### 10.5 Método de seleção / recrutamento

**Método:** Amostragem estratificada por conveniência

**Procedimento de seleção:**

1. **Consulta ao NCBI RefSeq:**
- Acesso ao banco de dados de genomas bacterianos
- Filtro por "Complete Genome"
- Ordenação por data de depósito (mais recentes)

2. **Estratificação por tamanho:**
- Separação em três faixas de tamanho
- Seleção de 6 genomas por faixa

3. **Critérios de diversidade:**
- Máximo de 2 genomas do mesmo gênero
- Representação de pelo menos 4 filos diferentes
- Balanceamento de conteúdo GC (baixo, médio, alto)

4. **Validação final:**
- Verificação de disponibilidade dos arquivos
- Confirmação de qualidade da montagem
- Documentação dos metadados

**Genomas pré-selecionados:**

| ID | Organismo | Tamanho | Categoria | RefSeq |
|----|-----------|---------|-----------|--------|
| G1 | *Mycoplasma genitalium* | 0,58 Mb | Pequeno | NC_000908.2 |
| G2 | *Chlamydia trachomatis* | 1,04 Mb | Pequeno | NC_000117.1 |
| G3 | *Rickettsia prowazekii* | 1,11 Mb | Pequeno | NC_000963.1 |
| G4 | *Helicobacter pylori* | 1,67 Mb | Pequeno | NC_000915.1 |
| G5 | *Treponema pallidum* | 1,14 Mb | Pequeno | NC_021490.2 |
| G6 | *Borrelia burgdorferi* | 0,91 Mb | Pequeno | NC_001318.1 |
| G7 | *Escherichia coli* K-12 | 4,64 Mb | Médio | NC_000913.3 |
| G8 | *Bacillus subtilis* 168 | 4,21 Mb | Médio | NC_000964.3 |
| G9 | *Pseudomonas aeruginosa* | 6,26 Mb | Médio | NC_002516.2 |
| G10 | *Staphylococcus aureus* | 2,82 Mb | Médio | NC_007795.1 |
| G11 | *Salmonella enterica* | 4,88 Mb | Médio | NC_003197.2 |
| G12 | *Mycobacterium tuberculosis* | 4,41 Mb | Médio | NC_000962.3 |
| G13 | *Streptomyces coelicolor* | 8,67 Mb | Grande | NC_003888.3 |
| G14 | *Bradyrhizobium japonicum* | 9,10 Mb | Grande | NC_004463.1 |
| G15 | *Sorangium cellulosum* | 13,03 Mb | Grande | NC_010162.1 |
| G16 | *Rhodococcus jostii* | 9,70 Mb | Grande | NC_008268.1 |
| G17 | *Burkholderia xenovorans* | 9,73 Mb | Grande | NC_007951.1 |
| G18 | *Nocardia farcinica* | 6,29 Mb | Grande | NC_006361.1 |

---

### 10.6 Treinamento e preparação dos sujeitos

**Treinamento do operador (pesquisador principal):**

| Fase | Conteúdo | Duração | Método |
|------|----------|---------|--------|
| **Fase 1** | Fundamentos de anotação genômica | 4 horas | Estudo dirigido + tutoriais online |
| **Fase 2** | Operação do RAST | 2 horas | Tutorial oficial + prática |
| **Fase 3** | Operação do DFAST | 2 horas | Tutorial oficial + prática |
| **Fase 4** | Operação do Prokka | 3 horas | Documentação + instalação + prática |
| **Fase 5** | Scripts de automação | 4 horas | Desenvolvimento e teste |
| **Fase 6** | Ferramentas de monitoramento | 2 horas | Configuração e calibração |
| **Fase 7** | Estudo piloto | 8 horas | Execução completa com 3 genomas |

**Materiais de preparação:**
- Documentação oficial de cada ferramenta
- Artigos científicos de referência (Seemann, 2014; Aziz et al., 2008; Tanizawa et al., 2018)
- Checklist de verificação pré-experimento
- Scripts de automação documentados
- Vídeos tutoriais gravados pelo pesquisador

**Critérios de conclusão do treinamento:**
- Execução bem-sucedida de anotação em cada ferramenta
- Compreensão dos formatos de saída (GFF, GenBank, FASTA)
- Capacidade de interpretar logs de erro
- Familiaridade com scripts de coleta de métricas

---

## 11. Instrumentação e protocolo operacional

### 11.1 Instrumentos de coleta (questionários, logs, planilhas, etc.)

#### Tabela de Instrumentos de Coleta

| ID | Instrumento | Tipo | Descrição | Variáveis Coletadas |
|----|-------------|------|-----------|---------------------|
| I1 | **Script de Cronometragem** | Python | Registra timestamps de início/fim de cada execução | M1 (Tempo total), M2 (Overhead) |
| I2 | **Monitor de Sistema** | PowerShell/Python | Captura uso de CPU e RAM em intervalos de 5s | M4 (CPU), M5 (RAM) |
| I3 | **Parser de Resultados** | Python | Extrai contagens de features dos arquivos GFF/GenBank | M6 (CDS), M7 (RNAs) |
| I4 | **Planilha de Registro** | Excel/CSV | Registro manual de observações e incidentes | Todas |
| I5 | **Log de Execução** | TXT | Saída padrão e erros de cada ferramenta | M18 (Sucesso), M19 (Falhas) |
| I6 | **BUSCO** | Software | Avaliação de completude das anotações | M10 (Score BUSCO) |
| I7 | **Checklist de Sessão** | Google Forms | Registro estruturado de cada sessão experimental | Metadados |
| I8 | **Script de Comparação** | Python | Calcula concordância entre anotações | M8 (Kappa), M9 (Sobreposição) |
| I9 | **Monitor de Rede** | Wireshark/NetLimiter | Registra latência e throughput de rede | M2 (Overhead de rede) |
| I10 | **Repositório Git** | GitHub | Versionamento de scripts e dados | Backup, reprodutibilidade |

---

### 11.2 Materiais de suporte (instruções, guias)

#### Lista de Materiais de Suporte

| ID | Material | Formato | Conteúdo | Destinatário |
|----|----------|---------|----------|--------------|
| S1 | **Manual do Experimento** | PDF | Procedimentos detalhados, troubleshooting | Operador |
| S2 | **Guia Rápido RAST** | PDF (2 páginas) | Passo a passo de submissão e download | Operador |
| S3 | **Guia Rápido DFAST** | PDF (2 páginas) | Passo a passo de submissão e download | Operador |
| S4 | **Guia Rápido Prokka** | PDF (2 páginas) | Comandos e parâmetros essenciais | Operador |
| S5 | **Checklist Pré-Sessão** | PDF (1 página) | Verificações antes de cada execução | Operador |
| S6 | **Checklist Pós-Sessão** | PDF (1 página) | Verificações após cada execução | Operador |
| S7 | **Glossário de Termos** | PDF | Definições de termos técnicos | Operador |
| S8 | **FAQ de Problemas Comuns** | PDF | Soluções para erros frequentes | Operador |
| S9 | **Template de Relatório** | Word/MD | Estrutura para documentar resultados | Operador |
| S10 | **README dos Scripts** | Markdown | Documentação técnica dos scripts | Operador/Replicadores |

---

### 11.3 Procedimento experimental (protocolo – visão passo a passo)

#### Fluxograma do Experimento

#### Protocolo Detalhado Passo a Passo

**FASE 1: PREPARAÇÃO (Semanas 1-2)**

| Passo | Ação | Responsável | Duração | Entregável |
|-------|------|-------------|---------|------------|
| 1.1 | Download dos 18 genomas do NCBI RefSeq | Operador | 2 horas | Arquivos FASTA |
| 1.2 | Verificação de integridade (MD5) | Operador | 30 min | Log de verificação |
| 1.3 | Instalação do Prokka via WSL2 | Operador | 3 horas | Prokka funcional |
| 1.4 | Criação de conta no RAST | Operador | 15 min | Credenciais |
| 1.5 | Criação de conta no DFAST | Operador | 15 min | Credenciais |
| 1.6 | Desenvolvimento de scripts de automação | Operador | 8 horas | Scripts testados |
| 1.7 | Configuração de monitores de sistema | Operador | 2 horas | Monitores calibrados |
| 1.8 | Randomização da ordem de execução | Operador | 1 hora | Matriz randomizada |
| 1.9 | Revisão do protocolo com orientador | Orientador | 2 horas | Protocolo aprovado |

**FASE 2: ESTUDO PILOTO (Semana 3)**

| Passo | Ação | Responsável | Duração | Entregável |
|-------|------|-------------|---------|------------|
| 2.1 | Seleção de 3 genomas piloto (fora da amostra) | Operador | 30 min | Lista de genomas |
| 2.2 | Execução completa com genoma piloto 1 | Operador | 4 horas | Dados piloto |
| 2.3 | Execução completa com genoma piloto 2 | Operador | 4 horas | Dados piloto |
| 2.4 | Execução completa com genoma piloto 3 | Operador | 4 horas | Dados piloto |
| 2.5 | Análise dos resultados piloto | Operador | 4 horas | Relatório piloto |
| 2.6 | Ajustes no protocolo | Operador | 4 horas | Protocolo revisado |
| 2.7 | Aprovação para execução principal | Orientador | 1 hora | Go/No-Go |

**FASE 3: EXECUÇÃO PRINCIPAL (Semanas 4-6)**

| Passo | Ação | Responsável | Duração | Entregável |
|-------|------|-------------|---------|------------|
| 3.1 | Execução do Checklist Pré-Sessão | Operador | 10 min | Checklist preenchido |
| 3.2 | Limpeza de cache e reinício do sistema | Operador | 5 min | Sistema limpo |
| 3.3 | Iniciar scripts de monitoramento | Operador | 2 min | Monitores ativos |
| 3.4 | Iniciar cronômetro | Operador | 1 min | Timer iniciado |
| 3.5 | Submeter genoma à ferramenta | Operador | 5-10 min | Submissão confirmada |
| 3.6 | Aguardar processamento | Operador | 5-120 min | Processamento concluído |
| 3.7 | Parar cronômetro | Operador | 1 min | Tempo registrado |
| 3.8 | Download/coleta dos resultados | Operador | 5 min | Arquivos de saída |
| 3.9 | Execução do Checklist Pós-Sessão | Operador | 10 min | Checklist preenchido |
| 3.10 | Registro na planilha de dados | Operador | 5 min | Dados registrados |
| 3.11 | Backup no repositório Git | Operador | 2 min | Commit realizado |
| 3.12 | Intervalo entre sessões | Operador | 30 min | Descanso |

**FASE 4: PÓS-PROCESSAMENTO (Semana 7)**

| Passo | Ação | Responsável | Duração | Entregável |
|-------|------|-------------|---------|------------|
| 4.1 | Execução do BUSCO em todas as anotações | Operador | 8 horas | Scores BUSCO |
| 4.2 | Cálculo de concordância entre ferramentas | Operador | 4 horas | Índices Kappa |
| 4.3 | Consolidação de todos os dados | Operador | 4 horas | Dataset unificado |
| 4.4 | Verificação de dados faltantes | Operador | 2 horas | Relatório de qualidade |
| 4.5 | Tratamento de outliers | Operador | 2 horas | Dataset limpo |

**FASE 5: ANÁLISE (Semanas 8-9)**

| Passo | Ação | Responsável | Duração | Entregável |
|-------|------|-------------|---------|------------|
| 5.1 | Análise estatística descritiva | Operador | 8 horas | Tabelas e gráficos |
| 5.2 | Testes de hipóteses (ANOVA) | Operador | 8 horas | Resultados estatísticos |
| 5.3 | Interpretação dos resultados | Operador/Orientador | 8 horas | Discussão |
| 5.4 | Redação do relatório final | Operador | 16 horas | Documento final |
| 5.5 | Revisão pelo orientador | Orientador | 4 horas | Feedback |
| 5.6 | Publicação no repositório | Operador | 2 horas | Repositório público |

---

### 11.4 Plano de piloto (se haverá piloto, escopo e critérios de ajuste)

**Haverá estudo piloto:** Sim

**Escopo do piloto:**
- 3 genomas de teste (1 pequeno, 1 médio, 1 grande)
- Genomas diferentes dos 18 da amostra principal
- Execução completa do protocolo em todas as 3 ferramentas
- Duração estimada: 3 dias

**Objetivos do piloto:**
1. Validar o funcionamento dos scripts de automação
2. Calibrar tempos estimados para cada etapa
3. Identificar problemas técnicos não previstos
4. Treinar o operador no protocolo completo
5. Verificar adequação dos instrumentos de coleta

**Genomas do piloto:**

| ID | Organismo | Tamanho | Categoria |
|----|-----------|---------|-----------|
| P1 | *Lactobacillus acidophilus* | 1,99 Mb | Pequeno |
| P2 | *Vibrio cholerae* | 4,03 Mb | Médio |
| P3 | *Myxococcus xanthus* | 9,14 Mb | Grande |

**Critérios de ajuste permitidos após o piloto:**

| Aspecto | Ajuste Permitido | Ajuste Não Permitido |
|---------|------------------|----------------------|
| **Tempo estimado** | Recalcular baseado no piloto | - |
| **Scripts** | Corrigir bugs, otimizar | Mudar métricas coletadas |
| **Ordem de execução** | Ajustar intervalos | Mudar randomização |
| **Instrumentos** | Adicionar campos na planilha | Remover variáveis |
| **Protocolo** | Clarificar instruções | Mudar ferramentas testadas |
| **Hardware** | Otimizar configurações | Trocar equipamento |

**Critérios de aprovação do piloto:**
- ✓ Todas as 9 execuções (3 genomas × 3 ferramentas) completadas com sucesso
- ✓ Dados coletados para todas as variáveis dependentes
- ✓ Scripts funcionando sem erros críticos
- ✓ Tempo total dentro de 150% do estimado
- ✓ Aprovação formal do orientador

---

## 12. Plano de análise de dados (pré-execução)

### 12.1 Estratégia geral de análise (como responderá às questões)

#### Mapeamento Questões → Análises

| Questão | Dados Necessários | Análise | Visualização |
|---------|-------------------|---------|--------------|
| **Q1.1** Diferença no tempo entre web/desktop | M1 (tempo total) | ANOVA + teste-t | Box plot |
| **Q1.2** Impacto do tamanho no tempo | M1, M3 | ANOVA 2-way | Scatter plot |
| **Q1.3** Consumo de recursos | M4, M5 | Estatísticas descritivas | Bar chart |
| **Q2.1** Elementos genômicos identificados | M6, M7 | ANOVA | Bar chart agrupado |
| **Q2.2** Concordância entre ferramentas | M8, M9 | Fleiss' Kappa | Heatmap |
| **Q2.3** Completude da anotação | M10, M11 | ANOVA | Box plot |
| **Q3.1** Esforço de instalação | M12, M13 | Descritiva | Tabela comparativa |
| **Q3.2** Facilidade de integração | M14, M15 | Descritiva | Radar chart |
| **Q4.1** Taxa de sucesso | M18, M19 | Teste qui-quadrado | Bar chart |
| **Q4.2** Impacto da conectividade | M20, M21 | Teste-t | Line chart |

**Fluxo de análise:**

Dados Brutos → Limpeza → Análise Descritiva → Testes de Pressupostos → Análise Inferencial → Interpretação → Conclusões

---

### 12.2 Métodos estatísticos planejados

#### Testes Estatísticos por Hipótese

| Hipótese | Teste Principal | Teste Alternativo (se pressupostos violados) | Software |
|----------|-----------------|---------------------------------------------|----------|
| **H1 (Performance)** | ANOVA medidas repetidas | Friedman | R/Python |
| **H2 (Qualidade)** | ANOVA one-way | Kruskal-Wallis | R/Python |
| **H3 (Interação)** | ANOVA two-way | Aligned Rank Transform | R |
| **H4 (Confiabilidade)** | Teste qui-quadrado | Teste exato de Fisher | R/Python |

#### Verificação de Pressupostos

| Pressuposto | Teste | Critério | Ação se Violado |
|-------------|-------|----------|-----------------|
| **Normalidade** | Shapiro-Wilk | p > 0,05 | Usar teste não-paramétrico |
| **Homogeneidade de variâncias** | Levene | p > 0,05 | Usar Welch ANOVA |
| **Esfericidade** | Mauchly | p > 0,05 | Usar correção Greenhouse-Geisser |
| **Independência** | Design experimental | Garantido pelo design | - |

#### Testes Post-Hoc

| Situação | Teste Post-Hoc | Correção |
|----------|----------------|----------|
| ANOVA significativa (3 grupos) | Tukey HSD | Incluída no teste |
| Múltiplas comparações | Bonferroni | α/k comparações |
| Não-paramétrico | Dunn | Bonferroni |

#### Tamanho do Efeito

| Teste | Medida de Efeito | Interpretação |
|-------|------------------|---------------|
| ANOVA | η² (eta quadrado) | 0,01=pequeno, 0,06=médio, 0,14=grande |
| Teste-t | d de Cohen | 0,2=pequeno, 0,5=médio, 0,8=grande |
| Qui-quadrado | V de Cramér | 0,1=pequeno, 0,3=médio, 0,5=grande |

---

### 12.3 Tratamento de dados faltantes e outliers

#### Regras para Dados Faltantes

| Situação | Regra | Ação |
|----------|-------|------|
| Falha total de uma ferramenta para um genoma | Missing at Random | Excluir genoma da análise pareada |
| Métrica específica não coletada | Missing Completely at Random | Imputação pela média do grupo |
| Mais de 20% de dados faltantes em uma variável | Sistemático | Reportar separadamente |
| Timeout em ferramenta web | Censurado | Registrar como tempo máximo + flag |

#### Regras para Outliers

| Método de Detecção | Critério | Ação |
|--------------------|----------|------|
| Z-score | \|z\| > 3 | Investigar causa |
| IQR (Interquartile Range) | < Q1-1,5×IQR ou > Q3+1,5×IQR | Marcar para análise |
| Inspeção visual | Box plot | Documentar |

**Procedimento para outliers:**

1. Identificar outlier
2. Verificar se é erro de registro → Corrigir
3. Verificar se é erro de execução → Repetir se possível
4. Se valor legítimo → Manter e reportar
5. Realizar análise com e sem outliers
6. Reportar ambos os resultados se diferentes

**Decisões pré-registradas:**
- Outliers identificados NÃO serão automaticamente removidos
- Análise de sensibilidade será realizada (com/sem outliers)
- Todas as exclusões serão justificadas e documentadas
- Dados brutos completos serão disponibilizados

---

### 12.4 Plano de análise para dados qualitativos (se houver)

#### Dados Qualitativos Coletados

| Dado | Fonte | Tipo |
|------|-------|------|
| Observações durante execução | Checklist pós-sessão | Texto livre |
| Mensagens de erro | Logs das ferramentas | Texto estruturado |
| Dificuldades encontradas | Diário do operador | Texto livre |
| Características das anotações | Arquivos de saída | Categórico |

#### Método de Análise: Análise de Conteúdo

**Procedimento:**

1. **Coleta:** Compilar todas as observações textuais
2. **Leitura inicial:** Familiarização com o material
3. **Codificação aberta:** Identificar temas emergentes
4. **Categorização:** Agrupar códigos em categorias
5. **Quantificação:** Contar frequência de categorias
6. **Interpretação:** Relacionar com dados quantitativos

**Categorias pré-definidas:**

| Categoria | Códigos Esperados |
|-----------|-------------------|
| **Problemas técnicos** | Erro de conexão, timeout, falha de instalação |
| **Usabilidade** | Interface confusa, documentação insuficiente |
| **Performance** | Lentidão, travamento, uso excessivo de recursos |
| **Qualidade** | Anotação incompleta, inconsistência |

**Apresentação dos resultados:**
- Tabela de frequência de categorias
- Exemplos representativos de cada categoria
- Triangulação com dados quantitativos

---

## Resumo dos Instrumentos e Variáveis por Fase

| Fase | Instrumentos | Variáveis Coletadas | Métricas |
|------|--------------|---------------------|----------|
| **Preparação** | I10 (Git) | Metadados | - |
| **Piloto** | I1-I10 | Todas (teste) | M1-M23 (validação) |
| **Execução** | I1, I2, I3, I4, I5, I7 | VI, VD1-VD8 | M1-M7, M18-M19 |
| **Pós-processamento** | I6, I8 | VD derivadas | M8-M11 |
| **Análise** | R/Python | Todas | Todas |
