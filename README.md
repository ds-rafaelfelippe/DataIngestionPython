![](Imagens/Fundo.png)

# Entendimento do Negócio

Uma fábrica de alimentos planeja implementar um projeto de dados para analisar informações de sensores IoT. 

Localizados em diversas áreas da fábrica, esses sensores enviam informações sobre a temperatura e a umidade específicas de cada zona. A proposta é utilizar esses dados para aprimorar tanto a eficiência quanto a qualidade dos alimentos fabricados, assegurando o cumprimento dos padrões estabelecidos.

Sendo assim, nosso principal objetivo é garantir que os dados estejam acessíveis à equipe de Analytics, possibilitando a realização das análises necessárias.

# Ciclo de Vida dos Dados

Os dados provenientes dos sensores IoT são disponibilizados todas as manhãs no formato JSON e armazenados em uma pasta no servidor local. Nesse arquivo temos informações sobre o código ID do sensor, o horário preciso da coleta e a medição correspondente (temperatura ou umidade).

Além disso, a fábrica disponibiliza algumas tabelas de metadados que são mantidas em um banco de dados relacional. Essas tabelas contém dados sobre os tipos de sensores e os locais onde estão instalados.

# Ferramentas Utilizadas

![](Imagens/ferramentas.JPG)

# Arquitetura da Solução

![](Imagens/arquitetura.JPG)

Cada manhã, os sensores IoT geram um arquivo JSON, o qual é prontamente disponibilizado em uma pasta de um servidor local. O propósito central do script Python é efetuar o carregamento desse arquivo em sua forma bruta no MongoDB. Em seguida, são executadas as transformações necessárias nos dados, culminando na disponibilização estruturada dessas informações em uma tabela no SQL Server.

Os metadados são armazenados em tabelas específicas no SQL Server, sendo a finalidade principal a exposição dessa estrutura para a equipe de Analytics. Dessa maneira, possibilita-se a realização das análises necessárias com eficácia e precisão.

# Modelagem dos Dados

![](Imagens/modelagem.JPG)





