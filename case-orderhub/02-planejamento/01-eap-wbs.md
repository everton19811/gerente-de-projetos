# EAP / WBS — OrderHub

```mermaid
mindmap
  root((OrderHub))
    1. Gestão do Projeto
      1.1 Kickoff
      1.2 Planejamento
      1.3 Governança
      1.4 Encerramento
    2. Discovery
      2.1 Entrevistas
      2.2 Mapeamento AS-IS
      2.3 Desenho TO-BE
      2.4 Backlog inicial
    3. Portal Web
      3.1 UX/UI
      3.2 Frontend
      3.3 Backend API
      3.4 Autenticação SSO
    4. Integração SAP
      4.1 Análise APIs S/4HANA
      4.2 Middleware
      4.3 Sync catálogo
      4.4 Sync estoque
      4.5 Envio pedido
    5. Mobile
      5.1 App iOS
      5.2 App Android
    6. Qualidade
      6.1 Testes automatizados
      6.2 UAT
      6.3 Performance
      6.4 Segurança / LGPD
    7. Deploy
      7.1 Infra cloud
      7.2 CI/CD
      7.3 Monitoramento
      7.4 Rollout piloto
      7.5 Go-live
    8. Change Management
      8.1 Treinamento interno
      8.2 Onboarding clientes
      8.3 Material apoio
```

## Dicionário da EAP (extrato)
| ID | Pacote | Entrega | Critério aceite | Responsável |
|----|--------|---------|-----------------|-------------|
| 3.3 | Backend API | 42 endpoints REST + OpenAPI | Cobertura testes ≥80%, latência p95 <400ms | Tech Lead |
| 4.3 | Sync Catálogo | Job hora-hora + delta | 100% SKUs sincronizados, <5min delay | Eng. Integração |
| 6.4 | Segurança/LGPD | Relatório pentest + DPIA | Zero críticas, DPIA assinada | DPO + AppSec |
