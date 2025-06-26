# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

**Considerações:** As estimativas financeiras que usei no relatório foram baseadas em médias de mercado observadas em empresas de médio porte, como hubs de distribuição, com características parecidas às de uma indústria farmacêutica com operações B2B.

Data: 26/06/25  
Empresa: Abstergo Industries  
Responsável: Luiz Silva  

## Introdução
Este relatório apresenta o processo de implementação de ferramentas na empresa *Abstergo Industries*, realizado por Luiz Silva. O objetivo do projeto foi elencar 3 serviços AWS com foco em redução de custos imediatos, aproveitando a elasticidade, automação e modelos de pagamento sob demanda da nuvem.

## Descrição do Projeto
O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos específicos. A seguir, serão descritas as etapas do projeto:

**Etapa 1:**
- **Nome da ferramenta:** Amazon EC2 (com instâncias spot)
- **Foco da ferramenta:** Computação escalável e sob demanda
- **Descrição de caso de uso:** Utilização de instâncias spot para executar processos de análise de dados e relatórios fora do horário comercial, como extrações de dados do ERP e consolidações semanais. As instâncias spot oferecem até 90% de desconto em relação às instâncias sob demanda, permitindo economia significativa para cargas que podem ser interrompidas e retomadas.
- **Estimativa de ganho financeiro:** Redução de até 70% nos custos de servidores dedicados on-premise utilizados para tarefas esporádicas, representando uma economia mensal estimada de R$ 8.000,00 [[1](https://aws.amazon.com/solutions/case-studies/mercadolibre-ec2/)], [[2](https://aws.amazon.com/solutions/case-studies/Drip-ec2-spot/)].

**Etapa 2:**
- **Nome da ferramenta:** Amazon S3 (com políticas de ciclo de vida)
- **Foco da ferramenta:** Armazenamento escalável e de baixo custo
- **Descrição de caso de uso:** Substituição de servidores de arquivos locais por buckets no Amazon S3 com uso de políticas de ciclo de vida, migrando dados antigos para classes como S3 Glacier e Glacier Deep Archive. Ideal para armazenar notas fiscais eletrônicas, históricos de pedidos e documentos regulatórios com acesso eventual.
- **Estimativa de ganho financeiro:** Redução de até 80% em comparação com storage on-premise e manutenção de servidores NAS, com uma economia anual estimada de R$ 50.000,00[[3](https://aws.amazon.com/blogs/storage/amazon-s3-cost-optimization-for-predictable-and-dynamic-access-patterns/)], [[4](https://aws.criticalcloud.ai/s3-lifecycle-rules-cost-saving-tips/)].

**Etapa 3:**
- **Nome da ferramenta:** AWS Lambda
- **Foco da ferramenta:** Execução de código sem gerenciamento de servidores
- **Descrição de caso de uso:** Automatização de tarefas operacionais, como verificação diária de estoques e envio de alertas para o time comercial. Com o uso do AWS Lambda, a empresa evita manter servidores ligados o tempo todo, pagando apenas pelo tempo de execução do código.
- **Estimativa de ganho financeiro:** Redução de custos com servidores ociosos e administração de infraestrutura, com uma economia mensal estimada de R$ 2.000,00 [[5](https://aws.amazon.com/solutions/case-studies/katalon-lambda-case-study/)], [[6](https://aws.amazon.com/solutions/case-studies/capital-one-lambda-ecs-case-study/)].



## Conclusão
A implementação de ferramentas na empresa *Abstergo Industries* tem como esperado a redução significativa de custos com infraestrutura física, aumento de escalabilidade e melhoria na automação de processos internos, o que aumentará a eficiência e a produtividade da empresa. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam melhorar ainda mais os processos da empresa.    
  
Economia estimada total por ano: **R$ 170.000,00**
```
Serviço        | Economia Mensal Estimada           Valor
------------------------------------------------------------
EC2 Spot       | ██████████████████████████         R$ 8.000,00
Amazon S3      | █████████████                      R$ 4.166,67
AWS Lambda     | ██████                             R$ 2.000,00

```

## Anexos
[1] - Mercado Libre: ao migrar 30% de suas instâncias sob demanda para Spot, economizou 31% nos custos de computação mensal logo no primeiro mês - https://aws.amazon.com/solutions/case-studies/mercadolibre-ec2/  
[2] - Drip: economizou pelo menos 65 % (mais de US$ 100.000) durante um pico sazonal, ao migrar grande parte da carga para Spot - https://aws.amazon.com/solutions/case-studies/Drip-ec2-spot/  
[3] - Amazon S3 cost optimization for predictable and dynamic access patterns - https://aws.amazon.com/blogs/storage/amazon-s3-cost-optimization-for-predictable-and-dynamic-access-patterns/
[4] - S3 Lifecycle Rules: Cost-Saving Tips - https://aws.criticalcloud.ai/s3-lifecycle-rules-cost-saving-tips/  
[5] - Katalon: conseguiu economizar até 70 % no processamento de streaming usando AWS Lambda para análise de qualidade - https://aws.amazon.com/solutions/case-studies/katalon-lambda-case-study/  
[6] - Capital One: relata economias de até 90 % no custo de aplicações após migração para arquitetura serverless com Lambda + ECS - https://aws.amazon.com/solutions/case-studies/capital-one-lambda-ecs-case-study/

Assinatura do Responsável pelo Projeto:

Luiz Silva
