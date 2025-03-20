## aula 06/03/2025

Infraestrutura como código (IaC) = Automatizar o provisionamento das máquinas

Tratar recursos como descartavéis (serviço mais estável)

item altamente acoplavel = item com muitos acoplamentos (resposta: clonar DBs e usar o elastic load balancing (duplicar/triplicar para não sobrecarregar um único)  e distribuir as cargas, checagem de sáude) exemplos DNS, Reverse Proxy

Escolher o DB certo, saber quais as necessidades e escolher o DB que melhor se adequa ás necessidades

Arquiteto Frugal = arquiteto que se preocupa com custos

# aula 10/03/2025


Região AWS = localização no mundo onde existem equipamentos da AWS

Modelo de responsabilidade compartilhada = nunca é da AWS 100%, (EC2/IaaS = infraestrutura como um serviço - servidor) 

Porta 22 SSH - acesso remoto para máquina 

Permissões = acessos para determinadas funções.

# aula 13/03/2025

modelo de responsabilidade compartilhada = nuvem responsabilidade do cliente / hardware reponsabilidade da aws

princípio do privilégio minímo = apenas o que o usúario precisa para fazer suas funções, nem mais nem menos

autenticação = provar que é você mesmo

autorização 

identity and access management

usuários

acesso pelo console / acesso programático

MFA (MULTIFACTOR AUTHENTICATION)

CREDENCIAIS TEMPORÁRIAS / COM VALIDADE

gRUPOS SÓ POSSUEM USERS E PERMISSÕES / COLOCAR UM USUÁRIO NO GRUPO DISPONIBILIZA AS PERMISSÕES DO GRUPO PARA O USUÁRIO

ROLES (FUNÇÃO PAPEL)= EXEMPLO (PERMISSÕES DE COZINHA , PERDE AS PERMISSÕES E GANHA PERMISSÕES DE CAIXA TEMPORARIAMENTE) KEYS TEMPORÁRIAS AO ASSUMIR UMA FUNÇÃO NOVA, AO ASSUMIR NOVAMENTE ESSA POSIÇÃO, GANHA KEYS NOVAS QUE TAMBÉM SÃO TEMPORÁRIAS 

# aula 17/03/2025

RBAC 
ROLE BASE ACCESS CONTROL

efeito

ação 

recurso

# aula 20/03/2025

Amazon S3 só roda estático


