## Testes de Continuidade e Validação

Serão realizados testes periódicos para validar o plano de continuidade e o funcionamento das soluções migradas:
- Testes de failover com Azure Site Recovery (ASR) simulando falhas críticas do ambiente on-premises.
- Validações pós-migração de banco de dados, file server e aplicações Web App para garantir integridade e desempenho.
- Execução de testes de carga em ambientes Web App provisionados para avaliar elasticidade e tempo de resposta.


## Plano de Disaster Recovery

O ambiente de DR utiliza Azure Site Recovery para replicação de workloads críticos. Os parâmetros definidos são:

- RTO (Recovery Time Objective): até 30 minutos
- RPO (Recovery Point Objective): até 15 minutos
