---
casestudy:
  title: Projetar soluções de autenticação e autorização
  module: Authentication and authorization solutions
---


# Projetar soluções de autenticação e autorização

## Requisitos

A Tailwind Traders está indo muito bem e está expandindo sua força de trabalho. Ela adquiriu um varejista on-line no espaço de vestuário esportivo. A empresa também localizou um parceiro para terceirizar a literatura de marketing. A Tailwind Traders está usando o Azure Active Directory para contas de usuário e grupos. Aqui estão duas iniciativas específicas com as quais o departamento de TI gostaria que você ajudasse. 

**Novas contas de usuário**

  * A aquisição da varejista online adicionará 75 funcionários à Tailwind Traders. Todos os novos usuários têm contas locais do Active Directory Domain Services no domínio existente do varejista.

  * O novo parceiro de marketing terá, inicialmente, 15 funcionários que precisarão de acesso corporativo. Esses funcionários já têm identidades do Microsoft Entra no locatário do Microsoft Entra do parceiro.  

  * Os novos funcionários estão localizados em vários locais geográficos e precisarão de privilégios de conta para suas novas funções de trabalho. Algumas mudanças nas funções de funcionários existentes são esperadas. 

  * O departamento de TI quer aproveitar esta oportunidade para incluir novos recursos de segurança de identidade. 

**Novo acesso ao aplicativo**

  * A equipe de desenvolvimento de negócios tem um aplicativo que executa uma VM do Azure e os dados armazenados em um banco de dados SQL do Azure. Eles precisam permitir que a VM consulte o Banco de dados SQL do Azure com segurança. 
  * Ele também precisa de um servidor local para poder acessar com segurança o banco de dados SQL sem armazenar credenciais no código do aplicativo ou nos arquivos de configuração.

## Tarefas

**Novas contas de usuário**

  * Faça um diagrama do processo para trazer as contas de usuário adquiridas.

  * Faça um diagrama do processo para adicionar as novas contas de parceiro. 

  * Para os requisitos acima, certifique-se de incluir todas as ferramentas que serão usadas. Liste pelo menos três benefícios da solução sugerida. 

* Forneça pelo menos três recomendações para melhorar as soluções de identidade do usuário da Tailwind Traders. Classifique as recomendações em ordem de importância. Inclua suas razões para fazer essas sugestões. 

**Novo acesso ao aplicativo**

  * Forneça uma solução de acesso para o aplicativo de desenvolvimento de negócios.

  * Forneça uma solução de acesso para os recursos locais.

Como você está incorporando os pilares do Well-Architected Framework para produzir uma arquitetura de nuvem eficiente, estável e de alta qualidade?
