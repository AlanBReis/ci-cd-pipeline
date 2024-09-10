# CI/CD Pipeline

Este repositório demonstra a configuração de workflows usando GitHub Actions para automatizar processos de integração e entrega contínua (CI/CD). O foco principal deste repositório não está no código da aplicação em si, mas na configuração dos workflows que facilitam a automação de tarefas comuns no desenvolvimento.

## Workflows

### 1. Deployment Workflow

O workflow de deployment é acionado sempre que um push é feito no repositório. Ele realiza as seguintes etapas:

1. **Baixa a versão mais recente do código**: Faz o checkout da versão mais recente do repositório.
2. **Instala as dependências**: Utiliza `npm ci` para instalar as dependências do projeto.
3. **Executa o script de teste**: Realiza linting e testes automatizados para garantir que o código está correto e sem erros.
4. **Build do código**: Constrói o código para preparar a aplicação para produção.
5. **Mensagem de deploy**: Exibe uma mensagem `echo deploying...` para indicar que o processo de deployment está sendo executado.

O arquivo de configuração para este workflow é `deployment.yml` e está localizado em `.github/workflows/`.

### 2. Issue Workflow

O workflow de gerenciamento de issues é acionado quando um evento de issue ocorre (por exemplo, quando uma nova issue é criada ou uma issue existente é atualizada). Ele realiza as seguintes etapas:

1. **Output dos detalhes do evento**: Exibe detalhes do evento de issue que acionou o workflow, útil para depuração e auditoria.

O arquivo de configuração para este workflow é `issue.yml` e está localizado em `.github/workflows/`.

## Como Usar

1. **Clone o Repositório**:
   ```sh
   git clone https://github.com/AlanBReis/ci-cd-pipeline.git
   ```

2. **Configuração**:

Certifique-se de que seu repositório GitHub esteja configurado corretamente para usar GitHub Actions.
Personalize os arquivos de workflow conforme necessário para atender aos requisitos do seu projeto.


3. **Acompanhe os Workflows**:

Visite a aba "Actions" no GitHub para visualizar a execução dos workflows e os resultados.
Contribuição
Se você deseja contribuir com melhorias ou adicionar novos workflows, sinta-se à vontade para abrir uma issue ou um pull request.
