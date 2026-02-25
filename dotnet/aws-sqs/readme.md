## ☁️ AWS SQS Service Generator

Gera um serviço de mensageria que se adapta automaticamente entre ambiente local (LocalStack) e produção (AWS).

**Prompt File:** `prompts/sqs-service.yaml`

### Variáveis de Entrada
| Variável | Descrição | Exemplo |
| :--- | :--- | :--- |
| `namespace` | O namespace do projeto. | `MeuProjeto.Messaging` |
| `serviceName` | Nome da classe de serviço. | `NotificationProducer` |
| `queueName` | Nome da fila SQS. | `user-notifications` |

### Funcionalidade LocalStack
O código gerado no `Program.cs` verifica a presença da chave `ServiceUrl`.
- **Desenvolvimento Local:** Definir `ServiceUrl` como `http://localhost:4566` no `appsettings.json`.
- **Produção:** Remover ou deixar `ServiceUrl` vazio (o SDK assumirá as credenciais/region padrão da AWS).

### Dependências NuGet Necessárias
* `AWSSDK.SQS`
* `AWSSDK.Extensions.NETCore.Setup`
* `Microsoft.Extensions.Options.ConfigurationExtensions`
