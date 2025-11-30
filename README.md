# Proposta-de-Experimento-para-TCC

## 1. Identificação básica


### 1.1 Título do experimento

Análise Comparativa de Performance e Qualidade de Software: Anotadores Genômicos Web-based versus Desktop em Genomas Bacterianos

---

### 1.2 ID / código

EXP-TCC-ANNOT-2025-003

---

### 1.3 Versão do documento e histórico de revisão

- **v1.0** (21/11/2025): Criação inicial do documento com identificação básica e contexto
- **v2.0** (22/11/2025): Definiçao de Escopo, Objetivo
- **v2.5** (23/11/2025): Definiçao de Stakeholders/Impacto, Riscos de alto nível, premissas e critérios de sucesso
- **v3.0** (28/11/2025): Modelo conceitual e hipóteses; Variáveis, fatores, tratamentos e objetos de estudo; Desenho experimental

---
    
### 1.4 Datas (criação, última atualização)

- **Data de criação:** 21/11/2025
    
- **Última atualização:** 30/11/2025
    
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
