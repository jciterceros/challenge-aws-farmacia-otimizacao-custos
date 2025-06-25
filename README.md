# Challenge AWS Farmácia - Otimização de Custos

Este repositório apresenta um estudo e implementação de arquitetura cloud para otimização de custos em farmácias utilizando serviços AWS. O projeto foi desenvolvido como parte do bootcamp **Java AI Powered** da Digital Innovation One (DIO).

## Objetivo

Analisar, propor e documentar uma arquitetura escalável e econômica para farmácias, automatizando processos como gestão de estoque e pedidos, e aplicando estratégias para redução de despesas operacionais com computação, armazenamento e banco de dados.

## Principais Tecnologias e Serviços AWS
- **AWS Lambda:** Funções serverless para automação de processos (ex: atualização de estoque, backup, notificações).
- **Amazon RDS (PostgreSQL/MySQL):** Banco de dados relacional gerenciado, com alta disponibilidade e backups automáticos.
- **Amazon S3:** Armazenamento econômico e seguro de arquivos, documentos e backups, com políticas de ciclo de vida.
- **EC2 Auto Scaling:** Escalabilidade automática do backend conforme a demanda.
- **AWS Cost Explorer:** Monitoramento e análise detalhada dos custos dos serviços AWS.

## Estrutura do Projeto

- `relatorio.md`: Relatório completo do estudo, arquitetura, etapas de implementação, resultados e anexos.
- `detalhes-tecnicos.md`: Detalhes técnicos das configurações dos serviços AWS utilizados.
- `exemplos-lambda.md`: Exemplos de código das funções Lambda implementadas para automação de processos.
- `documentacao-c4.md`: Documentação visual da arquitetura do projeto utilizando o Modelo C4 em Mermaid.
- `modelo-relatorio.md`: Template para criação de novos relatórios de implementação de projetos AWS.

## Como navegar

- Consulte o [relatório principal](./relatorio.md) para entender o contexto, as decisões de arquitetura e os resultados do projeto.
- Veja os [detalhes técnicos](./detalhes-tecnicos.md) para configurações e responsabilidades de cada serviço AWS.
- Explore os [exemplos de código Lambda](./exemplos-lambda.md) para automação de processos.
- Visualize a [documentação C4 em Mermaid](./documentacao-c4.md) para entender a arquitetura de alto nível.
- Utilize o [modelo de relatório](./modelo-relatorio.md) como base para novos projetos.

## Anexos
- [Detalhes técnicos das configurações dos serviços AWS utilizados](./detalhes-tecnicos.md)
- [Exemplos de código das funções Lambda implementadas](./exemplos-lambda.md)
- [Relatórios de custos gerados pelo AWS Cost Explorer](./detalhes-tecnicos.md#relatórios-de-custos-gerados-pelo-aws-cost-explorer)
- [Documentação Visual: Modelo C4 (Mermaid)](./documentacao-c4.md)

## Referências
- [AWS Lambda - Documentação Oficial](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)
- [Amazon RDS - Documentação Oficial](https://docs.aws.amazon.com/pt_br/AmazonRDS/latest/UserGuide/Welcome.html)
- [AWS Cost Explorer - Documentação Oficial](https://docs.aws.amazon.com/cost-management/latest/userguide/ce-what-is.html)
- [Amazon EC2 Auto Scaling - Documentação Oficial](https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html)
- [Amazon S3 - Documentação Oficial](https://docs.aws.amazon.com/pt_br/AmazonS3/latest/userguide/Welcome.html) 