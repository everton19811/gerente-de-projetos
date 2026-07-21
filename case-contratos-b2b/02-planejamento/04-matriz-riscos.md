# ⚠️ Matriz de Riscos

Escala: P (Probabilidade) 1-5 · I (Impacto) 1-5 · Score = P × I

| # | Risco | Categoria | P | I | Score | Resposta | Owner |
|---|-------|-----------|---|---|-------|----------|-------|
| R01 | API SAP indisponível/lenta em picos | Técnico | 4 | 5 | 20 | Mitigar: circuit breaker + cache + janela batch | Arquiteto |
| R02 | Legado Cobol (cobrança) sem doc de interface | Legado | 5 | 4 | 20 | Mitigar: engenharia reversa + adapter dedicado | AF Sr |
| R03 | Divergência fiscal na integração SEFAZ | Compliance | 3 | 5 | 15 | Mitigar: sandbox + duplo controle 60 dias | Fiscal |
| R04 | Rejeição usuários comerciais ao novo fluxo | Pessoas | 4 | 4 | 16 | Mitigar: change mgmt + champions + treinamento | GP |
| R05 | Licenças MuleSoft atrasarem | Fornecedor | 3 | 5 | 15 | Transferir: contrato com SLA + penalidade | Compras |
| R06 | Vazamento de dados (LGPD) | Compliance | 2 | 5 | 10 | Mitigar: DPIA + criptografia + IAM | DPO |
| R07 | Retrabalho por escopo mal definido em legados | Escopo | 4 | 3 | 12 | Mitigar: spike de 2 sem por legado | GP |
| R08 | Falha em conciliação bancária no go-live | Financeiro | 3 | 5 | 15 | Mitigar: piloto controlado + rollback | CFO |
| R09 | Perda de talento-chave da squad | RH | 2 | 4 | 8 | Mitigar: pair programming + doc contínua | GP |
| R10 | Concorrência das áreas por prioridade TI | Organizacional | 3 | 4 | 12 | Escalar: comitê exec quinzenal | Sponsor |

Ver `diagramas/riscos-heatmap.mmd`.
