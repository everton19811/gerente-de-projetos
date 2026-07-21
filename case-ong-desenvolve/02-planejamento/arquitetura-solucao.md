# 🏗️ Arquitetura da Solução

## Visão Geral
Aplicação **web-first**, monolito modular com API REST, banco Postgres e frontend React. Deploy em nuvem gerenciada com CDN para o portal público.

## Camadas
```
[ Site público (WP) ] ──► [ API Gateway ] ──► [ Backend Node/Django ] ──► [ Postgres ]
                                    │                                          │
                              [ Fila (SQS) ]                            [ S3 – Anexos ]
                                    │
                    ┌───────────────┼────────────────┐
                    ▼               ▼                ▼
             [ Gateway Doações ] [ E-mail MKT ]  [ ERP Contábil ]
                                    │
                              [ BI – Metabase ]
```

## Componentes
- **CRM**: entidades Pessoa, Família, Interação, Doação
- **Portal Editorial**: Artigo, Revisão, Publicação, Categoria, Autor
- **Integrações**: webhooks + workers assíncronos
- **BI**: réplica leitura em Postgres + Metabase
- **IAM**: SSO Google Workspace + RBAC

## Decisões (ADR resumidas)
- ADR-001: **Monolito modular** vs microserviços — menor complexidade operacional para uma ONG
- ADR-002: **Postgres único** com schemas por domínio
- ADR-003: **Metabase open-source** para BI (custo zero de licença)
- ADR-004: **LGPD by design** — criptografia de campo em dados sensíveis
