---
title: System Schema
type: rules
confidence: high
updated: 2026-06-12
---

# Regras de Manutenção da Wiki

- **Formatação**: Todo arquivo `.md` deve conter frontmatter YAML rigoroso com as chaves: `title`, `type`, `tags`, `confidence`, e `updated`.
- **Linguagem**: Pragmática, adotando jargão técnico puro de engenharia de software e arquitetura.
- **Writeback Mandatório**: Sempre que um novo conceito for inferido ou um erro for solucionado no ciclo atual, atualize ou crie os artefatos correspondentes no Cache L2 (`wiki/`).
- **Links**: Utilize links relativos (ex: `[[nome_do_arquivo]]`) para interconectar entidades no diretório `wiki/concepts/`.
- **Preservação de Estado**: Arquivos no diretório `raw/` são imutáveis e não devem ser alterados sob nenhuma hipótese.
