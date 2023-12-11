---
casestudy:
  title: Criar uma solução de armazenamento relacional
  module: Relational storage solutions
---
# Estudo de Caso de Projeto de Armazenamento Relacional

## Requisitos

A Tailwind Traders quer mover seu banco de dados de site público existente para o Azure, já que o front-end do site também está sendo movido para lá.  Inicialmente, o front-end do site só será implantado em 2 regiões para redundância.  No entanto, espera-se que, à medida que o tráfego aumente, o site seja replicado para outras regiões ao redor do mundo. O banco de dados, que você está sendo solicitado a migrar, contém o catálogo de produtos e todos os pedidos on-line.  Atualmente, o banco de dados é executado em um único grupo de disponibilidade do Microsoft SQL Server Always On local.

![Arquitetura de armazenamento não relacional](media/relational%20storage.png)

Principais preocupações da Tailwind Traders:

-   **Alta disponibilidade**.  Uma das principais preocupações da Tailwind Traders é que esse banco de dados esteja altamente disponível, pois ele é fundamental para os negócios.  Qualquer interrupção pode resultar em perda de vendas ou confiança do cliente.

-   **Desempenho do site.**  Embora o desempenho de fazer pedidos seja normalmente satisfatório, navegar ou pesquisar páginas com muitos itens listados é relatado como sendo "lento".

-   **Segurança**.  A Tailwind Traders está muito preocupada com as informações pessoais ou financeiras armazenadas no banco de dados que está sendo exposto.  Além de implementar medidas de segurança adequadas, a equipe de segurança precisa verificar se as práticas recomendadas padrão do setor são implementadas, quando possível.


## Tarefas

1.  Criar a solução de banco de dados. Seu design deve incluir autorização, autenticação, preços, desempenho e alta disponibilidade. 
2.  Faça um diagrama do que você decidir e explique sua solução. 

Como você está incorporando os pilares do Well-Architected Framework para produzir uma arquitetura de nuvem eficiente, estável e de alta qualidade?
