## Automação com Infraestrutura como Código

- Provisionamento de infraestrutura Azure será realizado via Terraform, garantindo reprodutibilidade e versionamento da arquitetura.
- Ansible será utilizado para configuração pós-provisionamento de servidores e serviços, assegurando padronização operacional.

## Governança e Compliance

A estratégia de governança considera os seguintes pilares:
- Controle de acesso baseado em papéis (RBAC) utilizando Entra ID (Azure AD).
- Aplicação de políticas com Azure Policy para conformidade com regras internas e externas.
- Uso planejado de Azure Blueprints para padronização de ambientes, garantindo consistência entre Dev, Homologação e Produção.

## FinOps

- Monitoramento contínuo de custos com integração Datadog + Cost Management.
- Políticas de shutdown automático de recursos fora do horário comercial.
- Auto Scale configurado para reduzir instâncias ociosas.
- Infraestrutura criada com Terraform, permitindo revisão e auditoria de consumo.