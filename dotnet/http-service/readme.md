# Agente de Serviço HTTP (.NET)

Este agente gera uma camada de serviço completa para comunicar com APIs externas, seguindo as melhores práticas da Microsoft (Dependency Injection, Options Pattern, Typed Clients).

## Variáveis de Entrada
* `namespace`: O namespace do teu projeto (ex: `MeuProjeto.Services`).
* `serviceName`: O nome da classe de serviço (ex: `PagamentoService`).
* `resourceName`: O objeto que está a ser manipulado (ex: `Pagamento`).

## O que é gerado?
1. **Configuração**: Mapeamento seguro de `client_id` e `token`.
2. **Interface**: Contrato do serviço.
3. **Implementação**: Uso de `HttpClient` com tratamento de exceções.
4. **Setup**: Código para o `Program.cs`.
5.  **Test Generator:** Cria os testes unitários utilizando xUnit e Moq, simulando o `HttpClient`.

## 📂 Estrutura dos Arquivos

```text
/prompts
│
├── prompt.yaml        # Prompt para gerar o Código do Serviço
└── prompt-test.yaml   # Prompt para gerar os Testes Unitários
