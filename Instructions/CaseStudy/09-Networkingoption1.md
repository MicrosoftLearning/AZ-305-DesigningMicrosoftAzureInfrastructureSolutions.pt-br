
# Criar uma solução de infraestrutura de rede  

## Requisitos

Como a equipe de TI empresarial da Tailwind Traders se prepara para definir a estratégia de migração de algumas das cargas de trabalho da empresa para o Azure, ela deve identificar os componentes de rede necessários e criar uma infraestrutura de rede necessária para dar suporte a eles. Considerando o escopo de suas operações globais, a Tailwind Traders usará várias regiões do Azure para hospedar seus aplicativos. A maioria desses aplicativos tem dependências de serviços de infraestrutura e dados, que também residirão no Azure. Os aplicativos internos migrados para o Azure devem permanecer acessíveis aos usuários do Tailwind Traders. Os aplicativos voltados para a Internet migrados para o Azure devem permanecer acessíveis a qualquer cliente externo. 

Para montar o design de rede inicial, a equipe de TI da Tailwind Traders Enterprise escolheu dois aplicativos principais, que são representativos das categorias mais comuns de cargas de trabalho que devem ser migradas para o Azure.  

### Design - Aplicativo corporativo de catálogo de produtos

![Arquitetura do catálogo de produtos](media/catalog.png)

- Um aplicativo Web baseado no .NET Core de duas camadas voltado para a Internet e baseado no Windows que fornece acesso ao catálogo de produtos, hospedado em um banco de dados do Grupo de Disponibilidade Always On do SQL Server. Este aplicativo é categorizado como de missão crítica, com SLA de disponibilidade de 99,99%, RPO de 10 minutos e RTO de 2 horas. 

-   Os líderes de negócios enfatizam a importância da experiência ideal do cliente ao acessar aplicativos voltados para a Internet, portanto, é fundamental que o tempo necessário para carregar páginas da Web e baixar conteúdo estático seja minimizado. Da mesma forma, uma falha de servidores individuais que hospedam componentes de aplicativos Web e suas dependências deve ter um impacto insignificante na disponibilidade do aplicativo da web percebida pelos clientes. Embora se entenda que uma falha regional pode introduzir alguma interrupção em sessões da web existentes, o failover para um site de recuperação de desastres deve ser automático.

- Para aproveitar os benefícios oferecidos pelos serviços de PaaS do Azure, a equipe de TI corporativa decidiu implementar o banco de dados do aplicativo corporativo do catálogo de produtos usando o Banco de Dados SQL do Azure. 

- As equipes de Risco e Segurança da Informação da Tailwind Traders exigem que toda a comunicação entre VMs do Azure e serviços de PaaS que fazem parte do mesmo aplicativo viajem via backbone do Azure, em vez de por meio de um ponto de extremidade público dos serviços de PaaS. 

## Tarefas - Aplicativo corporativo de catálogo de produtos

1. Crie uma solução de rede de duas camadas para o Catálogo de Produtos. Quando apropriado, seu design pode incluir o Azure Front Door, o WAF, o Firewall do Azure e o Balanceador de Carga do Azure. Seus componentes de rede devem ser agrupados em redes virtuais e os grupos de segurança de rede devem ser considerados. Esteja preparado para explicar por que você escolheu cada componente do design. 

Como você está incorporando os pilares do Well-Architected Framework para produzir uma arquitetura de nuvem eficiente, estável e de alta qualidade?

