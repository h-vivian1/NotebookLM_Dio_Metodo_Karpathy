---
title: Método LLM Wiki e Software 3.0
type: concept
tags: [llm_wiki, software_3_0, agente, memoria, arquitetura]
confidence: high
updated: 2026-06-12
---

# O Método: LLM Wiki e Software 3.0

O método LLM Wiki faz parte de uma mudança de paradigma que [[andrej_karpathy]] chama de **Software 3.0** ou Engenharia Agêntica. Nele, a programação tradicional é substituída pela instrução de Grandes Modelos de Linguagem (LLMs) através de prompts em linguagem natural. Em uma analogia arquitetural, o LLM atua como o "processador" (CPU) e a janela de contexto atua como a "memória RAM" de um novo tipo de sistema operacional (LLM OS).

Nesse paradigma, as IA dominam tarefas verificáveis (embora possam exibir uma "inteligência irregular" ao falhar em lógicas comuns), e surge uma distinção clara entre o simples *vibe coding* e a verdadeira Engenharia Agêntica estruturada (prática adotada de acordo com as [[regras_de_codigo]]).

A aplicação prática desse conceito é o método da LLM Wiki. Em vez de usar a IA apenas para ler documentos na hora de responder a uma pergunta (RAG tradicional, que "esquece" informações), esse método usa a IA para compilar uma base de conhecimento persistente.

## O que esse método é capaz de fazer:
- **Compilação Incremental e Efeito Composto**: O LLM lê fontes brutas apenas uma vez e as compila em páginas conectadas por wikilinks.
- **Manutenção Automatizada ("Bibliotecário Digital")**: O trabalho de organizar notas e atualizar o [[index]] é feito pelo agente de IA.
- **Detecção de Contradições (Linting)**: Verificações periódicas de saúde permitem identificar páginas órfãs, dados desatualizados e contradições, utilizando padrões contidos em [[templates_prompts]].
- **Resolução de Problemas Complexos**: O LLM lê o [[index]] para achar respostas pré-digeridas, reduzindo alucinações.

O sistema divide-se conceitualmente em um Cache L1 (onde reside o [[perfil_usuario]] e diretrizes básicas) e um Cache L2 (onde reside o repositório de conhecimento expandido).
