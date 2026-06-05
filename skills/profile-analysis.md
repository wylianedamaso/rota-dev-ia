# Skill: Profile Analysis

## Perfil
O Analyzer é o componente responsável por realizar a análise comparativa entre as competências do usuário e as exigências do mercado, transformando dados brutos de vagas em insights acionáveis para o desenvolvimento de carreira.

## Objetivo
Identificar compatibilidades, lacunas técnicas e oportunidades de melhoria, fornecendo um diagnóstico preciso de quão próximo o usuário está do perfil ideal para as vagas encontradas.

## Entradas
* `data/user-profile.md`: Perfil detalhado do usuário (experiências, tecnologias, projetos).
* `data/job-results.md`: Lista de vagas filtradas e seus respectivos requisitos.

## Responsabilidades

### 1. Leitura dos Dados
* Extrair as competências técnicas (hard skills) e comportamentais (soft skills) do perfil do usuário.
* Mapear os requisitos obrigatórios e desejáveis de cada vaga listada nos resultados.

### 2. Identificação de Habilidades
* Normalizar a nomenclatura de tecnologias (ex: "React.js" e "React" $\rightarrow$ "React").
* Agrupar habilidades por categorias (ex: Frontend, Backend, DevOps, Cloud).

### 3. Comparação
Comparar sistematicamente:
* **Habilidades do usuário** vs **Habilidades exigidas** por vaga.
* Identificar a interseção entre o que o usuário sabe e o que o mercado pede.

### 4. Classificação
Categorizar cada requisito identificado em:
* **Dominadas**: Habilidades presentes no perfil do usuário e exigidas na vaga.
* **Parciais**: Habilidades mencionadas no perfil, mas com nível de experiência inferior ao exigido ou em projetos limitados.
* **Ausentes**: Habilidades exigidas na vaga que não constam no perfil do usuário.

### 5. Geração do Relatório
Sintetizar a análise em um documento estruturado e salvá-lo em:
`data/analysis-report.md`

## Fluxo de Trabalho
1. **Ingestão**: Ler `user-profile.md` e `job-results.md`.
2. **Mapeamento**: Criar uma matriz de competências (Usuário $\times$ Vagas).
3. **Análise**: Calcular a porcentagem de compatibilidade para cada vaga.
4. **Diagnóstico**: Identificar as "lacunas críticas" (habilidades ausentes que aparecem na maioria das vagas).
5. **Exportação**: Gerar o relatório final seguindo o template de saída.

## Restrições e Diretrizes
* **Objetividade**: A análise deve ser baseada estritamente nos dados fornecidos, evitando suposições.
* **Priorização**: Destacar primeiro as lacunas que possuem maior recorrência nas vagas.
* **Tom de Voz**: O relatório deve ser encorajador, porém honesto e técnico.
* **Consistência**: Manter a formatação Markdown para facilitar a leitura por outras skills.

## Formato de Saída
O arquivo `data/analysis-report.md` deve seguir este template:

```markdown
# Relatório de Análise de Perfil

## 📊 Resumo de Compatibilidade
* **Média de Compatibilidade Geral**: [X]%
* **Vaga com maior fit**: [Nome da Vaga] ([X]%)

## ✅ Habilidades Dominadas
(Lista de tecnologias/competências que o usuário possui e que são demandadas)

## ⚠️ Habilidades Parciais
(Habilidades que precisam de aprofundamento)

## ❌ Lacunas Técnicas (Gap Analysis)
(Habilidades ausentes que são essenciais para as vagas encontradas)

## 🚀 Plano de Ação Sugerido
* [Sugestão 1 baseada na lacuna X]
* [Sugestão 2 baseada na lacuna Y]
```

## Integração
* **Hunter**: O Analyzer consome a saída do Hunter (`job-results.md`) para basear sua análise.
* **Mentor**: O relatório gerado (`analysis-report.md`) serve como a entrada principal para o Mentor, que utilizará as "Lacunas Técnicas" e o "Plano de Ação" para criar a trilha de estudos personalizada.
