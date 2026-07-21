# 🏛️ Arquitetura de Alto Nível

## Camadas

1. **Experiência** — Portal ContractFlow (React) + App comercial + Portal cliente B2B
2. **Processos** — Motor de workflow (Camunda) + Regras de negócio + Contrato digital
3. **Orquestração** — MuleSoft ESB (Process APIs)
4. **Sistemas** — Conectores para 23 sistemas (System APIs)
5. **Dados** — Data Lake Azure + Power BI
6. **Observabilidade** — Azure Monitor + App Insights + Grafana
7. **Segurança** — Azure AD + IAM + Vault + Certificado A1

## Padrões Adotados
- API-led connectivity
- Event-driven para eventos de negócio (contrato assinado, fatura emitida, baixa recebida)
- CQRS no motor de reconciliação
- Saga pattern para transações distribuídas Order-to-Cash

## Decisões Arquiteturais (ADRs resumo)

| ADR | Decisão | Justificativa |
|-----|---------|---------------|
| ADR-01 | MuleSoft como ESB único | Licença corporativa + skill interno |
| ADR-02 | Camunda para workflow | Open source + BPMN 2.0 |
| ADR-03 | DocuSign para assinatura | Compliance + validade jurídica |
| ADR-04 | Azure como cloud primária | Alinhamento IT strategy |
| ADR-05 | Kafka para eventos de negócio | Throughput + retenção |
| ADR-06 | Adapter pattern p/ legados | Isolamento e substituição futura |

Ver `diagramas/arquitetura-camadas.mmd` e `diagramas/fluxo-order-to-cash.mmd`.
