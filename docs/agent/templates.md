# Templates de Prompt — Modo Agent

Templates rápidos para usar com [`prompts/prompt-agent.md`](../../prompts/prompt-agent.md).
Copie, preencha os `< >` e cole na conversa.

---

## 1) Nova feature / endpoint

```
Projeto: <nome>
Tarefa: implementar <descrição curta da feature>

Contexto:
- <regra de negócio relevante 1>
- <regra de negócio relevante 2>

Critérios de aceite:
- <critério 1>
- <critério 2>

Fora de escopo: <opcional — o que NÃO fazer agora>
```

---

## 2) Bugfix

```
Projeto: <nome>
Tarefa: corrigir bug — <descrição do comportamento errado>

Comportamento esperado: <o que deveria acontecer>
Comportamento atual: <o que está acontecendo>

Código relevante (se tiver):
<cole o trecho ou arquivo>

Stack trace / erro (se tiver):
<cole aqui>
```

---

## 3) Refactor

```
Projeto: <nome>
Tarefa: refatorar <arquivo ou módulo>

Motivo: <ex.: "função muito grande", "duplicação", "preparar pra feature Z">

Restrições:
- Não mudar comportamento externo (contrato de API/assinatura pública)
- <outra restrição, se houver>

Código atual:
<cole aqui>
```

---

## 4) Code review

```
Projeto: <nome>
Tarefa: revisar este código antes de eu abrir PR

Código:
<cole aqui ou descreva os arquivos>

Foco da revisão (marque o que importa):
- [ ] Edge cases
- [ ] Segurança
- [ ] Performance
- [ ] Aderência às convenções do projeto
- [ ] Cobertura de teste
```

---

## 5) Migration / mudança de schema

```
Projeto: <nome>
Tarefa: criar migration para <descrição da mudança no schema>

ORM/ferramenta de migration: <preencher — se não disser, Cortana assume e declara>
Tabelas/entidades afetadas: <nomes>
Precisa de dado de backfill? <sim/não — se sim, descreva a regra>
Reversível? <sim/não>
```

---

## 6) "Continua de onde parou" (retomar conversa)

```
Projeto: <nome>
Continuando a tarefa: <título/resumo da conversa anterior>

Onde paramos: <último checklist ou pendência listada>
Próximo passo: <o que você quer agora>
```

---

## Dica geral

Quanto mais os critérios de aceite forem explícitos, menos a Cortana precisa
interromper com perguntas — ela só pergunta quando a decisão tem alto impacto
no design (idempotência, auth, contrato público) ou quando o projeto/contexto
não está claro (ver `workflow.md`, etapa 0).