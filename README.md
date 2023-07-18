## Terraform - Trabalho Fiap:

### Requisitos:

Nesta abordagem o projeto deverá ser baseado na execução em Kubernetes, escolha um cluster de containers e desenvolva a arquitetura necessária para a entrega considerando apenas os seguintes recursos:
  - Deployment;
  - Exposição de recursos com um resource do tipo Service para garantir disponibilidade, em formato de LoadBalancer externo ou similar;

Todos os recursos entregues devem possuir duas labels na estrutura:
  - RM = <NUMERO DO RM DO ALUNO>
  - TURMA = 1SEGR
        
Utilize boas práticas na construção do Deployment como uso de tags nas imagens (existem imagens oficiais do projeto midiawiki e probes na estrutura, consulte a documentação: 
  - https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/

Todo o projeto deverá ser disponibilizado como IAC (ou seja, com a relação de YAMLS usados) em um repositório GIT, não será preciso providenciar a camada de persistência em banco de dados, o repositório deve ser público ou aberto ao usuário
  - https://github.com/helcorin



