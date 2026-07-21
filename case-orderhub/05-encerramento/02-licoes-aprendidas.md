# Lições Aprendidas — OrderHub

## O que funcionou bem 👍
1. **Discovery estruturado antes de codar** — 6 semanas de descoberta evitaram retrabalho estimado em R$ 180k
2. **Piloto controlado com 20 clientes** — capturou 47 bugs e 12 melhorias antes do go-live geral
3. **Middleware desacoplado do SAP** — permitiu que o SAP sofresse upgrade sem parar o OrderHub
4. **Weekly com Sponsor** — decisões em <48h em 100% dos casos
5. **DPIA no início** — evitou refactor caro em LGPD

## O que precisa melhorar 👎
1. **Estimativas de integração** — subestimadas em ~20% (usar T-shirt sizing + histórico)
2. **Onboarding do dev sênior novo** — 3 semanas até produtividade plena; criar programa
3. **Documentação da API** — atrasada em 2 sprints; incluir como Definition of Done
4. **Comunicação com clientes fora do piloto** — geraram ansiedade; criar newsletter externa antes

## Recomendações para próximos projetos
- Reservar 15% do orçamento para contingência em projetos com integração legado (usamos 10%, quase estourou)
- Adotar **DORA metrics** desde o dia 1
- Contratar UX pesquisador nas próximas fases (o hands-on de UX cobriu, mas pesquisa quali ficou fraca)

## Post-Mortem: Incidente P1 em 12/set
- **Fato:** timeout na sync de estoque, 40min de indisponibilidade
- **Causa raiz:** limite de conexões Postgres não dimensionado para pico Black Friday piloto
- **Ação:** connection pooling + alarme APM em 70% do limite
- **Blameless:** aprendizado, não punição
