# 📥 Plano de Migração — Planilhas → Plataforma

## Etapas
1. **Inventário**: catalogar todas as planilhas ativas (esperado ~40 arquivos)
2. **Perfilamento**: usar Python/pandas para medir qualidade (nulos, duplicatas, formatos)
3. **Padronização**: mapear colunas ↔ campos do CRM
4. **Limpeza**: normalizar CPF, telefone, endereço; dedupe fuzzy
5. **Carga em Staging**: importar para schema `staging`
6. **Validação por área**: coord. programas revisa amostra 10%
7. **Promoção para Produção**: transacional, com rollback
8. **Arquivamento**: planilhas viram somente-leitura

## Métricas de Qualidade Alvo
- ≥ 98% dos registros com campos obrigatórios preenchidos
- ≤ 1% de duplicatas após dedupe
- 100% dos consentimentos LGPD rastreáveis
