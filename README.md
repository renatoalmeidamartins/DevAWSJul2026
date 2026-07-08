# DevAWSJul2026

## Links de acesso ao curso
- [Link da reuniao](https://fast-lane.webex.com/fast-lane-pt-br/j.php?MTID=m5bc5c8e36e6d6e5432c089627e2762b0)
- [Acesso a material e laboratorio](https://us-east-1.student.classrooms.aws.training/class/wg7nviASCKEoeAcxs36Ymt)

## Links do dia 1
- [URL de funcoes Lambda](https://aws.amazon.com/blogs/aws/announcing-aws-lambda-function-urls-built-in-https-endpoints-for-single-function-microservices/)
- [X-ray está sendo descontinuado](https://docs.aws.amazon.com/xray/latest/devguide/xray-sdk-migration.html)
- [Sigv4, necessario para enviar pedidos para AWS](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_sigv.html)
- [Criando um pedido assinado com Sigv4, passo-a-passo](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_sigv-create-signed-request.html)
- [Toolkits e SDKs](https://aws.amazon.com/products/developer-tools/)
- O link acima te leva para o [builder center](https://builder.aws.com/build/tools), que vale a pena explorar, em especial as organizacoes de [labs](https://github.com/awslabs) e [samples](https://github.com/aws-samples)
- [Retries nos SDKs](https://docs.aws.amazon.com/sdkref/latest/guide/feature-retry-behavior.html)
- Cada SDK honra as primitivas, ou práticas de desenvolvimento, da linguagem em questão. Um bom exemplo disso é o uso de waiters (para esperar conclusão de operações assíncronas), onde usando o exemplo de CreateTable no DynamoDB, temos:
  - No [.Net](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/getting-started-step-1.html), usa-se task, await, e a chamada Async
  - Em [Python](https://docs.aws.amazon.com/boto3/latest/reference/services/dynamodb/client/get_waiter.html), usa-se o get_waiter
  - En [Java](https://docs.aws.amazon.com/sdk-for-java/latest/developer-guide/examples-dynamodb-tables.html), usa-se a classe DynamoDbWaiter
- Publicação de métricas do SDK, por exmplo,  [Java](https://docs.aws.amazon.com/sdk-for-java/latest/developer-guide/metrics.html)
- [Kiro, IDE agentica](https://kiro.dev/)
- [IAM policy generator](https://awspolicygen.s3.amazonaws.com/policygen.html)
- [Limites de tamanho de politica, efetivamente tamanho do json que a define](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_iam-quotas.html#reference_iam-quotas-entity-length)
- [Logica de avaliacao de politicas IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_evaluation-logic.html)
- [Variavies de ambiente podem armazenar configurações da CLI](https://docs.aws.amazon.com/cli/v1/userguide/cli-configure-envvars.html)
- [Uso de roles na CLI](https://docs.aws.amazon.com/cli/v1/userguide/cli-configure-role.html)
- [Ordem de "busca"de credenciais para conexão com AWS](https://docs.aws.amazon.com/cli/v1/userguide/cli-chap-authentication.html)
- [Comando AssumeRole na API Rest](https://docs.aws.amazon.com/STS/latest/APIReference/API_AssumeRole.html)
- [IAM Roles Anywhere permite que servicos fora da AWS assumam roles na AWS](https://docs.aws.amazon.com/rolesanywhere/latest/userguide/introduction.html)
- [Uso do Identity Center](https://docs.aws.amazon.com/singlesignon/latest/userguide/what-is.html)

## Links do dia 2
- [Tipos de volume do EBS](https://docs.aws.amazon.com/ebs/latest/userguide/ebs-volume-types.html)
- [11 9's de durabilidade, descrito na Google](https://cloud.google.com/blog/products/storage-data-transfer/understanding-cloud-storage-11-9s-durability-target)
- [Tamanho máximo de objeto no S3 agora é de 50 TB](https://aws.amazon.com/about-aws/whats-new/2025/12/amazon-s3-maximum-object-size-50-tb/)
- Tipos de bucket S3, além do tradicional "general purpose":
  - [File system](https://aws.amazon.com/blogs/aws/launching-s3-files-making-s3-buckets-accessible-as-file-systems/)
  - [Vector buckets](https://aws.amazon.com/blogs/aws/introducing-amazon-s3-vectors-first-cloud-storage-with-native-vector-support-at-scale/)
  - [Tables](https://aws.amazon.com/blogs/aws/new-amazon-s3-tables-storage-optimized-for-analytics-workloads/)
  - [Directory bucket / S3 express one-zone](https://aws.amazon.com/s3/storage-classes/express-one-zone/)
- [Video falando sobre a durabilidade do S3](https://www.youtube.com/watch?v=XyRdMT4zUrA)
- [Forcando transporte seguro e uma versao especifica de TLS em um bucket](https://aws.amazon.com/blogs/storage/enforcing-encryption-in-transit-with-tls1-2-or-higher-with-amazon-s3/)
- [Endpoints existentes em S3](https://docs.aws.amazon.com/general/latest/gr/s3.html)
- [PrivateLink em S3, para acesso atraves de VPCs sem internet - em realidade, disponivel para praticamente todos servicos AWS](https://docs.aws.amazon.com/AmazonS3/latest/userguide/privatelink-interface-endpoints.html)
- [Filtrando saida na CLI](https://docs.aws.amazon.com/cli/v1/userguide/cli-usage-filter.html)
- [Desde dezembro de 2025, S3 Object Lambda nao existe mais. Alternativas listadas aqui](https://docs.aws.amazon.com/AmazonS3/latest/userguide/amazons3-ol-change.html)
- [Acesso temporario a objetos no S3 - presign](https://docs.aws.amazon.com/AmazonS3/latest/userguide/ShareObjectPreSignedURL.html)
- [Operacoes batch](https://docs.aws.amazon.com/AmazonS3/latest/userguide/batch-ops.html)
- [Uso de CORS no S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/ManageCorsUsing.html)
- [Multipart upload, existem alternativas de alto nivel para evitar chamads diretas de multipart upload](https://docs.aws.amazon.com/AmazonS3/latest/userguide/mpu-upload-object.html), [S3TransferManager](https://docs.aws.amazon.com/java/api/latest/software/amazon/awssdk/transfer/s3/S3TransferManager.Builder.html) em Java, [transfer](https://docs.aws.amazon.com/boto3/latest/guide/s3.html) em python e [TransferUtility](https://docs.aws.amazon.com/AmazonS3/latest/userguide/HLuploadDirDotNet.html) em .Net ([outro exemplo em .Net](https://aws.amazon.com/blogs/developer/introducing-multipart-download-support-for-aws-sdk-for-net-transfer-manager/))
- [AWS suportando Valkey em lugar do Redis](https://aws.amazon.com/elasticache/redis/)
- [Normalização em bancos de dados relacionais](https://en.wikipedia.org/wiki/Database_normalization)
- [AWS re:Invent 2018: Amazon DynamoDB Deep Dive: Advanced Design Patterns for DynamoDB (DAT401)](https://www.youtube.com/watch?v=HaEPXoXVf2k)
- [Dynamo paper](https://www.allthingsdistributed.com/files/amazon-dynamo-sosp2007.pdf)
- [ExtendDB, DynamoDB open-source com armazenamento plugável](https://aws.amazon.com/blogs/database/introducing-extenddb-an-open-source-dynamodb-compatible-adapter-with-pluggable-storage-backends/)
- [Best practices for designing and architecting with DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/best-practices.html)
- [Choosing the Right DynamoDB Partition Key](https://aws.amazon.com/blogs/database/choosing-the-right-dynamodb-partition-key/)
- [NoSQL workbench, excelente para modelagem nao-relacional](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/workbench.html)
- [DynamoDB local](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBLocal.html)
