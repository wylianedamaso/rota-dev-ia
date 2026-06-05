# Skill: Job Search

## Perfil
Esta skill é a capacidade operacional do agente **Hunter**, especializada na prospecção ativa de oportunidades de emprego. Ela atua como a ponte entre as aspirações do usuário (definidas no perfil) e o mercado de trabalho real, utilizando ferramentas de extração de dados para encontrar vagas que maximizem a compatibilidade técnica e cultural.

## Objetivo
Localizar, filtrar e catalogar vagas de emprego reais que estejam alinhadas ao perfil profissional do usuário, transformando dados brutos da web em uma lista curada de oportunidades acionáveis.

## Entradas
A skill deve obrigatoriamente ler e processar:
* `data/user-profile.md`: Para extrair a base de conhecimento sobre as competências, experiências e preferências do usuário.

## Responsabilidades

### 1. Leitura do Perfil
Analisar o arquivo `data/user-profile.md` para compreender a identidade profissional do usuário, identificando pontos fortes, projetos relevantes e a proposta de valor do candidato.

### 2. Extração de Critérios
A partir da leitura do perfil, a skill deve extrair os seguintes parâmetros de busca:
* **Cargo desejado:** Títulos de vagas compatíveis (ex: "Frontend Developer", "Software Engineer").
* **Tecnologias:** Stack tecnológica obrigatória e desejável (ex: "React", "TypeScript", "Node.js").
* **Senioridade:** Nível de experiência esperado (ex: "Júnior", "Pleno", "Sênior").
* **Localização:** Cidades ou países de interesse.
* **Modalidade:** Preferências de trabalho (Remoto, Híbrido ou Presencial).

### 3. Construção da Consulta
Montar queries de busca otimizadas para motores de pesquisa e plataformas de vagas, utilizando operadores booleanos e palavras-chave estratégicas para reduzir o ruído e aumentar a precisão dos resultados.

### 4. Busca de Vagas
Utilizar a ferramenta **Firecrawl** para:
* Realizar buscas web abrangentes.
* Extrair conteúdo de páginas de carreiras e job boards.
* Mapear URLs de vagas que correspondam aos critérios extraídos.

### 5. Filtragem
Aplicar um filtro de relevância rigoroso para descartar:
* Vagas expiradas ou obsoletas.
* Vagas com requisitos incompatíveis com a senioridade do usuário.
* Oportunidades que não atendam aos critérios mínimos de stack tecnológica.

### 6. Persistência
Consolidar as oportunidades encontradas e salvar a lista final no arquivo `data/job-results.md`, garantindo que cada entrada contenha as informações necessárias para a próxima etapa de análise.

## Fluxo de Trabalho
1. **Análise**: Leitura de `data/user-profile.md` $\rightarrow$ Extração de Critérios.
2. **Prospecção**: Construção de Queries $\rightarrow$ Execução via Firecrawl.
3. **Refinamento**: Filtragem de Relevância $\rightarrow$ Seleção de Top Oportunidades.
4. **Entrega**: Formatação de Dados $\rightarrow$ Escrita em `data/job-results.md`.

## Restrições e Diretrizes
* **Veracidade**: Apenas vagas reais e verificáveis devem ser incluídas.
* **Atualidade**: Priorizar vagas publicadas nos últimos 30 dias.
* **Objetividade**: Evitar a inclusão de vagas "genéricas" que não possuam descrição clara de requisitos.
* **Eficiência**: Otimizar o uso do Firecrawl para evitar redundâncias de scraping.

## Formato de Saída
Os resultados em `data/job-results.md` devem seguir o seguinte template:

```markdown
# 🚀 Oportunidades Encontradas

## [Nome da Empresa] - [Título da Vaga]
- **Link:** [URL da Vaga]
- **Modalidade:** [Remoto/Híbrido/Presencial]
- **Localização:** [Cidade/Estado/País]
- **Stack Principal:** [Tecnologia A, Tecnologia B, Tecnologia C]
- **Destaque:** [Breve frase sobre por que esta vaga é compatível com o perfil]
---
```

## Integração
* **Maestro**: O Maestro coordena a execução desta skill após a validação do perfil do usuário.
* **Analyzer**: O arquivo `data/job-results.md` serve como a entrada principal para o agente **Analyzer**, que realizará o "match" detalhado entre a vaga e o currículo, sugerindo ajustes de abordagem.
