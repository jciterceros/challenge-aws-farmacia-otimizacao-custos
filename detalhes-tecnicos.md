## Detalhes Técnicos das Configurações dos Serviços AWS Utilizados

### AWS Lambda
- Responsabilidade: Executar funções serverless para automação de processos, integração entre sistemas, processamento de eventos e tarefas agendadas.
- Exemplos de uso: Atualização de estoque, envio de notificações, backup automático.
- Integração: Recebe eventos do S3, acessa dados no RDS, armazena arquivos no S3.
- Documentação: [AWS Lambda - Documentação Oficial](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)
- Exemplo de configuração (console):
  - Trigger: S3 (evento de upload)
  - Runtime: Python 3.9
  - Permissões: Acesso ao S3 e RDS via IAM Role

### Amazon RDS (PostgreSQL)
- Responsabilidade: Armazenar e gerenciar dados relacionais (estoque, pedidos, usuários) de forma segura, escalável e com alta disponibilidade.
- Exemplos de uso: Persistência de dados transacionais, consultas SQL, backup e recuperação.
- Integração: Acessado por funções Lambda e aplicações backend.
- Documentação: [Amazon RDS - Documentação Oficial](https://docs.aws.amazon.com/pt_br/AmazonRDS/latest/UserGuide/Welcome.html)
- Configuração:
  - Instância db.t3.micro (exemplo para ambiente de desenvolvimento)
  - Multi-AZ habilitado para alta disponibilidade
  - Backup automático diário
  - Parâmetros customizados para performance (max_connections, work_mem)
  - Segurança: acesso restrito por grupo de segurança e VPC

### Amazon S3
- Responsabilidade: Armazenar objetos (documentos, imagens, backups) de forma econômica, segura e escalável.
- Exemplos de uso: Armazenamento de arquivos de pedidos, imagens de produtos, backups automáticos.
- Integração: Gatilho de eventos para Lambda, destino de backups, armazenamento de logs.
- Documentação: [Amazon S3 - Documentação Oficial](https://docs.aws.amazon.com/pt_br/AmazonS3/latest/userguide/Welcome.html)
- Configuração:
  - Buckets separados para documentos, imagens e backups
  - Políticas de ciclo de vida para mover arquivos antigos para S3 Glacier
  - Versionamento habilitado para proteção contra deleção acidental
  - Permissões via IAM e políticas de bucket

### EC2 Auto Scaling
- Responsabilidade: Garantir escalabilidade automática do backend, ajustando a quantidade de instâncias EC2 conforme a demanda.
- Exemplos de uso: Hospedagem do backend da aplicação, processamento de cargas variáveis.
- Integração: Balanceamento de carga com Elastic Load Balancer, comunicação com Lambda e RDS.
- Documentação: [Amazon EC2 Auto Scaling - Documentação Oficial](https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html)
- Configuração:
  - Grupo de Auto Scaling com instâncias EC2 para backend do sistema
  - Políticas de scaling baseadas em CPU e requisições
  - Integração com Elastic Load Balancer
  - Imagem customizada (AMI) com aplicação Spring Boot

### AWS Cost Explorer
- Responsabilidade: Monitorar, analisar e reportar os custos dos serviços AWS, permitindo otimização e controle financeiro.
- Exemplos de uso: Relatórios mensais/diários de custos, alertas de orçamento, exportação de dados para análise.
- Integração: Utilizado por gestores e administradores para acompanhamento de gastos.
- Documentação: [AWS Cost Explorer - Documentação Oficial](https://docs.aws.amazon.com/cost-management/latest/userguide/ce-what-is.html)
- Configuração:
  - Relatórios automáticos de custos por serviço, tag e período
  - Alertas de orçamento configurados
  - Exportação de relatórios em CSV para análise detalhada
