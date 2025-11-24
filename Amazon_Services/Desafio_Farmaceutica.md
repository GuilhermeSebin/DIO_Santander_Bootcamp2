# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

Data: **[25/11/2025]**
Empresa: **Abstergo Industries**
Responsável: **Guilherme Sebin**

## Introdução
Este relatório apresenta o processo de implementação de ferramentas na empresa **Abstergo Industries**, realizado por **Guilherme Sebin**. O objetivo do projeto foi elencar 3 serviços AWS, com a finalidade de realizar **diminuição de custos imediatos** através da otimização de infraestrutura, armazenamento e licenciamento.

## Descrição do Projeto
O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos específicos. A seguir, serão descritas as etapas do projeto:

### Etapa 1: Otimização de Infraestrutura e Licenciamento
- **Nome da ferramenta:** **Amazon EC2 (Elastic Compute Cloud) com Instâncias Spot**
- **Foco da ferramenta:** Redução de custos de computação para cargas de trabalho tolerantes a interrupção.
- **Descrição de caso de uso:** A empresa farmacêutica possui cargas de trabalho de **análise de dados em lotes (batch processing)**, como simulações de docking molecular, análise de sequenciamento genético ou processamento de grandes conjuntos de dados de ensaios clínicos. Essas cargas de trabalho podem ser executadas em **Instâncias Spot do EC2**, que oferecem descontos de até 90% em relação às instâncias On-Demand. Isso elimina a necessidade de comprar e manter servidores físicos dedicados para picos de processamento, gerando economia imediata no *capex* (capital expenditure) e *opex* (operational expenditure).

### Etapa 2: Armazenamento e Backups Eficientes
- **Nome da ferramenta:** **Amazon S3 Glacier**
- **Foco da ferramenta:** Armazenamento de baixo custo para dados de longo prazo e conformidade regulatória.
- **Descrição de caso de uso:** O setor farmacêutico é altamente regulamentado e exige o armazenamento de dados de ensaios clínicos, relatórios de conformidade (FDA, ANVISA) e logs de auditoria por longos períodos (às vezes, décadas). Ao invés de usar armazenamento local caro ou discos rígidos de backup, os dados de **arquivamento e retenção de longo prazo**, que são acessados raramente, são migrados para o **S3 Glacier**. Isso reduz drasticamente os custos de armazenamento *per gigabyte*, pois o Glacier é otimizado para dados "frios" (acesso infrequente), liberando espaço e reduzindo a manutenção de sistemas de armazenamento primário.

### Etapa 3: Eliminação de Custos de Servidores de Gerenciamento e Software
- **Nome da ferramenta:** **Amazon Simple Email Service (SES)**
- **Foco da ferramenta:** Substituição de servidores de e-mail local (SMTP) e redução de custos de licenciamento.
- **Descrição de caso de uso:** A empresa precisa enviar grandes volumes de e-mails transacionais (ex: notificações de progresso de lotes de produção, alertas de monitoramento de equipamentos, envio de relatórios automatizados de *compliance*). Usar e-mails de servidores *on-premises* requer licenciamento de software, hardware, e manutenção de reputação de IP (para evitar ser classificado como spam). O **Amazon SES** é um serviço *pay-as-you-go* (pague pelo uso), que oferece uma solução de envio de e-mail altamente escalável e de baixo custo, eliminando imediatamente os custos fixos associados a servidores de correio internos.

---

## Conclusão
A implementação de ferramentas na empresa **Abstergo Industries** tem como esperado **reduzir os custos operacionais de TI, especialmente em computação, armazenamento de longo prazo e envio de e-mail, e aumentar a agilidade na realização de análises de dados**, o que aumentará a eficiência e a produtividade da empresa. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam melhorar ainda mais os processos da empresa, como a adoção de **AWS Lambda** para processamento *serverless* (sem servidor) e o uso de **AWS Organizations** para gerenciamento centralizado de custos.

## Anexos

* [Plano de Migração de Cargas de Trabalho Batch para EC2 Spot]
* [Matriz de Retenção de Dados e Classes de Armazenamento S3/Glacier]
* [Documento de Configuração e Políticas de Envio do Amazon SES]
* [Planilha de Comparativo de Custos: Infraestrutura On-Premises vs. AWS Estimado]

---
Assinatura do Responsável pelo Projeto:

Guilherme Sebin

---
