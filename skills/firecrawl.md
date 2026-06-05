# Skill: Firecrawl

## Objetivo

Fornecer capacidades de busca web para os agentes do Rota Dev IA.

Esta skill permite que os agentes encontrem vagas de emprego, cursos e informações relevantes utilizando o Firecrawl CLI.

## Ferramenta

* terminal
* Firecrawl CLI

## Comandos Disponíveis

### Buscar vagas

```bash
firecrawl search "[consulta]" --json
```

Exemplos:

```bash
firecrawl search "estágio java remoto" --json
```

```bash
firecrawl search "vaga desenvolvedor java junior são paulo" --json
```

### Obter conteúdo de uma página

```bash
firecrawl scrape <url> --format markdown
```

Exemplo:

```bash
firecrawl scrape https://empresa.com/vaga/123 --format markdown
```

## Saída Esperada

Os resultados devem conter:

* URL
* Título
* Descrição
* Conteúdo extraído (quando aplicável)

## Tratamento de Erros

* Não inventar resultados.
* Se a busca retornar vazia, informar que nenhuma vaga foi encontrada.
* Se o scrape falhar, registrar o erro.
* Nunca gerar dados fictícios.

## Agentes que utilizam esta Skill

### Hunter

Utiliza esta skill para buscar vagas compatíveis com o perfil do usuário.

### Mentor

Pode utilizar esta skill para buscar cursos e materiais de estudo relacionados às habilidades prioritárias.

## Integração

Os resultados obtidos devem ser armazenados em arquivos da pasta:

```text
data/
```

Principalmente:

```text
data/job-results.md
```
