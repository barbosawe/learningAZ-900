# LearningAZ-900
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO, referentes a Certificação da Microsoft AZ-900.

<sub> Computação em nuvem: domínio do objetivo </sub> 

# 1. Computação em Nuvem no Azure

No Microsoft Azure, a computação em nuvem é o fornecimento de serviços de TI (máquinas virtuais, bancos de dados, redes, inteligência artificial, armazenamento e muito mais) através da plataforma da Microsoft, com escalabilidade, alta disponibilidade e pagamento sob demanda.

# 2. Modelos de Nuvem no Azure

Nuvem Pública (Azure Public Cloud):
> Serviços hospedados e gerenciados pela Microsoft em seus datacenters globais, acessíveis pela internet.

### Exemplos de produtos:

> Azure Virtual Machines (VMs) – computação sob demanda.
> Azure Blob Storage – armazenamento de objetos.
> Azure App Service – hospedagem de aplicações web.

Nuvem Privada (Azure Stack):
Infraestrutura de nuvem dedicada, implementada no datacenter da própria organização, mas com os mesmos recursos do Azure.

### Exemplos de produtos:

> Azure Stack Hub – nuvem privada no ambiente local.
> Azure Arc – gerenciamento unificado de servidores, VMs e Kubernetes dentro e fora do Azure.

Nuvem Híbrida (Azure Hybrid):
Combinação entre nuvem pública do Azure e infraestrutura local da empresa.

### Exemplos de produtos:

> Azure Arc – para gerenciar workloads híbridos.
> Azure ExpressRoute – conexão privada entre infraestrutura local e Azure.
> Azure Backup e Site Recovery – integração entre on-premises e nuvem.

# 3. Casos de Uso Apropriados para Cada Modelo no Azure
Modelo	Produtos Azure	Casos de Uso
> Nuvem Pública	Azure Virtual Machines, Azure SQL Database, Azure Blob Storage, Azure App Service	Startups e empresas que querem escalar rapidamente; aplicações web; soluções de Big Data; backup em nuvem.

> Nuvem Privada	Azure Stack Hub, Azure Arc:	Organizações que precisam de total controle e conformidade (bancos, hospitais, governo); workloads sensíveis que não podem ir à nuvem pública.

> Nuvem Híbrida	Azure Arc, Azure ExpressRoute, Azure Backup, Azure Site Recovery: Empresas que fazem migração gradual para nuvem; integração de sistemas locais com a nuvem; continuidade de negócios e recuperação de desastres.
