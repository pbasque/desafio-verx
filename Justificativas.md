## Segurança e Protocolos de Comunicação

- Utilização obrigatória de HTTPS (TLS 1.2 ou superior) em todas as aplicações Web.
- Acesso SSH restrito por chave pública e segmentado por regras específicas em NSG (Network Security Group).
- Inspeção de pacotes via Azure WAF e análise de payloads para mitigar riscos de ataque.

## Diagnóstico e Performance com Modelo OSI

- Utilização de práticas baseadas no Modelo OSI para identificação de gargalos de rede e sistema.
- Camadas 3 e 4: Monitoramento de IP, portas e conexões com Datadog e Azure NSG.
- Camadas 6 e 7: Logs de aplicação e inspeção de tráfego HTTP via WAF e Datadog.

## Protocolos Utilizados para Administração e Monitoramento

- Administração: SSH (key-based), HTTPS (TLS 1.2+), RDP com restrição por NSG.
- Monitoramento: SNMP para camadas de rede, API do Datadog para coleta e geração de alertas.

## Integração On-Premises + Cloud

**Benefícios**:
- Continuidade de investimentos existentes (VMware, AD)
- Adoção gradual sem reescrita de aplicação
- Baixa latência via VPN/BGP

**Desafios**:
- Complexidade de gerenciamento híbrido
- Dependência de conectividade estável
- Diferenças de performance e visibilidade entre ambientes

## Uso de Kubernetes x Serverless

- Aplicações Web simples e de média carga: Web App + Serverless (Azure Function) para escalabilidade automática.
- Microsserviços com alta complexidade ou dependência de APIs em cadeia: containers orquestrados em AKS.

Planeja-se refactor dos serviços atuais para AKS a médio/longo prazo.

[<< Previous](Monitoramento_Observabilidade.md)   -   [Next Page >>](Estrategia_FinOps.md)