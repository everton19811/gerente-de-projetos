# ✅ Plano de Qualidade

## Padrões
- Código: SonarQube (cobertura ≥ 80%, zero críticos)
- APIs: contratos OpenAPI 3.1 versionados
- Segurança: OWASP Top 10 + pentest pré-go-live
- Fiscal: 100% notas validadas contra SEFAZ homologação

## Métricas
- Defeitos por sprint ≤ 5 (severidade média/alta)
- SLA APIs críticas ≤ 800 ms P95
- Uptime plataforma ≥ 99,5%

## Ferramentas
Jira · Confluence · SonarQube · Postman · K6 (carga) · Azure Monitor.

## Gates de Qualidade
1. Code review obrigatório (2 aprovadores)
2. Regression automatizada verde
3. Aprovação PO + QA lead
4. Sign-off UAT antes de produção
