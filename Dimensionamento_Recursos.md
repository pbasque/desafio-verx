## Dimensionamento de Recursos

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