# 🔒 Plano LGPD & Governança de Dados

## Bases Legais
| Dado | Titular | Base Legal |
|---|---|---|
| Cadastro beneficiário | Família | Consentimento + Proteção da Vida |
| Cadastro doador | Doador | Execução de contrato |
| Newsletter | Assinante | Consentimento |
| Voluntário | Voluntário | Execução de contrato |

## Controles
- Criptografia AES-256 em campos sensíveis (CPF, laudos)
- Trilha de auditoria imutável (append-only)
- Retenção: beneficiários 5 anos após inatividade; doadores 10 anos (fiscal)
- Portal do titular: exportação e exclusão on-demand
- DPIA revisado a cada release maior

## Papéis
- **DPO**: aprovação de novos tratamentos
- **Controlador**: ONG
- **Operadores**: cloud, gateway, e-mail marketing (contratos com cláusula LGPD)
