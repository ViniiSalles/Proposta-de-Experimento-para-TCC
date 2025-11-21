# Proposta-de-Experimento-para-TCC

## 1. Identificação básica


### 1.1 Título do experimento

Análise Comparativa de Performance e Acurácia: Anotadores Genômicos Web-based versus Desktop em Genomas Bacterianos

---

### 1.2 ID / código

EXP-TCC-ANNOT-2024-001

---

### 1.3 Versão do documento e histórico de revisão

- **v1.0** (21/11/2024): Criação inicial do documento com identificação básica e contexto

---
    
### 1.4 Datas (criação, última atualização)

- **Data de criação:** 21/11/2024
    
- **Última atualização:** 21/11/2024
    
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


