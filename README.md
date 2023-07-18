# Projeto de Implantação de um Cluster Kubernetes na AWS

Este projeto tem como objetivo demonstrar como implantar uma aplicação baseada em contêineres usando Kubernetes na AWS. O projeto utiliza um cluster Kubernetes e implanta uma aplicação MediaWiki.

## Descrição do Projeto

O projeto consiste em implantar uma aplicação MediaWiki em um cluster Kubernetes, garantindo alta disponibilidade e escalabilidade. A aplicação MediaWiki é uma plataforma de colaboração e gerenciamento de conteúdo, amplamente utilizada para criar wikis e enciclopédias online.

A infraestrutura é criada na AWS utilizando a seguinte abordagem:

- Provisionamento da infraestrutura do cluster Kubernetes usando o AWS Elastic Kubernetes Service (EKS) através do Terraform.
- Configuração e implantação da aplicação MediaWiki no cluster Kubernetes usando arquivos YAML e o kubectl.

## Requisitos

Antes de começar, certifique-se de ter os seguintes requisitos em seu ambiente de desenvolvimento:

  - Conta na AWS com permissões para criar recursos do EKS.
  - Instalação do Terraform.
  - Instalação do kubectl e configuração para se conectar ao seu cluster.
  - Repositório GIT público ou aberto para armazenar os arquivos de configuração.

## Implantação

Siga os passos abaixo para implantar o cluster Kubernetes e a aplicação MediaWiki na AWS:

### Passo 1: Provisionamento da Infraestrutura do Cluster Kubernetes

 1. Abra o arquivo `terraform/main.tf` e configure as variáveis necessárias, como região da AWS e nome do cluster.
 2. Execute o comando `terraform init` para inicializar o Terraform.
 3. Execute o comando `terraform apply` para criar os recursos do cluster Kubernetes na AWS.
 4. Aguarde até que o Terraform provisione todos os recursos. Isso pode levar alguns minutos.
 5. Anote o endpoint do cluster Kubernetes fornecido pelo Terraform após a conclusão da implantação.

### Passo 2: Implantação da Aplicação MediaWiki no Cluster Kubernetes

 1. Navegue até o diretório kubernetes.
 2. Abra o arquivo `deployment.yaml` e configure as labels de acordo com os requisitos definidos.
 3. Abra o arquivo `service.yaml` e configure o tipo de serviço (LoadBalancer externo ou similar).
 4. Se necessário, ajuste outras configurações nos arquivos YAML de acordo com suas necessidades.
 5. Execute o seguinte comando para implantar a aplicação MediaWiki no cluster Kubernetes:

    ```bash
    kubectl apply -f deployment.yaml
    kubectl apply -f service.yaml
    ```

 6. Aguarde até que os pods e o serviço sejam criados e estejam em execução.
 7. Anote o endereço IP ou o DNS do serviço MediaWiki fornecido pelo Kubernetes.

### Passo 3: Acesso à Aplicação MediaWiki

Após a conclusão da implantação, você pode acessar a aplicação MediaWiki usando o endereço IP ou DNS do serviço MediaWiki anotado anteriormente. Acesse o aplicativo em um navegador da web e siga as instruções para configurar a instância do MediaWiki.

## Considerações Finais

Neste projeto, demonstramos como implantar uma aplicação MediaWiki em um cluster Kubernetes usando a AWS como provedor. O uso do Terraform facilita a criação da infraestrutura necessária e o Kubernetes oferece recursos avançados para orquestração e gerenciamento de contêineres.

## Para mais informações, acesse o repositório Git:

```
https://github.com/karinarv/terraform/blob/main/README.md
```
