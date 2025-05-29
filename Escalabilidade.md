## Escalabilidade sob Demanda e Alta Disponibilidade

Para suportar picos de acesso durante períodos promocionais ou eventos sazonais, a arquitetura utilizará:
- Auto Scale em Web Apps com base em métricas de CPU, memória e requisições por segundo.
- App Service Plan Premium com instâncias adicionais pré-configuradas.
- Balanceamento de carga via Application Gateway com suporte a múltiplas zonas de disponibilidade.

## Independência dos Serviços

Ambos os serviços rodam em Web Apps independentes com base de dados desacopladas.

- O serviço de **Lançamentos** continua funcional mesmo com falha total do **Consolidado**.
- Cada serviço tem escalabilidade e disponibilidade separada.

[<< Previous Main](README.md) 