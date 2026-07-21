# Matriz de Riscos — OrderHub

| ID | Risco | Categoria | Prob | Impacto | Score | Resposta | Owner | Status |
|----|-------|-----------|------|---------|-------|----------|-------|--------|
| R01 | API SAP indisponível | Técnico | 3 | 5 | 15 🔴 | Mitigar: middleware + fila de retry | Tech Lead | Controlado |
| R02 | Baixa adesão clientes | Negócio | 4 | 4 | 16 🔴 | Mitigar: programa piloto + incentivo | GP + Comercial | Encerrado |
| R03 | Rotatividade dev sênior | RH | 3 | 4 | 12 🟠 | Mitigar: retenção + pair programming | GP | Controlado |
| R04 | LGPD — dados sensíveis | Compliance | 2 | 5 | 10 🟠 | Evitar: DPIA + anonimização + DPO | DPO | Encerrado |
| R05 | Estimativa otimista sprint | Cronograma | 4 | 3 | 12 🟠 | Mitigar: buffer 20% + planning poker | GP | Controlado |
| R06 | Falha performance no piloto | Técnico | 2 | 4 | 8 🟡 | Mitigar: load test + APM | Tech Lead | Encerrado |
| R07 | Estouro orçamento SAP | Financeiro | 3 | 3 | 9 🟡 | Mitigar: escopo fechado + T&M cap | GP | Encerrado |

**Escala:** Prob/Impacto 1–5 | 🔴 ≥15 | 🟠 8–14 | 🟡 4–7 | 🟢 <4

## Reserva Utilizada: **R$ 62k / R$ 80k (77%)**
