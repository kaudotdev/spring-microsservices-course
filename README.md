# Microsserviços Java com Spring Boot e Spring Cloud - Curso Udemy ☕

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Udemy](https://img.shields.io/badge/Udemy-A435F0?style=for-the-badge&logo=Udemy&logoColor=white)

Este repositório contém as tarefas e projetos desenvolvidos durante o curso **Microsserviços Java com Spring Boot e Spring Cloud** ministrado por Nélio Alves na plataforma Udemy.

O objetivo principal deste repositório é aplicar e demonstrar os conhecimentos adquiridos na construção de uma arquitetura de microsserviços robusta e escalável utilizando o ecossistema Spring e containers Docker.

---

## 🎯 Sobre o Curso

O curso foca na implementação de uma arquitetura de microsserviços utilizando as principais ferramentas do Spring Framework e Docker. Aborda desde a criação e comunicação entre serviços até questões de segurança, resiliência, gerenciamento de configurações e conteinerização.

**Instrutor:** [Nélio Alves](https://www.udemy.com/user/nelio-alves/)

---

## 🚀 Tecnologias e Ferramentas

| Ícone | Tecnologia/Ferramenta |
| :---: | --- |
| ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white) | **Java 11** |
| ![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white) | **Spring Boot & Spring Cloud** |
| ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white) | **Docker** |
| ![Netflix Eureka](https://img.shields.io/badge/Netflix_Eureka-6DB33F?style=for-the-badge&logo=netflix&logoColor=white) | **Eureka (Service Discovery)** |
| ![Netflix Zuul](https://img.shields.io/badge/Netflix_Zuul-6DB33F?style=for-the-badge&logo=netflix&logoColor=white) | **Zuul (API Gateway)** |
| ![OpenFeign](https://img.shields.io/badge/OpenFeign-6DB33F?style=for-the-badge&logo=spring&logoColor=white) | **Feign & Ribbon (Comunicação)** |
| ![Hystrix](https://img.shields.io/badge/Hystrix-6DB33F?style=for-the-badge&logo=netflix&logoColor=white) | **Hystrix (Circuit Breaker)** |
| ![OAuth2](https://img.shields.io/badge/OAuth2-262626?style=for-the-badge&logo=oauth&logoColor=white) | **OAuth2 & JWT (Segurança)** |
| ![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apache-maven&logoColor=white) | **Maven** |

---

## 📂 Estrutura do Projeto (Baseada nos Módulos do Curso)

O repositório está organizado seguindo as fases apresentadas no curso, com cada diretório correspondendo a um ou mais componentes da nossa arquitetura de microsserviços.

### Seção 2: Fase 1 - Comunicação Simples, Feign, Ribbon
Nesta fase, iniciamos a comunicação entre os microsserviços.
* `hr-worker/` - 👷 Microsserviço com a lógica de negócio do "trabalhador".
* `hr-payroll/` - 💰 Microsserviço que consome dados do `hr-worker` usando **Feign** para comunicação e **Ribbon** para balanceamento de carga.

### Seção 3: Fase 2 - Eureka, Hystrix, Zuul
Aqui, adicionamos componentes essenciais para a governança e resiliência da arquitetura.
* `hr-eureka-server/` - 🌐 **Service Discovery** que registra e gerencia as instâncias dos outros serviços.
* `hr-api-gateway-zuul/` - 🚪 **API Gateway** que serve como ponto de entrada único para o sistema, aplicando roteamento e filtros.
* Implementação do **Hystrix** para tolerância a falhas (Circuit Breaker).

### Seção 4: Fase 3 - Configuração Centralizada
Centralizamos as configurações de todos os microsserviços para facilitar o gerenciamento.
* `hr-config-server/` - 🔧 **Servidor de Configuração** que fornece as propriedades para todos os microsserviços a partir de um repositório Git.

### Seção 5: Fase 4 - Autenticação e Autorização
Implementamos a camada de segurança para proteger nossos serviços.
* `hr-user/` - 👤 Microsserviço para gerenciamento de usuários e papéis.
* `hr-oauth/` - 🔑 **Servidor de autorização** com **OAuth2** e **JWT** para gerar e validar tokens de acesso.

### Seção 6: Criando e Testando Containers Docker
Nesta fase, preparamos nossa aplicação para o deploy usando containers.
* `Dockerfile` - 🐳 Arquivos de configuração do Docker em cada microsserviço para a criação de suas respectivas imagens.

---

## ▶️ Como Executar

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)
    ```

2.  **Execute com o Maven:**
    Siga a ordem de inicialização para garantir que as dependências entre os serviços sejam atendidas:
    1.  `hr-config-server`
    2.  `hr-eureka-server`
    3.  `hr-worker`
    4.  `hr-payroll`
    5.  `hr-user`
    6.  `hr-oauth`
    7.  `hr-api-gateway-zuul`

    Em cada diretório, execute: `mvn spring-boot:run`



---

<p align="center">
  Feito com ❤️ por <a href="https://github.com/kaudotdev">Kaudotdev</a>
</p>
