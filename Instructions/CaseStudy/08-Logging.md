---
casestudy:
  title: Fabrikam Residences
  module: Logging and monitoring solutions
---
# Estudo de caso: Fabrikam Residences

## Requisitos

**Este estudo de caso requer que você tenha concluído os seguintes módulos e estudos de caso: computação, dados relacionais, dados não relacionais, autenticação, arquitetura de aplicativos**

Você assumiu uma nova posição na Fabrikam Residences, que é muito bem-sucedida e está tendo um rápido crescimento. A Fabrikam Residences é uma empreiteira de construção para novas casas e grandes reformas de casas e tornou-se bem-sucedida ao criar edifícios de qualidade e oferecer tecnologias de casa integrada mais novas do que os concorrentes.  

Atualmente, essas tecnologias são fornecidas e gerenciadas por empresas subcontratadas separadas. Os proprietários da Fabrikam Residences querem começar a oferecer essas opções de tecnologia atualizadas internamente para proporcionar melhor qualidade, suporte e dados sobre os padrões e necessidades dos clientes. 
 
Inicialmente, a empresa quer oferecer controle e monitoramento de HVAC (aquecimento e refrigeração), monitoramento e alertas de sistemas de segurança e automação residencial. Isso exigirá um novo site, solução de armazenamento de dados e solução de ingestão de dados.

A empresa teve um tremendo crescimento nos últimos 2 anos. A empresa estima que pode dobrar de tamanho nos próximos 12 a 18 meses. Com um crescimento tão rápido no mercado regional, a empresa não tem planos atuais de expansão para fora do mercado regional.

## Situação Atual

A sede da Fabrikam opera um pequeno datacenter em um único local. O datacenter hospeda o **software de PM (Gerenciamento de Projetos)** da empresa.

![Arquitetura de software de gerenciamento de projetos](media/fabrikam.png)

- O software de PM usa um aplicativo Windows de terceiros. O aplicativo é executado em um cluster NLB (Balanceamento de Carga de Rede) de 2 nós com um único back-end do Microsoft SQL Server.  

- Imagens e documentos são armazenados em uma unidade mapeada do servidor, que reside em um dispositivo NAS dedicado.

- Usuários corporativos, funcionários do escritório, usam um front-end da Web para inserir dados como cronogramas de entrega de suprimentos e pedidos de alteração.

-   Os superintendentes de campo usam laptops e tablets Windows offline para registrar continuamente o progresso da construção e outros detalhes.  Essas alterações, como novas ordens de serviço, são armazenadas em um arquivo de alteração local.  No final de cada dia, os superintendentes retornam ao escritório para se conectar à rede sem fio e executar um pequeno script a fim de carregar o arquivo de alteração em um servidor FTP.  Um segundo script é programado para ser executado todas as noites a fim de processar todos os arquivos de alteração e inserir seu conteúdo no banco de dados de Gerenciamento de Projetos (Microsoft SQL Server).

O **software de Tecnologia Doméstica** é atualmente fornecido e hospedado por terceiros e envolve pelo menos três sites diferentes que o cliente deve visitar.  Propõe-se que o software seja substituído por uma solução desenvolvida internamente e unificada.

![Diagrama do aplicativo HVAC, Segurança e Automação](media/software.png)

## Requisitos 

**Software de Gerenciamento de Projetos**

- Migre o maior número possível de sistemas para um provedor de nuvem pública.

- Substitua os scripts existentes para aproveitar um sistema mais seguro do que o FTP, pois surgiram preocupações de segurança. Além disso, você foi solicitado a certificar-se de que os arquivos de alteração sejam processados assim que forem carregados.

- Aumente a resiliência do banco de dados de gerenciamento de projetos. Embora o desempenho não seja um problema, a empresa gostaria de evitar a perda de acesso ao banco de dados em caso de uma única falha de hardware.

**Nova Solução de Tecnologia Doméstica**

- Adicione uma nova solução para coletar dados continuamente dos sensores de monitoramento domésticos.
  - Banco de dados de algumas leituras de sensores para análise de tendências e relatórios.
  - Forneça alertas configuráveis em tempo real com base nas necessidades do proprietário.
  
- Projete uma solução de banco de dados relacional para manter as preferências e configurações do proprietário.
  - O sistema deve ser escalável.
  - A redundância é fundamental.
  
- O novo site unificado será desenvolvido internamente e hospedado em Linux.  Esse site será usado para visualizar monitores e alterar preferências para itens como limites de temperatura ou alerta. As cargas podem variar muito, e o sistema deve ser capaz de escalar rapidamente.

-   Forneça aos usuários uma maneira de entrar no sistema sem criar outra conta de usuário e senha.

- Implemente controles de segurança e forneça relatórios semanais descrevendo como a empresa se compara às práticas recomendadas padrão do setor.

## Tarefas 

1. Projete uma solução para o software de Gerenciamento de Projetos. Esteja preparado para explicar por que você escolheu cada componente do design e como ele atende aos requisitos da solução.

2. Projete uma arquitetura para a Nova Solução de Tecnologia Doméstica. Esteja preparado para explicar por que você escolheu cada componente do design e como ele atende aos requisitos da solução.

Como você está incorporando os pilares do Well-Architected Framework para produzir uma arquitetura de nuvem eficiente, estável e de alta qualidade?

