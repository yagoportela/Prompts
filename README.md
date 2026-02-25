# Prompt Registry (PromptOps)

Este repositório centraliza prompts. Ele armazena, versiona e distribui **Prompts como Código**.

## Estrutura de Pastas

*   `registry.yaml`: O "cérebro" do repositório. Contém metadados, descrições e caminhos para todos os prompts aprovados.
*   `dotnet/`, `python/`, etc.: Pastas organizadas por tecnologia.
*   `*/prompt.yaml`: O arquivo do prompt em si.
*   `*/test-prompt.yaml`: como testar.
*   `*/readme.md`: descrição do prompt.


## Como Usar

### 1. Configuração no seu Projeto (Recomendado)

Para ter acesso fácil aos prompts dentro do seu editor (VS Code / Rider), adicione este repositório como um submódulo na raiz do seu projeto:

```bash
git submodule add git@github.com:sua-org/prompts.git .prompts
```

Isso criará uma pasta oculta `.prompts` contendo toda a biblioteca.

## Contribuindo com Novos Prompts

1.  Crie uma nova pasta para o seu prompt (ex: `react/component-generator`).
2.  Crie o arquivo `prompt.yaml` com as instruções detalhadas.
3.  (Opcional) Crie um `README.md` dentro da pasta explicando variáveis.
4.  **Importante:** Registre o novo prompt no arquivo `registry.yaml` na raiz.

### Padrão do `registry.yaml`

```yaml
agents:
  tecnologia:
    NomeDoPrompt:
      description: "O que faz e QUANDO usar (Gatilho)."
      path: "./caminho/do/prompt"
      entry_point: "prompt.yaml"
```
