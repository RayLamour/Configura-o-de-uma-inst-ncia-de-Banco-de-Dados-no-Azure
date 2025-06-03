# Azure na Prática: Configuração de Instância de Banco de Dados

Este repositório foi criado como parte de um desafio prático com foco na **configuração de uma instância de banco de dados** utilizando a plataforma **Microsoft Azure**. O conteúdo aqui registrado inclui **resumos, anotações, dicas práticas e explicações passo a passo**, com o objetivo de servir como material de apoio para estudos e futuras implementações em ambientes de nuvem.

---

## Objetivos

- Explorar a criação de bancos de dados gerenciados na Azure.
- Entender as opções de configuração e segurança oferecidas.
- Aprender como se conectar à instância de forma segura.
- Registrar boas práticas e pontos de atenção para novos projetos.

---

##  Etapas Detalhadas do Processo

### 1. Acesso ao Portal Azure
- Acesse: [https://portal.azure.com](https://portal.azure.com)
- Faça login com sua conta Microsoft (use uma conta com acesso gratuito ou de estudante, se aplicável).

### 2. Criando um Banco de Dados
1. No menu lateral, clique em **"Criar um recurso"**.
2. Procure por **"Banco de Dados SQL"**, **"Azure Database for PostgreSQL"** ou outro tipo que desejar.
3. Clique em **"Criar"** e preencha os seguintes campos:
   - **Nome do banco de dados**
   - **Grupo de recursos** (crie um novo ou use um existente)
   - **Localização (região)**: escolha uma região próxima para melhor performance.
   - **Opções de autenticação**: defina nome de usuário e senha ou autenticação via Azure AD.

### 3. Configuração do Servidor (ou Instância)
- Será necessário criar um **servidor lógico** para hospedar o banco:
  - Nome do servidor (único no Azure)
  - Nome de administrador
  - Senha segura
  - Região do servidor

### 4. Configurações de Rede
- Escolha se o banco será de **acesso público** (via internet) ou **privado** (acesso restrito a redes virtuais).
- Se optar por acesso público:
  - Adicione o **endereço IP atual** à lista de IPs permitidos.
  - Configure regras de **firewall** para controlar o acesso.

### 5. Revisão e Criação
- Revise todas as configurações.
- Clique em **"Criar"** e aguarde o provisionamento do recurso (pode levar alguns minutos).

---

## Conectando à Instância

Após a criação:

- Copie a **string de conexão** disponível no painel da instância.
- Use uma ferramenta como:
  - [DBeaver](https://dbeaver.io/)
  - Azure Data Studio
  - pgAdmin (para PostgreSQL)
  - SQL Server Management Studio (para Azure SQL)

---

## Dicas Importantes
Autenticação: Prefira métodos seguros. Nunca exponha credenciais em repositórios.

Rede: Limite IPs permitidos e monitore acessos com logs de diagnóstico.

Backups: Azure fornece backups automáticos — entenda como restaurar.

Monitoramento: Use o painel de métricas para acompanhar performance.

Custo: Ao terminar seus testes, exclua recursos para evitar cobranças desnecessárias.

---

## Recursos Complementares:
Documentação oficial do Azure SQL

Azure para PostgreSQL

Gerenciar bancos no Azure Portal

---

## Sobre este repositório
Este repositório foi desenvolvido como parte de um laboratório prático de aprendizado da plataforma Azure. Seu objetivo é reunir um material técnico e didático para facilitar revisões e apoiar estudantes ou profissionais que estão iniciando no uso de serviços de banco de dados em nuvem.

Contribuições são sempre bem-vindas! 
