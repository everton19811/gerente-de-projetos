# 🔌 Plano de Integrações

| # | Sistema | Direção | Método | Objetivo |
|---|---|---|---|---|
| 1 | Site WordPress público | Site → Plataforma | Webhook + API | Capturar leads/inscrições |
| 2 | Gateway de Doações (Pagar.me) | Bi-direcional | Webhook + API | Registrar doações, atualizar status |
| 3 | ERP Contábil | Plataforma → ERP | API REST diária | Conciliação financeira |
| 4 | E-mail Marketing (Mailchimp) | Plataforma → EMKT | API | Segmentação e campanhas |
| 5 | Google Workspace | SSO | OAuth 2.0 | Login unificado |
| 6 | WhatsApp Business API | Plataforma → WA | API | Comunicação com famílias |
| 7 | Metabase | Postgres → BI | JDBC | Dashboards |

## Padrões
- Todas as chamadas com retry exponencial e DLQ
- Contratos versionados (`/v1`, `/v2`)
- Logs estruturados com correlation-id
