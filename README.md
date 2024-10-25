# Resumo-DIO-Azure
## Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO


### Laboratorio 1 - Computação em nuvem

  No primeiro laboratorio foi lecionado as primeiras impressões sobre o portal, apresentando de modo superficial os serviços que usaremos, como Containers, computação, network, Identidade, armazenamento e banco de dados. De modo geral existem varios outras soluções e serviços para está clicando e aprendendo, mas como explicado são nas proximas aulas. Na aula também aprendemos a customizar nossa plataforma na linguaguem e região que estamos localizados. 

  
### Laboratorio 2 - Beneficios da Nuvem

  Iniciando o laboratorio apresentando os tempos de SLA da Azure, mostrando que de acordo com o a assinatura contratada com a Microsoft, você pode ter o tempo de inatividade dos seus serviços de 5,26 minutos por ano e até 99,999% de SLA, mas logicamente esse nivel de disponibilidade tente a ser mais caro. Mas de modo benefico temos nossas aplicações rodando de modo totalmente disponivel, ageis e redundante, entregando ao cliente serviços de qualidade, e assim valor para a empresa. Como exemplo foi mostrado de modo previo as opções de disponibilidade das maquinasa virtuais, por região, zona e local, e os preços dessas opções.


### Laboratorio 3 - Tipos de serviços

  Nesse laboratorio aboardamos os 3 tipos de serviços ofertados ao cliente, Infraestrutura como Serviço (IaaS), Plataforma como Serviço (PaaS) e Software como Serviço (SaaS). Em IaaS foi usado como exemplo o uso de maquina virtual, onde criamos a maquina que será usada, adicionamos a aplicação que será usada e ai sim começamos a utilizar o serviço. Como PaaS é utilizado o banco de dados, onde só escolhemos qual linguagem será usado e região, e ai sim podemos alimentar nosso banco de dados, sem a nescessidade de criar a maquina virtual. Em SaaS você paga somente o software ja pronto e utiliza sem a preocupação de saber em qual SO ou Plataforma a o software está rodando. 


### Laboratorio 4 - Componentes de arquitetura do Azure

  Nesse laboratorio foi mostrado como estão localizados os datacentes da Microsoft Azure, visitando o site [Global Infraestructure](https://azure.microsoft.com/en-us/explore/global-infrastructure/) você vê globalmente as regiões em que presta serviço. Clicando em mais, você consegue ver de forma detalhada os quais serviços aquela região em que está localizado você pode está utilizando, se possui redundacia e para onde é replicado. É possivel entrar virtualemnte nos datacenters e fazer um tour na empresa. Indo para o portal da [Microsoft Azure](https://portal.azure.com/) entramos em assinatura e logo depois em grupo de recursos, logo após criamos um novo grupo de recurso, e selecionamos a região em que esse grupo será criado. Exploramos os serviços dentro do grupo de recursos como IAM, segurança, computação e armazenamento. Por fim, criamos uma rede virtual na região dod Brasil.


### Laboratorio 5 - Computação e redes

  Dentro de maquinas virtuais conhecemos os tipo de maquinas que seria para desempenho ou computação, escolhemos a maquina para computação escolhemos aa ISO que será utilizada. Também pode ser utilizado uma maquina virtual com recursos ja pre configurados com banco de dados, chave SSH, grupo de segurança de rede,  armazenamento. Continuando pede para selecionar a assinatura, logo apos o grupo de recurso, criamos o nome da maquina, e em qual região ela vai ser alocada, selecionamos como vai está disponivel a maquina, se tem redundancia ou não, em mais de 1 zona, selecionamos o numero de instancia, usuario e senha, ou acesso SSH, configuração de autoscale com o limite minimo de 2 instacias e o maximo de 20, a porcentagem de processamento que será utilizado antes de começar a escalar, você pode escolher se vai utilizar o spot ou não
nescessario abrir a porta 443 e a 8080 para ter acesso a maquina, liberada a pora RDP 3389, para acessar a maquina. Escolhemos o armazenamento de disco em SSD e marcamos a opção de excluir o disco com a VM para que na hora de excluir a maquina virtual, o armazenamendo ser excluido junto, pode escolher adcionar um novo disco ou existente. Na parte de rede, configuramos nossa sub-rede para acesso interno, marcamos a opção de excluir o IP e o NIC junto a VM. Configuramos o email para caso a VM desligue o usuario ser avisado, e tambpem podemos agendar o desligamento automatico, configuramos o backup, horario quantidade de backups diarios. A marte de monitoramento configuramos as regras padrão, desabilitamos o diagnostico, podemos instalar um antivirus, mas foi optado não instalar.E por fim é criada a maquina.
  Na criação de pool, fazemos igual a maquina virtual, configuramos o tipo de pool, balanceamento, configuramos a maquina virtual, essa configuração é para pessoal que podem ter uma aplicação muito especifica.
  Em aplicativo de função, damos um nome para a nova função, selecionamos se é codigo ou container, selecionamos a linguagem, versão e região, vamos em configuração de armazenamento


 ### Laboratorio 6 - Dominando o Armazenamento na Azure

   Entrando em criar uma conta de armazenamento, se pode ter Containers de varios tipos, para banco de dados, armazenamento de arquivos estaticos entre varios outros. Primeiramente devemos escolher a assinatura, o grupo de recurso, precisamos criar um nome unico para o nome da conta de armazenamento, escolhemos a região e zona, escolher o tipo de desempenho padrão ou premium. Logo em seguida escolhemos a redundancia como teste deixamos em LRS que é o modo mais simples de redundacia. Em armazenamento de Blobs ele da a opção de quente ou frio, escolhemos quente. Por fim criamos o storage account, dentro dele temos os containeres, compartilhamento de arquivo, tabelas e filas. Criamos um compartilhamento de arquivos, e já podemos conectar e mapear atraves de script, o armazenamento é utilizado via SMB. Em filas Podemos criar mensagens para aplicações. Em Tabelas podemos criar nossas tabelas de banco de dados para serem usados também por aplicações. Em container criamos pequenos armazenamentos para ser usados para as aplicações. Aprendemos também os tipos de migração pra o Azure, para banco de dados, servidores e aplicativos web, somente banco de dados e maquinas virtuais. Criamos um projeto para verificar como funciona o serviço. Verificamos também como é feito as migrações e vemos os preços de cada migração para o azure. Vemos também como usar o azcopy, baixar ele no computador, criamos um container, criamos um token, copiamos o codigo do token, fazemos a sincronização da maquina local com o Azure para usar o azcopy. Feito a a sincronização e envio dos arquivos  está concluido o azcopy. Vemos tambpem o gerenciador de arquivos do azure, onde é feita toda a sincronização pode do Azure em seu computador e assim utilizar para colocar arquivos do seu computador ou baixar.


### Laboratorio 7 - Entendendo sobre segurança e identidade na Azure

  Agora o Active Directory se chama Entra ID, é onde as credenciais são guardadas, e criamos também usuarios, grupos e funções, podemos ver os dispositivos cadastrados com as credenciais, app registrados. Podemos também resetar as senhas dos colaboradores ou eles mesmos podem fazer, se configurado. Para criar funções é nescessario ter uma conta Entra ID premuim P1 ou P2, a diversas regras dentro de Roles e administrators. Podemos também adicionar nossos dominios para ser utilizando como conta. Disponivel também o moitoramento dos nossos serviços. Vimos também somre o microsoft Defender for cloud que monitora as nuvens Azure, AWS e GCP, vemos as recomendações de segurança, ele também tem a função de Devops, onde onde conta de Github ou Gitlab para verificar a segurança. O MDC consegue fazer a verificação de maquinas também e tambpem pode tentar resolver os problemas das contas.

### Laboratorio 8 - Otimizando custos no Azure

  Entramos na calculadora do TCO para verificar o valor gasto dentro da nossa empresa. Na calculadora vamos ver os 3 passos para fazer a migração da nossa aplicação para a nuvem, lá ele pede pra escolher qual servidor vamos usar, quantos vão ser, numero de nucleos, podemos ver se vamos ou não usar banco de dados, qual a liguagem do banco de dados, se vai ser armazenado em HD ou SSD. Depois passamos para ajustar suposições, para ve se tem cobertura de beneficio  do Azure, para trazer economia, podemos ver também quanto gastamos dentro da nossa empresa, e quanto vamos economizar durante a utilização dos serviços do Azure, podemos ver no que mais vamis está gastando entre outros indicativos de valor.
  dentro da Calculadora de custos podemos calcular os valores dos serviços e quais regiões gastamos mais, dentro dele podemos fazer o orçamento dos gastos que fariamos se fosse realizado o projeto dentro da nuvem, dentro da calculadora podemos fazer a simulação de todos os serviços utilizados, como exemplo foi utilizado o orçamento de uma maquina virtual, calculamos o tipo da maquina, quanto tempos estará ligada, o tipo de contratação, e verificamos o quanto vai ser gasto mensalmente. Indo para o cost management + Billing, podemos criar regras para ter uma noçã o do quanto está gastando dentro do Azure, ele pode nos avisar caso o valor de uso estrapole o valor que estamos contratando, ele também nos trás recomendações para diminuir gastos.

### Laboratorio 9 - Governança e Conformidade

  Entramos no [Portal de Confiança do Serviço](https://servicetrust.microsoft.com/) da Azure, onde podemos ver as certificações, regulamentos e padrões utilizados pelo Portal, você precise verificar ou alguma auditoria externa vem fazer a avaliação, a nuvem esteja assegurada, podemos ver os artefados e baixar eles também, de acordo com o paises em que esteja localizado. Agora vamos ver os bloqueios dentro de resource group, podemos bloquear os serviços em todo grupo de recurso. Em microsoft purfiew accounts, criamos uma nova conta e ja podemos utilizar, podemos fazer uma governança dos serviços utilizados, fazer auditorias, catalagos de dados, mapeamento de dados e proteção da informação. Ele ajuda a identificar também pontos fracos e fortes do seu dashboard. Passando para as Policies, podemos criar politicas dentro das assinaturas, contas ou resouce group. Dentro dela ja existem politicas padrões ja sendo utilizadas pelo Azure, ciramos uma nva politica para ser utilizada dentro da assinatura, escolhemos a região, e ja podemos aplicar.

### Laboratorio 10 - Ferramentas de gerenciamento e implantação

 Neste laboratorio, é nos apresentado o shell para que possamos criar serviços por codigo, é um Powershell virtual, então é utilizando os comandos do windows, mas podemos escolher o bash, para usar como linux, os comandos são utilizados com inicial "az", na opção de CLI temos comandos padrões e como utiliza-los dentro do terminal. Dentro de Export Templates, podemos criar um JSON ou uma exportar esse modelos pra criar automações de um jeito mais rapido. Agora sobre o Azure Arc, ele cria e genrencia infraestruturas de serviço como banco de dados grupos de rede ou até um site, alem de gerenciar serviços de fora. 


 
