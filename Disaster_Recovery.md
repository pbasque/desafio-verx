## Testes de Continuidade e Validação

Serão realizados testes periódicos para validar o plano de continuidade e o funcionamento das soluções migradas:
- Testes de failover com Azure Site Recovery (ASR) simulando falhas críticas do ambiente on-premises.
- Validações pós-migração de banco de dados, file server e aplicações Web App para garantir integridade e desempenho.
- Execução de testes de carga em ambientes Web App provisionados para avaliar elasticidade e tempo de resposta.

Dimensionamento de Recursos

Para garantir desempenho e escalabilidade adequada, os serviços foram dimensionados da seguinte forma:

- **Serviço de Lançamentos**:
  - CPU: 2 vCPUs
  - Memória: 4 GB
  - Tipo: App Service Plan Premium v3 (P1v3)
  - Escala: Horizontal com 1 a 3 instâncias via Auto Scale

- **Serviço de Consolidados**:
  - CPU: 4 vCPUs
  - Memória: 8 GB
  - Tipo: App Service Plan Premium v3 (P2v3)
  - Escala: Horizontal com 1 a 5 instâncias

- **Azure SQL Managed Instance**:
  - Tier: General Purpose
  - vCores: 8
  - Memória: 32 GB
  - Storage inicial: 512 GB, escalável

- **Azure Files + Sync**:
  - Storage Account GPv2, com redundancy ZRS
  - File Sync habilitado com cache local

## Plano de Disaster Recovery

O ambiente de DR utiliza Azure Site Recovery para replicação de workloads críticos. Os parâmetros definidos são:

- RTO (Recovery Time Objective): até 30 minutos
- RPO (Recovery Point Objective): até 15 minutos

As ativações são automatizadas via Azure Function e testadas trimestralmente.