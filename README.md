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





![Arquitetura](https://github.com/luizcortezdev/atividade-final-compass-uol/assets/138727208/7f72b9f7-2122-4e5e-973d-c855929da145)



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

### Para o Deploy usando ferramentas de práticas Devops.

![pipeline](https://github.com/luizcortezdev/atividade-final-compass-uol/assets/138727208/7a7f52c2-9f20-42cf-8e26-aede406b27d4)



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
![DMS](https://github.com/luizcortezdev/atividade-final-compass-uol/assets/138727208/94537d1b-33f5-4664-92e6-7911582a5d96)

  
  
## Cronograma e Prazo de entrega.
 - Carga Horaria 8h diárias em dias úteis
 - Equipe de 3 Desenvolvedor
   

| Cronograma das atividades |
| --- |
- ###### Análise do Projeto 
  Estudar o projeto ,pesquisar ferramentas e planejar todo o andamento do trabalho e definir os serviços aws serão usados.
  
- ###### Reunião de alinhamento com equipe
  Participar de reunião online com os colegas discutir e atribuir funções e planejar e compartilhar ideias.
  
- ###### Arquitetura do projeto
    Usar ferramentas visuais para a arquitetura e outras para auxiliar no desempelho do projeto.
  
- ###### Configuração do ambiente
  Implementar os serviços selecionados, criar contas , Banco de dados , habilitar serviços de segurança. Usando as boas práticas de congiguração de ambiante de forma segura para proporcional maior agilidade e otimização de tempo.
  
- ###### Testes
  Nesse periodo são realizados testes ultilitário para garantir ao cliente um serviço seguro livre de falha. 

- ###### Implementação
   Como estágio final da aplicação buscamos atuar de forma coordenada e colaborativa para gerar um produto confiável de integração e implantação contínuas. 

## Previsão para o prazo de entrega. 

| Tempo | Serviço |
| --- | --- |
| 3 Dias/24h | Análise do Projeto |
| 1 Dia/8h | Reunião de alinhamento com equipe |
| 2 Dias/12h | Arquitetura do projeto |
| 5 Dias/ 40h | Configuração do ambiente |
| 2 Dias /12h | Teste |
| 1 Dia/8h | Implementação |


| Tempo | 
| --- |
| 104 horas |
| 13 dias úteis |



## Orçamento 
##### Valores inclui custos dos serviços da aws e tempo de serviço.
Para calcular os serviços da aws usaremos a ferramenta AWS Pricing Calculator que auxilia no planejamento da arquitetura de forma gratuita e ajuda a criar estimativas de custo nos serviços AWS.




