# Exemplos de Código das Funções Lambda

## Atualização de Estoque (Python)
```python
import psycopg2
import os

def lambda_handler(event, context):
    conn = psycopg2.connect(
        host=os.environ['DB_HOST'],
        database=os.environ['DB_NAME'],
        user=os.environ['DB_USER'],
        password=os.environ['DB_PASS']
    )
    cursor = conn.cursor()
    pedido_id = event['pedido_id']
    cursor.execute('UPDATE estoque SET quantidade = quantidade - 1 WHERE produto_id = %s', (pedido_id,))
    conn.commit()
    cursor.close()
    conn.close()
    return {'status': 'ok'}
```

## Backup Automático para S3 (Python)
```python
import boto3
import datetime

def lambda_handler(event, context):
    s3 = boto3.client('s3')
    data = 'backup dos dados...'
    nome_arquivo = f"backup_{datetime.datetime.now().isoformat()}.txt"
    s3.put_object(Bucket='meu-bucket-backup', Key=nome_arquivo, Body=data)
    return {'status': 'backup realizado'}
``` 