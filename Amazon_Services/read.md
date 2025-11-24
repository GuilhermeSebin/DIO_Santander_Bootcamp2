## Pontos de Presença (Edge Locations/Locais de borda)
Pontos específicos no globo para distribuir conteúdo de forma rápida.
Realiza armazenamento de dados de acordo com a proximidade dos servidores principais.
Exemplo dado: Acesso ao serviço na China por um usuário no Brasil. O primeiro acesso será na China, mas acessos posteriores serão transferidos para outra localidade mais próxima. Permite armazenar cache de dados para acessos futuros em relação à proximidade do servidor.
**Amazon CloudFront**
Serviço de entrega de conteúdo: CDN.
Melhora performance do serviço.
**Route 53**
Serviço de DNS que redireciona corretamente as requisições de acesso.

### Provisionamento de Recursos AWS 

## Elastic Compute Cloud (EC2)
Serviço de computação na AWS. 
Cita construção de data center próprio e seus altos custos, bem como questões futuras sobre: investimento excessivo e processamento desperdiçado / negócio cresceu e é necessário investir mais na estrutura física.

Oferece economia de recurso, escalabilidade, elasticidade e disponibilidade.

## Elastic Compute Cloud (EC2) - Auto Scaling
Serviço que oferece acesso ao serviço com mais de uma zona de disponibilidade com tolerância à falhas.

- Provê escalabilidade horizontal para os serviços
- Melhora tolerância a falhas com identificação de instâncias indisponíveis e implantação multi-AZ (Availability zones)
- Melhor gerenciamento de custos

Scaling Preditivo: conhecer bem o serviço para saber os períodos com picos de acesso

Scaling Dinâmico: basea-se em uma métrica analisada para fazer o scaling de instâncias

## ELB (Elastic Load Balance)
coordena as requisições de forma a dividir a carga de requisição para as instâncias de processamento.

## Serviço Mensageria
- SQS (simple queue service)
segue uma ordem de fila entre requisições de microsservices

- SNS (simple notification service)
sistema pub/sub
utiliza tópicos como estrutura
usuário publica mensagens no tópico e assinantes escutam

## Computação sem servidor (Servless)
código é executado em servidores sem que precise provisionar ou gerenciar o servidor
capacidade automaticamente ajustada pelo serviço




## _Redes AWS_
#### Amazon VPC (Virtual Private Cloud)
Permite construir e configurar redes virtuais
Sub-redes:
- privadas (fazem conexão com outras instâncias, sem conexão com internet) 
- públicas (permitem fazer conexão global)

**Gateway da Internet**
Permite realizar conexões com a internet.
Para conexões com as redes VPC, o utiliza-se, junto com o Gateway, um VPN.

![[Pasted image 20251124094041.png]]

**AWS Direct Connect**
![[Pasted image 20251124094121.png]]
Permite uma conexão dedicada entre a nuvem AWS e servidores privados.
Necessita da disponibilidade entre provedores de internet parceiros dos serviços AWS

#### Sub-redes e listas de controle de acesso
**Network ACLs**
Realizam o controle de acesso às sub-redes e tráfego de entrada e saída de sub-redes.
Possui comportamento Stateless (não mantém estados/tem regras para entrada e saída de dados).
Por padrão, permite todo tráfego de entrada e saída. Deve ser configurada antes de utilizar toda a rede.

**Grupos de Segurança**
Permite a criação de grupos para aumentar a segurança de instâncias do Amazon EC2.
Realizam controle de tráfego de dados (entrada e saída)
Tem comportamento Stateful (mantém estado de máquina)
Por padrão, nega todo o tráfego de entrada e permite todo o tráfego de saída.


### Armazenamento e Banco de Dados
##### Tipos de Armazenamento
- **Object Storage**
	dados como objetos (arquivos e metadados)
	não estruturados
	casos de uso: data lakes, mídias, backup e recuperação
- **File Storage**
	sistemas de arquivos compartilhados
	permite acesso por meio de servidores, aplicações e usuários
	analogia com pastas compartilhadas em uma rede
	casos de uso: ferramentas de desenvolvimento, diretórios pessoais
- **Block Storage**
	HDD, SSD
	dispositivos com diferentes configurações de leitura e escrita
	casos de uso: VMs, contêiners, banco de dados


### Amazon Elastic Block Store - EBS
Volume físico dedicado à instâncias EC2 para manter dados de forma segura e definitiva, sem chance de perder os dados.
- permite definir o tipo de volume
- tamanho e configurações
- anexar o volume à instância EC2

**Volume Instance Store**
Conceito aplicado à virtualização de computação em rede. Instâncias de computação utilizam discos físicos anexados ao computador host e são ideais para dados de armazenamento temporário (buffers, cache, dados de rascunho)
Dados são perdidos se houver: 
	falha no disco
	interrupção ou desligamento da instância

**Backups**
Snapshots (imagem da instância no momento do processo)
Backup Incremental
	- permite realizar backup de dados que foram alterados ou inseridos.
	- economiza espaço ao fazer backup apenas dos dados alterados, e não total do sistema.
	- referencia os backups com imagens "antigas", permitindo recuperar instâncias completas de acordo com a passagem temporal.

### Amazon S3 (Simple Storage Service)
Objeto no S3: um dado que pode ser de qualquer tipo (dados, metadados e chave)


