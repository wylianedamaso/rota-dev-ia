# 🚀 Rota Dev IA

**Rota Dev IA** é um ecossistema inteligente baseado em arquitetura multiagente, criado para auxiliar estudantes e profissionais iniciantes da área de tecnologia em sua jornada de entrada no mercado de trabalho.

O projeto utiliza agentes especializados para transformar informações sobre o perfil do usuário em ações práticas, como identificação de oportunidades, análise de competências, elaboração de planos de estudo e preparação para entrevistas.

---

# 📝 Sobre o Projeto

O projeto foi inspirado nos conceitos de agentes autônomos, engenharia de prompts e orquestração de IA apresentados na **Imersão IA da Alura**, sendo desenvolvido como uma aplicação autoral voltada para empregabilidade na área de tecnologia.

O objetivo é reduzir a distância entre:

* O perfil atual do candidato;
* As exigências do mercado;
* O plano necessário para conquistar a vaga desejada.

Através da colaboração entre múltiplos agentes especializados, o sistema é capaz de orientar o usuário durante toda a sua preparação profissional.

---

# 🎯 Objetivos

* Auxiliar estudantes e iniciantes na área tech.
* Identificar oportunidades compatíveis com o perfil do usuário.
* Detectar lacunas de conhecimento (Skill Gaps).
* Gerar planos de estudo personalizados.
* Simular entrevistas técnicas e comportamentais.
* Aumentar a empregabilidade através de orientação baseada em IA.

---

# 🏗️ Arquitetura Multiagente

O sistema opera utilizando agentes especializados, cada um responsável por uma etapa específica da jornada do usuário.

```text
Usuário
   │
   ▼
🎩 Maestro
   │
   ▼
🏹 Hunter
   │
   ▼
🔍 Analyzer
   │
   ▼
📚 Mentor
   │
   ▼
🎙️ Coach
```

---

# 🤖 Agentes do Sistema

## 🎩 Maestro (Orquestrador)

Responsável por:

* Receber a solicitação do usuário.
* Coletar informações do perfil.
* Gerar o contexto inicial.
* Direcionar o fluxo para o agente adequado.
* Gerenciar a comunicação entre os agentes.

---

## 🏹 Hunter (Busca de Vagas)

Responsável por:

* Identificar oportunidades compatíveis com o perfil.
* Filtrar vagas por tecnologia, senioridade e modalidade.
* Gerar relatórios de oportunidades.

> A integração com Firecrawl para coleta de vagas em tempo real está prevista para versões futuras.

---

## 🔍 Analyzer (Análise de Habilidades)

Responsável por:

* Comparar o perfil do usuário com as exigências do mercado.
* Identificar lacunas técnicas.
* Priorizar habilidades mais relevantes para empregabilidade.
* Gerar relatórios de análise profissional.

---

## 📚 Mentor (Plano de Estudos)

Responsável por:

* Criar trilhas de aprendizado personalizadas.
* Organizar tópicos em ordem estratégica.
* Sugerir projetos para portfólio.
* Definir metas de curto, médio e longo prazo.

---

## 🎙️ Coach (Simulação de Entrevistas)

Responsável por:

* Simular entrevistas técnicas.
* Simular entrevistas comportamentais.
* Avaliar respostas.
* Fornecer feedback estruturado.
* Sugerir melhorias para futuras entrevistas.

---

# 📂 Estrutura do Projeto

```text
rota-dev-ia/
│
├── README.md
│
├── personas/
│   ├── maestro.md
│   ├── hunter.md
│   ├── analyzer.md
│   ├── mentor.md
│   └── coach.md
│
├── skills/
│   ├── dispatch.md
│   ├── job-search.md
│   ├── profile-analysis.md
│   ├── study-plan.md
│   └── interview-simulation.md
│
└── data/
    ├── user-profile.md
    ├── job-results.md
    ├── skill-gaps.md
    ├── analysis-report.md
    ├── study-plan.md
    └── interview-report.md
```

---

# 🔄 Fluxo de Funcionamento

## 1. Coleta de Perfil

O Maestro coleta:

* Nome
* Localização
* Tipo de vaga desejada
* Modalidade
* Stack tecnológica
* Soft Skills
* GitHub

Resultado:

```text
data/user-profile.md
```

---

## 2. Busca de Oportunidades

O Hunter analisa o perfil e gera:

```text
data/job-results.md
```

---

## 3. Análise de Competências

O Analyzer compara:

* Perfil do usuário
* Requisitos das vagas

Resultado:

```text
data/analysis-report.md
```

---

## 4. Plano de Desenvolvimento

O Mentor utiliza o relatório para gerar:

```text
data/study-plan.md
```

---

## 5. Preparação para Entrevistas

O Coach utiliza todos os artefatos anteriores para gerar:

```text
data/interview-report.md
```

---

# 🛠️ Tecnologias Utilizadas

* Zed
* OpenRouter
* Modelos LLM (Open Source)
* Markdown
* Git
* GitHub

Tecnologias planejadas:

* Firecrawl
* APIs de vagas
* Interface Web
* Banco de Dados

---

# 📌 Status do Projeto

🚧 MVP Conceitual Funcional

## ✅ Concluído

* Arquitetura multiagente definida
* Personas especializadas criadas
* Skills documentadas
* Fluxo de orquestração implementado
* Estrutura de persistência em Markdown
* Simulação do fluxo completo entre agentes
* Documentação inicial

## 🔄 Em Desenvolvimento

* Refinamento das skills
* Testes de integração
* Melhorias na persistência dos dados

## 🚀 Próximas Versões

### v1.1.0

* Integração com Firecrawl
* Busca de vagas em tempo real

### v1.2.0

* Persistência automatizada
* Histórico de execuções

### v1.3.0

* Interface Web

### v2.0.0

* Memória de longo prazo
* Integração com APIs externas
* Recomendações avançadas de carreira

---

# 🎓 Aprendizados Aplicados

Este projeto aplica conceitos de:

* Arquitetura Multiagente
* Engenharia de Prompts
* Orquestração de IA
* Context Engineering
* Planejamento de Fluxos Inteligentes
* Organização de Sistemas Baseados em LLMs

---

# 👩‍💻 Autora

Wyliane Damaso

Estudante de Análise e Desenvolvimento de Sistemas, com foco em desenvolvimento Back-End.

---

⭐ Projeto desenvolvido para fins de estudo, prática de arquitetura multiagente e aplicação dos conhecimentos adquiridos na Imersão IA da Alura.
