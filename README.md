
# aula 24/02/2025

Well-Architected Framework: Um conjunto de boas práticas da AWS para garantir que soluções de software sejam eficientes, seguras e escaláveis. Ele abrange pilares como segurança, confiabilidade e otimização de custos, essenciais para construir arquiteturas de software resilientes.

Excelência operacional: Refere-se à capacidade de monitorar, automatizar e otimizar os processos operacionais para garantir que o sistema seja robusto e fácil de manter a longo prazo.

Segurança: Implica na implementação de controles de segurança para proteger dados e infraestruturas, como criptografia, autenticação e práticas de controle de acesso, fundamentais para garantir que a arquitetura de software esteja protegida.

Confiabilidade (Reliability): Diz respeito à criação de sistemas que sejam redundantes e capazes de se recuperar rapidamente de falhas. No design de software, isso pode ser alcançado com failover, testes de resistência e outras técnicas para evitar interrupções.

Eficiência em performance: Garantir que o software use recursos de maneira eficiente, como o uso de cache, balanceamento de carga e distribuição inteligente de dados, visando otimizar a performance sem desperdiçar recursos.

Otimização de custos: Utilização eficiente dos recursos na nuvem, aplicando estratégias como dimensionamento adequado, automação e escolha correta de serviços para evitar desperdício de recursos e reduzir custos operacionais.

Sustentabilidade: No design de software, implica em criar soluções que minimizem o impacto ambiental, como reduzir o consumo de energia por meio de otimização de processos e uso de tecnologias ecologicamente responsáveis.


# aula 27/02/2025

Trade-Offs: Quando projetamos software, frequentemente há que escolher entre diferentes abordagens (ex: desempenho vs. complexidade). Avaliar trade-offs é crucial para decidir qual solução é mais adequada para os requisitos do sistema.

Escalabilidade/Elasticidade: São conceitos fundamentais no design de sistemas distribuídos, permitindo que o software cresça conforme a demanda. A escalabilidade horizontal, por exemplo, permite adicionar mais instâncias de servidores ou containers.

Automatização auto escalabilidade: O software pode ser projetado para ajustar automaticamente os recursos em função da carga de trabalho, melhorando a eficiência e a utilização de recursos.

Infraestrutura como Código (IaC): Permite que arquiteturas de software e infraestrutura sejam definidas de forma programática, permitindo automação e consistência na criação e gerenciamento de recursos.

Tratar os recursos como descartáveis: No design de software, isso significa que componentes e recursos (como instâncias de servidores) podem ser criados, destruídos e substituídos sem afetar a integridade do sistema, facilitando a manutenção e escalabilidade.

Baixo acoplamento: Arquiteturas de software devem ser projetadas para minimizar dependências entre módulos ou serviços, permitindo maior flexibilidade, facilidade de manutenção e escalabilidade.

Design de serviços e não servidores: No contexto de microserviços, por exemplo, você projeta os serviços de forma independente dos servidores subjacentes, permitindo mais agilidade e flexibilidade.

Escolha o banco de dados correto: A escolha do banco de dados (SQL vs. NoSQL, por exemplo) impacta diretamente o desempenho e a escalabilidade do sistema. Deve ser feito conforme os requisitos específicos do software, como consistência, disponibilidade e performance.




# aula 06/03/2025

Infraestrutura como código (IaC) = Automatizar o provisionamento das máquinas

Tratar recursos como descartavéis (serviço mais estável)

item altamente acoplavel = item com muitos acoplamentos (resposta: clonar DBs e usar o elastic load balancing (duplicar/triplicar para não sobrecarregar um único)  e distribuir as cargas, checagem de sáude) exemplos DNS, Reverse Proxy

Escolher o DB certo, saber quais as necessidades e escolher o DB que melhor se adequa ás necessidades

Arquiteto Frugal = arquiteto que se preocupa com custos

Trade-Offs: A avaliação de trade-offs é essencial no design de arquitetura, especialmente em decisões sobre escalabilidade, disponibilidade e custo, para que o sistema atenda de forma eficiente os requisitos do negócio.

Evitar ponto único de falha: No design de software, isso se traduz em garantir que não haja dependências críticas que possam derrubar todo o sistema, implementando redundâncias e mecanismos de failover.

Otimização de custo: Ao projetar sistemas, a escolha de serviços em nuvem deve ser feita de forma estratégica para minimizar custos, como utilizando serviços gerenciados em vez de manter infraestrutura própria.

Uso de cache: O uso de caches (memória em vez de banco de dados) pode acelerar o acesso aos dados, melhorando significativamente o desempenho de sistemas que fazem muitas leituras.

Proteger sua infraestrutura: A arquitetura de software deve ser projetada com defesas contra ataques e falhas, como o uso de firewalls, criptografia e controle de acesso granular.

Infraestrutura global da AWS: No design de software, isso significa projetar soluções com alta disponibilidade e baixa latência em diversas regiões e zonas de disponibilidade, melhorando a resiliência e o desempenho.

Regiões e Zonas de Disponibilidade: Arquitetura distribuída deve usar múltiplas zonas de disponibilidade para garantir alta disponibilidade e resiliência, evitando que falhas em um local afetem o sistema como um todo.

Local Zones: Implementar Local Zones pode reduzir a latência em sistemas críticos ao disponibilizar recursos mais próximos dos usuários finais, ideal para aplicações sensíveis ao tempo de resposta.

Data Centers: Ao planejar uma arquitetura de software global, a escolha de data centers adequados, próximos aos usuários finais, melhora a performance e a disponibilidade.

# aula 10/03/2025


Região AWS = localização no mundo onde existem equipamentos da AWS

Modelo de responsabilidade compartilhada = nunca é da AWS 100%, (EC2/IaaS = infraestrutura como um serviço - servidor) 

Porta 22 SSH - acesso remoto para máquina 

Permissões = acessos para determinadas funções.

Infraestrutura global da AWS: Usar a rede global da AWS permite criar uma arquitetura de software com baixa latência e alta disponibilidade em diversas regiões.

POPs - Edge Locations: Para aplicações que exigem baixa latência, como streaming de vídeo ou jogos online, as POPs permitem que dados sejam servidos mais próximos ao usuário, melhorando a performance.

Segurança: A segurança deve ser integrada ao design do software desde o início, com controles de acesso, criptografia e monitoramento contínuo.

Modelo de responsabilidade compartilhada: No design de software, isso implica dividir responsabilidades entre a AWS (infraestrutura) e o cliente (aplicação), garantindo que ambas as partes implementem controles de segurança adequados.

Autenticação: A autenticação é crucial no design de sistemas, garantindo que apenas usuários autorizados acessem a aplicação.

Autorização: Após a autenticação, a autorização controla o que os usuários podem acessar, definindo papéis e permissões detalhadas.

Princípio do privilégio mínimo: Garantir que os usuários e serviços só tenham os privilégios necessários para executar suas funções, minimizando os riscos de falhas ou ataques.

Criptografia: A criptografia deve ser aplicada tanto em trânsito (TLS) quanto em repouso (no banco de dados), protegendo dados sensíveis durante todo o ciclo de vida.





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
Modelo de responsabilidade compartilhada: Definir as responsabilidades entre cliente e AWS na segurança.

Modelo de responsabilidade compartilhada: A arquitetura de segurança no design de software depende da colaboração entre o provedor de nuvem (AWS) e o cliente, que deve configurar adequadamente as permissões e a segurança na aplicação.

Princípio do privilégio mínimo: Deve ser implementado em todos os níveis do software, garantindo que cada componente tenha acesso apenas aos recursos e dados necessários.

Autenticação: Fundamental para garantir que a identidade do usuário seja validada antes de permitir o acesso ao sistema.

Autorização: Após a autenticação, a autorização define o que cada usuário pode fazer, sendo crucial para implementar políticas de segurança eficazes.

Identity and Access Management (IAM): O uso adequado do IAM para gerenciar identidades e permissões é essencial para a segurança e governança de software na nuvem.

Usuários: Gerenciar usuários e suas permissões no IAM permite controlar quem pode acessar e manipular os recursos da AWS.

Acesso pela console/acesso programático: O acesso via console é mais comum para administradores, enquanto o acesso programático (via API) é utilizado por sistemas automatizados, sendo importante garantir segurança em ambos os métodos.




# aula 17/03/2025

RBAC 
ROLE BASE ACCESS CONTROL

efeito

ação 

recurso

Policy de Identidade: Políticas IAM associadas a identidades controlam o que um usuário ou grupo pode acessar, sendo essencial no design de software seguro.

Policy de Recurso: Políticas IAM associadas a recursos controlam o acesso a serviços específicos, garantindo que cada componente do sistema tenha os privilégios necessários.

S3: O S3 é frequentemente usado como armazenamento de objetos em arquiteturas de software, e é importante configurar políticas de acesso para controlar quem pode ler e gravar dados nos buckets.



# aula 20/03/2025

Amazon S3 só roda estático



# aula 24/03/2025

LifeCycle
Limite de vida dos arquivos, muitos GB = Muitos custos, é importante apagar arquivos inúteis, ou adicionar validade para arquivos, assim é mais fácil o controle de arquivos inúteis e importantes.

CORS : SUPORT FOR CROSS-ORIGIN RESOURCE SHARING
proteção para compartilhamento 


