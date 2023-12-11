---
casestudy:
  title: Projete uma solução de rede - Aplicativo corporativo de BI
  module: Network infrastructure solutions
---
# Criar uma solução de infraestrutura de rede  

## Requisitos

Como a equipe de TI empresarial da Tailwind Traders se prepara para definir a estratégia de migração de algumas das cargas de trabalho da empresa para o Azure, ela deve identificar os componentes de rede necessários e criar uma infraestrutura de rede necessária para dar suporte a eles. Considerando o escopo de suas operações globais, a Tailwind Traders usará várias regiões do Azure para hospedar seus aplicativos. A maioria desses aplicativos tem dependências de serviços de infraestrutura e dados, que também residirão no Azure. Os aplicativos internos migrados para o Azure devem permanecer acessíveis aos usuários do Tailwind Traders. Os aplicativos voltados para a Internet migrados para o Azure devem permanecer acessíveis a qualquer cliente externo. 

Para montar o design de rede inicial, a equipe de TI da Tailwind Traders Enterprise escolheu dois aplicativos principais, que são representativos das categorias mais comuns de cargas de trabalho que devem ser migradas para o Azure.  

## Design - Aplicativo corporativo de BI 

![Arquitetura do aplicativo corporativo de BI](media/compute.png)

-   Um aplicativo corporativo de BI (business intelligence) interno, baseado no Windows, de três camadas, com a camada front-end executando servidores Web IIS, a camada intermediária hospedando a lógica de negócios baseada no .NET Framework e a camada back-end implementada como um banco de dados do Grupo de Disponibilidade Always On do SQL Server. 

-   Este aplicativo é categorizado como de missão crítica e requer provisões de alta disponibilidade com SLA de disponibilidade de 99,99% e provisões de recuperação de desastres, com RPO de 10 minutos e RTO de 2 horas.

-   Para fornecer conectividade aos aplicativos internos migrados para o Azure, a Tailwind Traders precisará estabelecer conectividade híbrida a partir de seus datacenters locais. O grupo de TI empresarial já estabeleceu que essa conectividade será implementada usando o circuito ExpressRoute de seu datacenter principal de Seattle, no entanto, neste momento ainda não está claro o que seria solução de failover caso esse circuito fique indisponível. O CFO da Tailwind Traders quer evitar pagar por outro circuito redundante ExpressRoute. 

- Há considerações adicionais que se aplicam à conectividade local com aplicativos internos migrados para o Azure. Como o ambiente do Azure da Tailwind Traders consistirá em várias assinaturas e, efetivamente, várias redes virtuais, para minimizar os custos, é importante minimizar o número de recursos do Azure necessários para implementar os principais recursos de rede. Esses recursos incluem conectividade híbrida para pontos locais, bem como filtragem de tráfego. Aliás, essa necessidade de minimizar o custo está alinhada com os requisitos de Risco e Segurança da Informação, que afirmam que todo o tráfego entre pontos locais e redes virtuais do Azure deve fluir por meio de uma única rede virtual, que hospedará componentes responsáveis pela conectividade híbrida e filtragem de tráfego. 

-   De acordo com os requisitos definidos pelas equipes de Risco e Segurança da Informação da Tailwind Traders, toda a comunicação entre VMs do Azure em camadas diferentes que fazem parte do mesmo aplicativo deve permitir apenas as portas necessárias para executar e manter o aplicativo. No entanto, devido a limitações de espaço de endereço IP, talvez não seja possível alocar sub-redes dedicadas para cada camada. O grupo de TI corporativo precisa identificar a maneira ideal de configurar a origem e o destino para a filtragem de tráfego que não exigiria a referência direta a endereços IP ou intervalos de endereços IP.


## Tarefas - Aplicativo corporativo de BI 

1. Projete uma solução de rede de 3 camadas para o Aplicativo de BI. Seu design pode incluir Azure ExpressRoute, Gateways VPN, Gateways de Aplicativo, Firewall do Azure e Balanceadores de Carga do Azure. Seus componentes de rede devem ser agrupados em redes virtuais e os grupos de segurança de rede devem ser considerados. Esteja preparado para explicar por que você escolheu cada componente da solução. 

2. Com base em sua solução de arquitetura do estudo de caso de computação, como isso afetaria o projeto de rede? Você precisaria de algum recurso de rede adicional para proteger o acesso ao aplicativo modernizado? Você não precisaria mais de algumas das soluções recomendadas implementadas em seu projeto de rede original? 

3. Com base em seu estudo de caso de armazenamento (relacional), como você atualizaria o design da rede para proteger o acesso à conta de armazenamento e garantir que apenas usuários selecionados tenham acesso à conta de armazenamento?

4. Com base na modernização do back-end do SQL, como você planeja habilitar o acesso pragmático ao banco de dados para que o front-end não tenha segredos codificados em sua base de código?

Como você está incorporando os pilares do Well-Architected Framework para produzir uma arquitetura de nuvem eficiente, estável e de alta qualidade?
