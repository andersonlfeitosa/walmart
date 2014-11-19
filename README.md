walmart
=======

[![Build Status](https://travis-ci.org/andersonlf/walmart.svg?branch=master)](https://travis-ci.org/andersonlf/walmart)


Problema
--------

**Entregando Mercadorias**

O Walmart esta desenvolvendo um novo sistema de logistica e sua ajuda é muito importante neste momento. Sua tarefa será desenvolver o novo sistema de entregas visando sempre o menor custo. Para popular sua base de dados o sistema precisa expor um Webservices que aceite o formato de malha logística (exemplo abaixo), nesta mesma requisição o requisitante deverá informar um nome para este mapa. É importante que os mapas sejam persistidos para evitar que a cada novo deploy todas as informações desapareçam. O formato de malha logística é bastante simples, cada linha mostra uma rota: ponto de origem, ponto de destino e distância entre os pontos em quilômetros.

<pre>
A B 10
B D 15
A C 20
C D 30
B E 50
D E 30
</pre>

Com os mapas carregados o requisitante irá procurar o menor valor de entrega e seu caminho, para isso ele passará o nome do ponto de origem, nome do ponto de destino, autonomia do caminhão (km/l) e o valor do litro do combustivel, agora sua tarefa é criar este Webservices. Um exemplo de entrada seria, origem A, destino D, autonomia 10, valor do litro 2,50; a resposta seria a rota A B D com custo de 6,25.

Voce está livre para definir a melhor arquitetura e tecnologias para solucionar este desafio, mas não se esqueça de contar sua motivação no arquivo README que deve acompanhar sua solução, junto com os detalhes de como executar seu programa. Documentação e testes serão avaliados também =) Lembre-se de que iremos executar seu código com malhas beeemm mais complexas, por isso é importante pensar em requisitos não funcionais também!!

Também gostariamos de acompanhar o desenvolvimento da sua aplicação através do código fonte. Por isso, solicitamos a criação de um repositório que seja compartilhado com a gente. Para o desenvolvimento desse sistema, nós solicitamos que você utilize a sua (ou as suas) linguagem de programação principal. Pode ser Java, JavaScript ou Ruby.


Solução
-------

**Arquitetura**

Aplicativo JEE 7.


**Softwares necessários**

  * Oracle JDK 8
  * Wildfly 8.1.0.Final
  * Apache Maven 3.2.3
  * H2 Database


**Instalação**

  1. Acesse http://download.jboss.org/wildfly/8.1.0.Final/wildfly-8.1.0.Final.zip e realize o download do servidor de aplicação Wildfly 8.1.0.Final
  1. Descompacte o arquivo baixado na raiz do diretório home do usuário. A partir de agora esse diretório será chamado JBOSS_HOME.
  1. 


**Execução**

Como executar.


**TODO**

  1. Criar script DDL de banco de dados
  1. Explicar a arquitetura
  1. Tutorial sobre como instalar:
    * como configurar o banco
    * como criar datasource
    * como implantar o artefato
  1. Tutorial sobre como executar: 
    * informando os links dos web services
    * informando os parametros
  1. Escrever premissas e suposições
  1. Criar teste unitários para os webservices
  

**Concluídos**
  1. Criar DAO
  1. Alterar o algoritmo de dijkstra
  1. Tratar exceção quando uma malha já estiver incluída
  1. Tratar exceção quando não existir malha cadastrada
  1. Melhorar javadoc
  