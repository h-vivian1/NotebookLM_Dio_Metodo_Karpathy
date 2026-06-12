---
title: Templates de Prompts para Engenharia Agêntica
type: templates
tags: [prompts, templates, ingestao, query, linting, ferramentas]
confidence: high
updated: 2026-06-12
---

# Templates de Prompts Parametrizados para a LLM Wiki

Abaixo estão três templates criados para que outros desenvolvedores possam testar o conceito de 'Agente lendo uma Wiki', conforme os princípios do [[metodo_llm_wiki]] arquitetado por [[andrej_karpathy]].

## Template 1: Ingestão e Compilação de Novo Conhecimento (Ingest)
*Instrui o agente a ler uma fonte primária imutável e distribuir o conhecimento na Wiki de forma interligada.*

> Leia o documento bruto localizado em `[INSERIR CAMINHO DO ARQUIVO RAW]`. Extraia as principais conclusões focando especificamente em `[INSERIR TEMA]`. Após a leitura:
> 1. Crie uma página de resumo estruturada em `wiki/sources/[INSERIR NOME_DO_ARQUIVO].md`.
> 2. Atualize ou crie páginas em `wiki/concepts/` usando `[[wikilinks]]`.
> 3. Atualize o catálogo principal no arquivo [[index]] com as novas entradas.
> 4. Adicione um registro desta operação no arquivo [[log]].

## Template 2: Consulta Roteada pelo Índice com Efeito Composto (Query & Writeback)
*Impede que o LLM dependa apenas de seu treinamento base, usando o [[index]] como um mapa para rotear a busca e aplicando as preferências de output técnico exigidas pelo [[perfil_usuario]].*

> Tenho um problema técnico sobre `[INSERIR PERGUNTA OU DESAFIO]`. Leia primeiro o arquivo [[index]] e identifique quais páginas da base de conhecimento são relevantes. Acesse e leia apenas essas páginas. Sintetize uma resposta utilizando citações cruzadas. Se gerar uma conclusão valiosa, crie automaticamente um novo arquivo em `wiki/comparisons/` para preservarmos esse insight.

## Template 3: Auditoria e Manutenção da Base (Linting)
*Transforma o LLM em um mantenedor ativo da base, capaz de detectar contradições lógicas, validando o cumprimento rigoroso das [[regras_de_codigo]].*

> Atue como auditor da base de conhecimento. Faça uma varredura completa nos arquivos markdown localizados na pasta `wiki/`, focando sobre `[INSERIR TEMA]`. Busque:
> 1. Contradições de informações entre páginas.
> 2. Páginas órfãs.
> 3. Conceitos ou termos importantes que não possuem uma página própria.
> Gere um relatório estruturado salvando como `wiki/logs/lint_report_[DATA].md`.
