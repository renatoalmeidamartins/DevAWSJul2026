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
