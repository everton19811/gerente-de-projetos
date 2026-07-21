# 🔌 Plano de Integrações (23 Sistemas)

## Classificação

| Categoria | Sistemas | Padrão de Integração |
|-----------|----------|---------------------|
| **Alta plataforma — síncrona** | SAP ECC, Salesforce CRM, TOTVS Protheus, DocuSign | REST/OData via MuleSoft, autenticação OAuth2 |
| **Alta plataforma — assíncrona** | Manhattan TMS, WMS Infor, Data Lake, Power BI | Eventos Kafka/JMS + CDC |
| **Bureaus externos** | Serasa, SPC, SEFAZ, SPED, e-Social | SOAP/REST + certificado digital A1 |
| **Baixa plataforma / legado** | Portal PHP, Cobol Cobrança, VB6 Comissões, Access Regional, GED, Planilhas críticas | Adapter dedicado + FTP/SFTP + polling |
| **Financeiro** | Gateway Bancário, Boletos Registrados | API REST + assinatura HMAC |

## Padrões Arquiteturais
- **API-led connectivity** (System / Process / Experience APIs)
- **Circuit breaker** em toda chamada síncrona
- **Retry exponencial** + Dead Letter Queue em fluxos assíncronos
- **Idempotência** obrigatória via header `X-Idempotency-Key`
- **Observabilidade**: correlation ID ponta a ponta

## Detalhamento dos 23 Sistemas

| # | Sistema | Tipo | Camada | Protocolo | Criticidade |
|---|---------|------|--------|-----------|------------|
| 1 | SAP ECC | ERP | Alta | REST/OData | Crítica |
| 2 | Salesforce CRM | CRM | Alta | REST | Crítica |
| 3 | TOTVS Protheus | ERP fiscal | Alta | SOAP | Crítica |
| 4 | Manhattan TMS | Logística | Alta | Kafka | Alta |
| 5 | WMS Infor | Armazém | Alta | Kafka | Alta |
| 6 | DocuSign | Assinatura | SaaS | REST | Crítica |
| 7 | MuleSoft ESB | Orquestração | Middleware | — | Crítica |
| 8 | Serasa Experian | Bureau crédito | Externo | REST | Alta |
| 9 | SPC Brasil | Bureau crédito | Externo | REST | Média |
| 10 | SEFAZ | Fiscal | Governo | SOAP | Crítica |
| 11 | SPED | Fiscal | Governo | SOAP | Crítica |
| 12 | e-Social | RH/fiscal | Governo | SOAP | Média |
| 13 | Gateway Bancário | Financeiro | Externo | REST HMAC | Crítica |
| 14 | Boletos Registrados | Financeiro | Externo | REST | Alta |
| 15 | Power BI | Analytics | Alta | Dataset API | Média |
| 16 | Data Lake Azure | Analytics | Alta | CDC/ADF | Alta |
| 17 | Portal Parceiros (PHP) | Legado | Baixa | REST custom | Alta |
| 18 | Cobol Cobrança | Legado | Baixa | Adapter + arquivo | Crítica |
| 19 | VB6 Comissões | Legado | Baixa | ODBC + polling | Média |
| 20 | Access Regional | Legado | Baixa | SFTP + CSV | Baixa |
| 21 | GED (SharePoint) | Documental | Alta | Graph API | Média |
| 22 | Planilhas críticas | Legado | Baixa | Watcher + parser | Média |
| 23 | E-mail corporativo (SMTP) | Notificação | Alta | SMTP/API | Baixa |

Ver `diagramas/arquitetura-integracoes.mmd`.
