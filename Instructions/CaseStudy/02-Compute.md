---
casestudy:
  title: Criar uma solução de computação
  module: Compute solutions
---

# Criar uma solução de computação

## Requisitos

A Tailwind Traders quer migrar seu aplicativo de catálogo de produtos para a nuvem. Este aplicativo tem uma configuração tradicional de 3 camadas usando o SQL Server como o armazenamento de dados. A equipe de TI espera que você possa ajudar a modernizar o aplicativo. Ela forneceu este diagrama e várias áreas que poderiam ser melhoradas. 

![arquitetura de computação](media/compute.png)

* O aplicativo front-end é um aplicativo web baseado em .NET core. Durante os períodos de pico, 1750 clientes visitam o site a cada hora. 

* O aplicativo é executado em servidores web IIS em uma camada front-end. Essa camada lida com todas as solicitações de compra de produtos dos clientes. Durante a última promoção de fim de ano, os servidores front-end atingiram seus limites de desempenho e os carregamentos de página foram longos. A equipe de TI considerou adicionar mais servidores, mas fora do horário de pico os servidores geralmente ficam ociosos.

* A camada intermediária hospeda a lógica de negócios que processa as solicitações do cliente. Essas solicitações geralmente são para suporte técnico. As solicitações de suporte estão na fila e ultimamente os tempos de espera têm sido muito longos. É oferecido e-mail como alternativa à espera por um representante. Mas muitos clientes parecem ficar frustrados e se desconectam em vez de esperar. Há 75-125 solicitações de clients por hora. 

* A camada de back-end usa o banco de dados do SQL Server para armazenar pedidos de clientes. Atualmente, os servidores de banco de dados do back-end estão tendo um bom desempenho.

* Embora a alta disponibilidade seja uma preocupação, devido às exigências legais, a empresa deve manter todos os recursos em uma única região.

## Tarefas

* **Camada de front-end**. Qual serviço de computação do Azure você recomendaria para a camada front-end? Explique por que você escolheu sua solução. 

* **Camada intermediária**. Qual serviço de computação do Azure você recomendaria para a camada intermediária? Explique por que você escolheu sua solução. 

Como você está incorporando os pilares do Well-Architected Framework para produzir uma arquitetura de nuvem eficiente, estável e de alta qualidade?
