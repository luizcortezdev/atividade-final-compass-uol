# Atividade - DevSecOps - Projeto final Aws

### Desenvolvido por:
- Amanda Campos
- Luiz Fernando de Oliveira Cortez
- Vinicius da Costa Soares

#### Desafio
###### Construção da arquitetura usando as prática Devops e recursos da AWS.

CASE:
Nós somos da empresa "Fast Engineering
S/A" e gostaríamos de uma solução dos
senhores(as), que fazem parte da empresa
terceira "TI SOLUÇÕES INCRÍVEIS".
Nosso eCommerce está crescendo e a solução
atual não está atendendo mais a alta demanda
de acessos e compras que estamos tendo.
Desde o Início do ano os acessos e compras
estão crescendo 20% a cada mês.
</br>
Atualmente usamos:
* 01 servidor para Banco de Dados Mysql;
* 01 servidor para a aplicação utilizando REACT;
* 01 servidor de web Server e que armazena
estáticos como fotos e links.
</br>
O que é requerido na atividade:
  </br>
  
- Ambiente Kubernetes;
  
- Banco de dados PaaS;
  
- MultiAZ;
  
- Segurança de backup de dados;
  
- Persistência dos dados;
  
- Balanceamento de carga com healthcheck;
  
- necessário/mínimo acesso possível).



## Proposta da empresa 
A nossa arquitetura busca resolver os problemas atuais e otimizar os serviços do nosso cliente
entregando produtos com maior disponibilidade e escabilidade conforme a demanda da empresa.

## Arquitetura do projeto proposto.





![Arquitetura](https://github.com/luizcortezdev/atividade-final-compass-uol/blob/main/diagrama.svg)



#### Serviços AWS utilizados na projeto:
- 4 instancias ec2 - t3.medium
  
- Amazon Route
   O Amazon Route 53 é um serviço da Web de Sistema de Nomes de Domínio (DNS) altamente disponível e escalável.
   O Route 53 conecta as requisições do usuário a aplicações da Internet executadas na AWS ou on-premises.

- Elastic Load Balancing
   O Elastic Load Balancing (ELB) distribui automaticamente o tráfego de aplicações de entrada entre vários destinos e dispositivos virtuais
   em uma ou mais Zonas de disponibilidade (AZs).
 
- Amazon CloudFront
   O Amazon CloudFront é um serviço de rede de entrega de conteúdo (CDN) criado para alta performance, segurança e conveniência do desenvolvedor.
  
 
- Amazon S3
   O Amazon Simple Storage Service (Amazon S3) é um serviço de armazenamento de objetos que oferece escalabilidade, disponibilidade de dados, segurança e performance líderes do setor. Clientes de todos os portes e setores podem armazenar e proteger qualquer quantidade de dados
  de praticamente qualquer caso de uso, como data lakes, aplicações nativas da nuvem e aplicações móveis.
  
  
- Amazon RDS multi az - maquina db.m6gd.large com 8gb de ram
   O Amazon Relational Database Service (Amazon RDS) é uma coleção de serviços gerenciados que facilita a configuração, a operação e a escalabilidade de bancos de dados na nuvem.

- Autoscaling
   Auto Scaling ajuda a garantir que você tenha o número correto de instâncias do Amazon EC2 disponíveis para lidar com a carga da sua aplicação.
  
- EKS - para cluster kubernetes
   O Amazon Elastic Kubernetes Service (Amazon EKS) é um serviço gerenciado que elimina a necessidade de instalar, operar e manter o seu próprio ambiente de gerenciamento do Kubernetes na Amazon Web Services (AWS).
  
- Natgateway
    
- CloudWatch
  Usado para monitorar o autoscaling para verificar se o seu sistema está funcionando conforme o esperado.
  
- CloudFormation
   O Amazon EC2 Auto Scaling é integrado ao AWS CloudFormation, um serviço que ajuda você a modelar e configurar seus recursos da AWS para que você possa gastar menos tempo criando e gerenciando seus recursos e infraestrutura.
  
### Segurança
##### AWS Identity and Access Management (IAM)
Para segurança da conta as medidas de segurança oferecida pela IAM são: autenticação multifator (MFA) com cada conta,Configure o registro de atividades do usuário e da API com o AWS CloudTrail.Tambem Pode ser usado serviços de segurança gerenciados avançados, como o Amazon Macie, que auxilia na descoberta e na proteção de dados confidenciais armazenados no Amazon S3.
##### AWS WAF firewall
O AWS WAF ajuda você a se proteger contra explorações comuns da Web e bots que podem afetar a disponibilidade, comprometer a segurança ou consumir recursos excessivos.
### Segurança no Backup de dados
O Amazon RDS cria e salva backups automáticos da instância de banco de dados ou do cluster de banco de dados multi-AZ durante a janela de backup da instância de banco de dados. O RDS cria um snapshot do volume de armazenamento da instância de banco de dados, fazendo o backup de toda a instância de banco de dados e não apenas dos bancos de dados individuais. O RDS salva os backups automatizados da instância de banco de dados de acordo com o período de retenção de backup especificado. Se necessário, você poderá recuperar a instância de banco de dados para qualquer ponto no tempo durante o período de retenção de backup.



### Para o Deploy usando ferramentas de práticas Devops.

![pipeline](https://github.com/luizcortezdev/atividade-final-compass-uol/blob/main/pipeline.svg)



Usando recursos disponivel da aws
- CodeCommit
   O AWS CodeCommit é um serviço de controle de código-fonte totalmente gerenciado, seguro e altamente escalável que hospeda repositórios privados do Git.
  
- CodePipeline
  O AWS CodePipeline é um serviço totalmente gerenciado de entrega contínua que ajuda a automatizar pipelines de lançamento para oferecer atualizações rápidas e confiáveis de aplicações e infraestruturas.
  
- CodeBuild
  O AWS CodeBuild é um serviço de integração contínua totalmente gerenciado que compila código-fonte, executa testes e produz pacotes de software prontos para implantação.

- ECR - Para repositorios de imagens Docker AWS
  O Amazon ECR também oferece suporte à criação e ao envio de listas de manifestos do Docker, que são usadas para imagens de multiarquitetura.

### Para migração de dados
O AWS Database Migration Service (AWS DMS) é um serviço de replicação e migração gerenciado que ajuda a mover
workloads analíticos e bancos de dados para a AWS rapidamente, de forma segura e com o mínimo possível de inatividade e zero perda de dados.

#### AWS DMS
![DMS](https://github.com/luizcortezdev/atividade-final-compass-uol/blob/main/dms.svg)

  
  
## Cronograma 

## Prazo de entrega



## Valores
![Captura de tela de 2024-02-07 19-33-27](https://github.com/luizcortezdev/atividade-final-compass-uol/assets/138727208/a7e0a527-1e70-47bc-9708-5826f7c34643)



##### Valores inclui custos dos serviços da aws e tempo de serviço.
Para calcular os serviços da aws usaremos a ferramenta AWS Pricing Calculator que auxilia no planejamento da arquitetura de forma gratuita e ajuda a criar estimativas de custo nos serviços AWS.




