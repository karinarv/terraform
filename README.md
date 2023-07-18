# Projeto de Implantação de um Cluster Kubernetes na AWS

Este projeto tem como objetivo demonstrar como implantar uma aplicação baseada em contêineres usando Kubernetes na AWS. O projeto utiliza um cluster Kubernetes e implanta uma aplicação MediaWiki.

## Descrição do Projeto

O projeto consiste em implantar uma aplicação MediaWiki em um cluster Kubernetes, garantindo alta disponibilidade e escalabilidade. A aplicação MediaWiki é uma plataforma de colaboração e gerenciamento de conteúdo, amplamente utilizada para criar wikis e enciclopédias online.

A infraestrutura é criada na AWS utilizando a seguinte abordagem:

    Provisionamento da infraestrutura do cluster Kubernetes usando o AWS Elastic Kubernetes Service (EKS) através do Terraform.
    Configuração e implantação da aplicação MediaWiki no cluster Kubernetes usando arquivos YAML e o kubectl.

## Requisitos

Antes de começar, certifique-se de ter os seguintes requisitos em seu ambiente de desenvolvimento:

    Conta na AWS com permissões para criar recursos do EKS.
    Instalação do Terraform.
    Instalação do kubectl e configuração para se conectar ao seu cluster.
    Repositório GIT público ou aberto para armazenar os arquivos de configuração.

## Passo a Passo

Siga os passos abaixo para implantar o cluster Kubernetes e a aplicação MediaWiki na AWS:

1. Provisionamento da Infraestrutura do Cluster Kubernetes

    Abra o arquivo terraform/main.tf e configure as variáveis necessárias, como região da AWS e nome do cluster.
    Execute o comando terraform init para inicializar o Terraform.
    Execute o comando terraform apply para criar os recursos do cluster Kubernetes na AWS.
    Aguarde até que o Terraform provisione todos os recursos. Isso pode levar alguns minutos.
    Anote o endpoint do cluster Kubernetes fornecido pelo Terraform após a conclusão da implantação.

2. Implantação da Aplicação MediaWiki no Cluster Kubernetes

    Navegue até o diretório kubernetes.
    Abra o arquivo mediawiki-deployment.yaml e configure as labels de acordo com os requisitos definidos.
    Abra o arquivo mediawiki-service.yaml e configure o tipo de serviço (LoadBalancer externo ou similar).
    Se necessário, ajuste outras configurações nos arquivos YAML de acordo com suas necessidades.
    Execute o seguinte comando para implantar a aplicação MediaWiki no cluster Kubernetes:

    ```bash
    kubectl apply -f deployment.yaml
    kubectl apply -f service.yaml
    ```

    Aguarde até que os pods e o serviço sejam criados e estejam em execução.
    Anote o endereço IP ou o DNS do serviço MediaWiki fornecido pelo Kubernetes.

3. Acesso à Aplicação MediaWiki

Após a conclusão da implantação, você pode acessar a aplicação MediaWiki usando o endereço IP ou DNS do serviço MediaWiki anotado anteriormente. Acesse o aplicativo em um navegador da web e siga as instruções para configurar a instância do MediaWiki.

## Considerações Finais

Neste projeto, demonstramos como implantar uma aplicação MediaWiki em um cluster Kubernetes usando a AWS como provedor. O uso do Terraform facilita a criação da infraestrutura necessária e o Kubernetes oferece recursos avançados para orquestração e gerenciamento de contêineres.

Sinta-se à vontade para explorar e ajustar os arquivos YAML fornecidos de acordo com suas necessidades específicas. Este projeto serve como ponto de partida para implantar aplicativos em contêineres na AWS usando Kubernetes.
