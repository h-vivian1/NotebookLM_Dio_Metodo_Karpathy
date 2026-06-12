---
title: Padrões Arquiteturais e Estilo de Código
type: l1_cache
tags: [architecture, guidelines, coding_standards]
confidence: high
updated: 2026-06-12
---

# Diretrizes de Implementação

1. **Design Orientado a Domínio (DDD)**: O domínio dita rigorosamente as fronteiras dos contextos (Bounded Contexts).
2. **Imutabilidade**: Dados fluem de maneira unidirecional. Mutações de estado devem ser isoladas e rastreáveis.
3. **Observabilidade (Telemetry)**: Logs estruturados nativos em formato JSON para traceamento completo de invocações de LLM e latência de ferramentas. Isto apoia a funcionalidade do [[log]] de auditoria.
4. **Engenharia de Resiliência**: Fallbacks graciosos (graceful degradation) para lógicas heurísticas em caso de falha sistêmica ou timeout na inferência neural.

*Nota: Todas as operações do agente devem estar em conformidade com as regras deste artefato, bem como alinhadas às expectativas técnicas estabelecidas no [[perfil_usuario]], garantindo que a base do [[metodo_llm_wiki]] seja sólida.*
