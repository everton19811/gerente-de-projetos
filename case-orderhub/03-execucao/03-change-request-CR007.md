# Change Request CR-007 — SSO Azure AD

## Solicitante
Diretor de TI | Data: 20/06/2024

## Descrição
Adicionar autenticação SSO via Azure AD para usuários internos, substituindo login local previsto originalmente.

## Justificativa
- Alinhamento com política corporativa aprovada em mai/24
- Reduz suporte de senha (economia ~R$ 24k/ano)
- Melhora segurança (MFA nativo)

## Impactos
| Dimensão | Impacto |
|----------|---------|
| Escopo | +1 história (SSO) + ajuste 3 telas |
| Prazo | +7 dias corridos (absorvido em buffer) |
| Custo | +R$ 38k (licenças + dev) |
| Riscos | Baixo — SDK maduro |
| Qualidade | Positivo (MFA) |

## Análise de Alternativas
- **A) Fazer agora:** custo R$ 38k, prazo +7d ✅ recomendado
- B) Fase 2: custo R$ 65k (retrabalho), risco churn interno

## Aprovação
Sponsor ______ | CFO ______ | Data 28/06/2024 | ✅ Aprovado
