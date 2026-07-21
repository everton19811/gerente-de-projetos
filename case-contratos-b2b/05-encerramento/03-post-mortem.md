# 🔬 Post-Mortem Técnico

## Contexto
Go-live 15/11/2025, hypercare 45 dias, zero incidentes P1, três P2 resolvidos em < 4h.

## Timeline de Incidentes
| Data | Severidade | Descrição | Resolução |
|------|-----------|-----------|-----------|
| 18/11 | P2 | Latência SAP > 2s em pico matinal | Ajuste de cache + índice |
| 27/11 | P2 | Divergência em 3 notas SEFAZ | Correção regra CFOP |
| 09/12 | P2 | Fila DocuSign travou | Retry policy revisada |

## Causa Raiz por Categoria
- 40% — configuração de retry/timeout mal calibrada
- 35% — regras fiscais específicas (CFOP/CST) não cobertas em UAT
- 25% — comportamento de pico não simulado

## Ações Estruturais
1. Ampliar cenários UAT com dados fiscais reais anonimizados
2. Testes de carga trimestrais permanentes
3. Runbook de retry/timeout como parte do checklist de deploy
