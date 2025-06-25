# RELATÓRIO DE OTIMIZAÇÃO DE CUSTOS EM FARMÁCIAS COM AWS

Data: 2024-06-10  
Empresa: Farmacias Populares  
Responsável: Fernando Flores Terceros

## INTRODUÇÃO

Este relatório foi elaborado como parte do desafio de projeto do bootcamp **Java AI Powered** promovido pela Digital Innovation One (DIO). O objetivo é apresentar um estudo sobre a aplicação de serviços AWS para otimização de custos em farmácias, abordando arquitetura cloud escalável, automação de processos e estratégias para redução de despesas operacionais.

## DESCRIÇÃO DO PROJETO

A farmácia busca modernizar sua infraestrutura tecnológica, tornando-a mais eficiente e econômica. Para isso, foram selecionados e implementados serviços AWS que proporcionam escalabilidade, automação e controle de custos, conforme as melhores práticas de cloud computing.

### Tecnologias e Serviços Utilizados
- **AWS Lambda (Serverless):** Automatização de processos como gestão de estoque e pedidos, eliminando a necessidade de servidores dedicados e reduzindo custos com infraestrutura ociosa.
- **Amazon RDS (PostgreSQL/MySQL):** Gerenciamento de banco de dados relacional com alta disponibilidade, escalabilidade automática e backups gerenciados, otimizando recursos e custos.
- **AWS Cost Explorer:** Monitoramento e análise detalhada dos custos dos serviços AWS, permitindo identificar oportunidades de economia e ajustar o consumo conforme a demanda.
- **EC2 Auto Scaling:** Ajuste automático da capacidade computacional de acordo com a demanda, evitando gastos desnecessários com instâncias subutilizadas.
- **Amazon S3:** Armazenamento econômico e seguro de dados, como documentos, imagens de produtos e backups, com políticas de ciclo de vida para otimização de custos.

## ETAPAS DE IMPLEMENTAÇÃO

### 1. Levantamento de Necessidades e Planejamento
- Análise dos processos internos da farmácia para identificar oportunidades de automação e redução de custos.
- Definição dos requisitos de armazenamento, processamento e banco de dados.

### 2. Arquitetura e Configuração dos Serviços AWS
- **Amazon S3:**
  - Criação de buckets para armazenamento de arquivos e backups.
  - Definição de políticas de ciclo de vida para mover dados antigos para classes de armazenamento mais baratas (ex: S3 Glacier).
- **AWS Lambda:**
  - Desenvolvimento de funções para automação de tarefas rotineiras (ex: atualização de estoque, envio de notificações de pedidos).
  - Integração com outros serviços AWS (S3, RDS) para orquestração de processos.
- **Amazon RDS:**
  - Provisionamento de instância PostgreSQL/MySQL com escalabilidade automática.
  - Configuração de backups automáticos e políticas de segurança.
- **EC2 Auto Scaling:**
  - Criação de grupos de Auto Scaling para workloads variáveis, garantindo performance e economia.
- **AWS Cost Explorer:**
  - Configuração de relatórios e alertas para monitoramento contínuo dos custos.

### 3. Migração e Otimização
- Migração dos dados e processos para a nuvem AWS.
- Ajustes finos nas configurações para maximizar a eficiência e minimizar custos.
- Treinamento da equipe para uso das novas ferramentas e acompanhamento dos gastos.

## RESULTADOS E BENEFÍCIOS
- Redução significativa dos custos operacionais com infraestrutura de TI.
- Maior escalabilidade e flexibilidade para lidar com variações de demanda.
- Automação de processos críticos, liberando a equipe para atividades estratégicas.
- Monitoramento contínuo dos custos, permitindo ajustes proativos.
- Armazenamento seguro e econômico de dados sensíveis e operacionais.

## CONCLUSÃO

A adoção de serviços AWS permitiu à farmácia modernizar sua operação, tornando-a mais eficiente, escalável e econômica. O uso de soluções serverless, banco de dados gerenciado, automação e monitoramento de custos são fundamentais para garantir competitividade e sustentabilidade no setor farmacêutico.

## ANEXOS
1. [Detalhes técnicos das configurações dos serviços AWS utilizados](./detalhes-tecnicos.md)
2. [Exemplos de código das funções Lambda implementadas](./exemplos-lambda.md)
3. [Relatórios de custos gerados pelo AWS Cost Explorer](./detalhes-tecnicos.md#relatórios-de-custos-gerados-pelo-aws-cost-explorer)
4. [Documentação Visual: Modelo C4 (Mermaid)](./documentacao-c4.md)

---

## Referências:
- [AWS Lambda - Documentação Oficial](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)
- [Amazon RDS - Documentação Oficial](https://docs.aws.amazon.com/pt_br/AmazonRDS/latest/UserGuide/Welcome.html)
- [AWS Cost Explorer - Documentação Oficial](https://docs.aws.amazon.com/cost-management/latest/userguide/ce-what-is.html)
- [Amazon EC2 Auto Scaling - Documentação Oficial](https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html)
- [Amazon S3 - Documentação Oficial](https://docs.aws.amazon.com/pt_br/AmazonS3/latest/userguide/Welcome.html)

---

Assinatura do Responsável pelo Projeto: Fernando Flores Terceros