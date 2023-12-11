---
casestudy:
  title: Criar uma solução de arquitetura de aplicativo
  module: App architecture solutions
---
# Criar uma solução de arquitetura de aplicativo

## Requisitos

A Tailwind Traders deseja atualizar seu site para incluir imagens de produtos fornecidos pelo cliente, além das fotos já existentes fornecidas pelo marketing. Ela acredita que ter mais fotos de produtos em uso dará aos clientes em potencial uma sensação melhor de como os clientes anteriores amaram seus produtos depois de comprá-los. Ela tem alguns requisitos, conforme descrito abaixo:

* As imagens carregadas precisarão ser verificadas antes de serem publicadas no site. O Jurídico e o Marketing estão solicitando que, após o carregamento inicial, as imagens sejam verificadas para quaisquer problemas que prejudiquem a empresa ou possam causar problemas legais. Uma API interna já foi desenvolvida e implantada que pode executar a varredura necessária. 

* Com base nos padrões existentes, a Tailwind Traders espera que os carregamentos de imagens aconteçam de forma muito desigual ao longo do dia. Certos períodos podem ter mais carregamentos do que o software de verificação consegue suportar, enquanto outros períodos podem ter muito poucos ou nenhum carregamento.

* Uma vez que uma imagem carregada tenha sido verificada e aprovada pelo sistema, a Tailwind Traders gostaria que o cliente recebesse um e-mail agradecendo por compartilhar sua imagem.

* O custo e o gerenciamento da solução são uma preocupação, especialmente porque a Tailwind Traders não tem certeza de quão popular esse recurso será inicialmente. Minimize os custos e aproveite as soluções sem servidor sempre que possível.

 

![Arquitetura do aplicativo](media/Apparchitecture.png)

 

## Tarefa

Crie uma arquitetura para as imagens do cliente a serem adicionadas ao site da empresa. 

* Em que local as imagens devem ser armazenadas?

* Como você garantirá que todas as imagens sejam verificadas mesmo quando os carregamentos estiverem ultrapassando a verificação?

* Depois que as imagens forem aprovadas e o banco de dados do catálogo for atualizado, como o cliente será notificado? 

Como você está incorporando os pilares do Well-Architected Framework para produzir uma arquitetura de nuvem eficiente, estável e de alta qualidade?

 
