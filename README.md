# Formação AWS Cloud Foundations

Este repositório documenta os conteúdos e práticas desenvolvidas durante a formação **AWS Cloud Foundations**, com foco em compreender os principais conceitos da nuvem AWS, configurar a conta com segurança e aplicar automações simples utilizando o IAM e a AWS CLI.

---

## Conteúdo Programático Detalhado

### Módulo 1: Introdução à AWS e Conceitos Básicos
- **História e evolução da AWS**: de provedora de infraestrutura para líder em serviços de nuvem.
- **Infraestrutura global**:
  - Regiões (Regions) → áreas geográficas que contêm múltiplas zonas.
  - Zonas de Disponibilidade (Availability Zones) → datacenters redundantes dentro de uma região.
  - Edge Locations → pontos de presença para distribuição de conteúdo (CloudFront).
- **Modelo de negócios da AWS**:
  - Pagamento sob demanda (pay-as-you-go).
  - Escalabilidade elástica (scale up/down conforme necessidade).
  - Modelos de responsabilidade compartilhada.

### Configuração da Conta AWS e Práticas de Segurança
- Criação da conta com autenticação multifator (MFA).
- Configuração do usuário root apenas para tarefas críticas.
- Criação de usuários administrativos pelo **IAM**.
- Definição de boas práticas iniciais de segurança.

---

## Conceitos Fundamentais
- Diferença entre **IaaS (Infraestrutura como Serviço)**, **PaaS (Plataforma como Serviço)** e **SaaS (Software como Serviço)**.
- Principais serviços introduzidos:
  - **EC2**: servidores virtuais sob demanda.
  - **S3**: armazenamento de objetos.
  - **RDS**: banco de dados relacional gerenciado.
  - **IAM**: gerenciamento de identidades e permissões.
- Introdução ao **AWS Free Tier** para prática sem custos adicionais.

---

## Módulo 2 Detalhado

### 1. Controle de Gastos e Alertas
- Configuração do **Billing Dashboard** para monitoramento.
- Criação de orçamentos (Budgets) com limites definidos em dólares.
- Definição de alertas por e-mail quando valores ultrapassarem os thresholds configurados.
- Uso prático do **Cost Explorer** para visualizar consumo por serviço.

### 2. IAM - Identity and Access Management
- Criação de **usuários individuais** com credenciais próprias.
- Organização em **grupos** para aplicar políticas em lote.
- Criação de **policies** personalizadas em JSON para regras específicas.
- Implementação do princípio de **menor privilégio**, garantindo que cada usuário só possua permissões necessárias.

### 3. Formas de Acesso à AWS
- **Console AWS**: interface gráfica acessada via navegador.
- **AWS CLI**:
  - Instalação no ambiente local.
  - Configuração via comando:
    ```bash
    aws configure
    ```
  - Teste de conexão:
    ```bash
    aws s3 ls
    ```
- **CloudShell**:
  - Ambiente de terminal pré-configurado diretamente no console AWS.
  - Ideal para comandos rápidos sem instalar nada localmente.

### 4. IAM – Automação com Usuários e Grupos
Automação desenvolvida para acelerar a criação de identidades.

Passos realizados:
1. Instalação do **Git Bash** no Windows para executar scripts.
2. Instalação do **AWS CLI** para interagir com a nuvem via terminal.
3. Configuração de credenciais com `aws configure`.
4. Criação de grupos previamente definidos.
5. Execução do script para criação em massa:
   ```bash
   bash scriptIAM.sh usuarios.csv


Aprendizados e Benefícios:
-Compreensão clara do modelo de responsabilidade compartilhada.
=Capacidade de configurar alertas de custo para evitar gastos inesperados.
=Domínio inicial do IAM para criação e organização de usuários.
=Familiaridade com ferramentas de acesso como CLI e CloudShell.
=Habilidade em automatizar processos de criação de usuários e grupos.
