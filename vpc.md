##1. Criar a VPC

Para criar a VPC, siga os passos abaixo:

Acesse a interface do CloudStack.
Vá até Redes > Criar VPC.
Preencha as informações:
Nome: MinhaVPC
CIDR: 10.1.1.0/24
Zona: Selecione a zona desejada
Clique em Criar VPC.


##2. Criar o Tier de Network

Dentro da VPC criada, vá até Tiers > Criar Tier.
Preencha as informações:
Nome: Web-Tier
CIDR: 10.1.1.0/24
Gateway: 10.1.1.1
Máscara de Rede: 255.255.255.0
Clique em Criar.

##3. Configurar o Load Balancer

Após criar as VMs, configure o Load Balancer para distribuir o tráfego:
Vá até Redes > VPC > Load Balancer.
Clique em Criar Load Balancer.
Preencha os detalhes:
Nome: WebLB
Protocolo: HTTP
Porta Pública: 80
Porta Privada: 80
Adicione as duas VMs criadas (APACHE1 e APACHE2) ao balanceador.
Salve e ative a configuração.
