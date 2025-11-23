# Proposta-de-Experimento-para-TCC

## 1. Identificação básica


### 1.1 Título do experimento

Análise Comparativa de Performance e Acurácia: Anotadores Genômicos Web-based versus Desktop em Genomas Bacterianos

---

### 1.2 ID / código

EXP-TCC-ANNOT-2025-002

---

### 1.3 Versão do documento e histórico de revisão

- **v1.0** (21/11/2025): Criação inicial do documento com identificação básica e contexto
- **v2.0** (22/11/2025): Definiçao de Escopo, Objetivo
- **v2.5** (23/11/2025): Definiçao de Stakeholders/Impacto, Riscos de alto nível, premissas e critérios de sucesso

---
    
### 1.4 Datas (criação, última atualização)

- **Data de criação:** 21/11/2025
    
- **Última atualização:** 23/11/2025
    
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



