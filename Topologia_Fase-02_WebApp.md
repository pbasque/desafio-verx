# Fases 2 a 5 - Modernização de WebApp e Serviços Gerenciados

## Fase 2
- Migrar o SQL Server para Azure SQL Managed Instance, visando escalabilidade, alta disponibilidade e manutenção simplificada.
- Reconfigurar backups gradativamente para refletir o novo destino.
- Realizar testes de integridade e desempenho pós-migração.

## Fase 3
- Migrar o File Server para Azure Files com integração do File Sync para manter sincronização temporária com ambiente on-premises.
- Atualizar regras de backup e autenticação conforme a nova arquitetura.

## Fase 4
- Converter aplicações legadas baseadas em IIS para Azure Web App, iniciando com os sites atualmente rodando no IIS.
- Migrar SRV APP LANÇAMENTOS e SRV APP CONSOLIDADOS para Web App, desativando gradualmente os serviços legados.
- Atualizar o DR conforme as aplicações são modernizadas, retirando as VMs do plano de replicação.
- Reconfigurar autenticação progressivamente para uso exclusivo de Entra ID (Azure AD).

## Fase 5
- Após estabilização das fases anteriores, iniciar refactory das aplicações para arquitetura de microsserviços baseados em containers.
- Utilizar Azure Kubernetes Service (AKS) como plataforma de orquestração.
- Aplicações devem ser desenvolvidas visando escalabilidade, governança e observabilidade.


![Topologia Fase 02](Topologia_Fase-02_Web-App.jpg)


[<< Previous](Topologia_Fase-01_DR_Hibrido.md)   -   [Next Page >>](Escalabilidade.md)
