# Estratégia de Modernização – Ambiente XPTO

## Índice

- [Contexto do Produto](#contexto-do-produto)
- [Fluxo de Tráfego da Solução](#fluxo-de-tráfego-da-solução)
- [Fase 1 - Continuidade Operacional (DR Híbrido)](Topologia_Fase-01_DR_Hibrido.md)
- [Fases 2 a 5 - Migração e Modernização de Serviços](Topologia_Fase-02_WebApp.md)
- [Escalabilidade e Independência dos Serviços](Escalabilidade.md)
- [Dimensionamento de Recursos](Dimensionamento_Recursos.md)
- [Disaster Recovery](Disaster_Recovery.md)
- [Monitoramento e Observabilidade](Monitoramento_Observabilidade.md)
- [Segurança, Protocolos e Diagnóstico OSI](Justificativas.md)
- [FinOps, Automação e Governança](Estrategia_FinOps.md)

## Contexto do Produto

O projeto de modernização tem como foco inicial a aplicação de Fluxo de Caixa, composta por dois serviços executados atualmente em servidores on-premises:

- Serviço de Controle de Lançamentos: responsável pelo registro e manutenção de lançamentos financeiros no ambiente operacional da empresa.
- Serviço de Consolidação Diária: realiza a agregação e apuração de dados financeiros de diversos sistemas, consolidando informações estratégicas. Esses serviços serão gradualmente migrados para Web Apps e futuramente containerizados em AKS.

## Fluxo de Tráfego da Solução

1. Usuário acessa Web App via Application Gateway (WAF) pela Internet.
2. Web App se conecta ao Azure SQL para dados ou Azure Files para documentos.
3. Monitoramento contínuo coleta métricas e envia para Datadog.
4. Conexão VPN garante integração com recursos on-premises (AD, cache local, etc).

[Next Page](Topologia_Fase-01_DR_Hibrido.md)
