---
casestudy:
  title: Criar uma solução de armazenamento não relacional
  module: Non-relational storage solutions
---
# Estudo de Caso de Armazenamento Não Relacional de Projeto

## Requisitos

A Tailwind Traders quer reduzir os custos de armazenamento, reduzindo o conteúdo duplicado e, sempre que aplicável, migrando-o para a nuvem. Eles gostariam de uma solução que centralize a manutenção e, ao mesmo tempo, forneça acesso mundial para clientes que navegam em arquivos de mídia e literatura de marketing. Além disso, gostariam de abordar o armazenamento de arquivos de dados da empresa. 

![Arquitetura de armazenamento não relacional](media/Nonrelational%20storage.png)

 

* **Arquivos de mídia**. Os arquivos de mídia incluem fotos de produtos e vídeos de recursos que são exibidos no site público da empresa, que é desenvolvido e mantido internamente. Quando um cliente navega para um item, os arquivos de mídia correspondentes são exibidos. Os arquivos de mídia estão em diferentes formatos, mas JPEG e MP4 são os mais comuns. 

* **Literatura de marketing**. A literatura de marketing inclui histórias de clientes, folhetos de vendas, gráficos de dimensionamento e informações ecológicas de fabricação. Os usuários de marketing interno acessam a literatura por meio de uma unidade mapeada em suas estações de trabalho Windows. Os clientes acessam a literatura diretamente do site público da empresa.

* **Documentos corporativos**. São documentos internos de departamentos como recursos humanos e finanças. Esses documentos são acessados e gerenciados por meio de um aplicativo da web desenvolvido internamente. A lei exige que vários documentos sejam retidos por um período de tempo específico. Ocasionalmente, os documentos precisarão ser mantidos por mais tempo quando questões legais ou de RH estiverem sendo investigadas. A maioria dos documentos corporativos com mais de um ano são mantidos apenas por motivos de conformidade e raramente são acessados.

* **Localização do arquivo**. Todos os arquivos são armazenados localmente no datacenter do escritório principal. Existem inúmeros compartilhamentos de arquivos organizados por departamento ou linha de produtos. Os servidores de dados estão com dificuldades para fornecer arquivos para o site. Durante os horários de pico, as páginas do site demoram para serem renderizadas. 

* **Frequência de acesso aos arquivos**. Alguns produtos são mais populares, e esses dados são acessados com mais frequência. No entanto, alguns produtos, como equipamentos de esqui, só são acessados durante sua temporada. Os eventos de vendas geram muito interesse em determinados itens em promoção. 

## Tarefas

1. Projete uma solução de armazenamento para a Tailwind Traders. 

      * Que tipo de dados são representados? 

      * Quais fatores você considerará em seu projeto?

      * Você usará camadas de acesso de blob?

      * Você usará armazenamento imutável?

      * Como o conteúdo será acessado com segurança?

2.  Sua solução deve considerar a mídia, a literatura de marketing e os documentos corporativos. Suas recomendações podem ser diferentes dependendo dos dados. Esteja preparado para discutir suas decisões. 

Como você está incorporando os pilares do Well-Architected Framework para produzir uma arquitetura de nuvem eficiente, estável e de alta qualidade?
