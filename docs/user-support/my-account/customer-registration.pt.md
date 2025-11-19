---
title: Registro de Cliente
layout: default
parent: Minha Conta
grand_parent: Suporte ao Usuário
lang: pt 
permalink: /docs/user-support/my-account/customer-registration
---

# Registro de Cliente

V1.0 – Nov 2025

| **Versão**        | **Autor**                           | **Descrição**        |
| ----------------- | ----------------------------------- | -------------------- |
| V1.0 – 2025-11-19 | Fernando Gabriel Chacon  50037923   | Initial Version      |
| V1.0 – 2025-11-19 | Gabriel Gutierrez  00817435         | Document Review      |

1. Índice
{:toc}

## Introduction

A Huawei Cloud fornece uma plataforma de nuvem global e segura. Antes de acessar os serviços de nuvem, os clientes devem criar e ativar suas contas por meio do portal oficial de registro. Este guia oferece um passo a passo completo e estruturado para que novos clientes concluam com sucesso o processo de registro.

## Fluxo de Registro

<pre class="mermaid">
flowchart TD
    %% Main Flow
    A["1️⃣ Home page"] --> B["2️⃣ Register page"]

    subgraph Z[" "]
        B -.-> B1["Fill in:<br>- Country<br>- Email<br>- Password"]
    end

    subgraph ZA[" "]
        B1 --> C["3️⃣ Email/phone verification"]
        C -.-> C1["Receive and fill in<br>verification code"]
        C1 -.-> C2["Authorize and login, agree with <b>Huawei Cloud Customer Agreement and Privacy Statement</b>"]
    end

    C2 --> D["Registration info display"]
    D --> E["4️⃣ Complete information"]

    subgraph ZB[" "]
        E -.-> E1["Phone verification"]
        E1 -.-> E2["Select <b>Enterprise</b> as Tenant Type"]
        E2 -.-> E3["Fill in:<br>- CNPJ<br>- Contact Name<br>- Designation<br>- Industry"]
    end

    E3 --> F["✅ Done"]

    classDef main fill:#cce5ff,stroke:#336699,stroke-width:1px;
    classDef gray fill:#f0f0f0,stroke:#aaa;
    classDef red fill:#fff,stroke:#000,color:#a00,font-weight:bold;
    classDef white fill:#fff,stroke:#000,color:#000;

    class A,B,C,E,F main;
    class D gray;
    class B1,C1,C2,E1,E2,E3 white;
</pre>

## Etapas

### 1. Acessar a Página Inicial

Acesse o site oficial da Huawei Cloud: [https://www.huaweicloud.com/intl/en-us/](https://www.huaweicloud.com/intl/en-us/)

{% include image.html post=page.path file="step1-huawei-cloud-home-page.png" alt="Huawei Cloud Home Page" %}

Clique no botão **Sign Up** no canto superior direito para abrir o portal de registro.

{% include image.html post=page.path file="step2-register-page.png" alt="Register Page" %}

Informe seu e-mail, clique em **Get Code**, insira o código de verificação recebido em sua caixa de entrada, defina uma senha e clique no botão **Register**.

### 2. Completar a Verificação

Nesta etapa opcional, você pode adicionar um número de telefone para aumentar a segurança da conta.
Se desejar configurá-lo, insira seu número de celular, clique em Get Code, informe o código recebido por SMS e clique em OK. Caso contrário, clique em **Skip**.

{% include image.html post=page.path file="step3-set-security-phone-number.png" alt="Set Security Phone Number" %}

### 3. Autorizar e Fazer Login

Confirme a solicitação de autorização clicando no botão **Authorize**.

{% include image.html post=page.path file="step4-authorize-and-log-in.jpg" alt="Authorize and Log-in" %}

### 4. Ativar os Serviços da Huawei Cloud

Prossiga para ativar os serviços da Huawei Cloud. Aceite o acordo do cliente e a declaração de privacidade, e opcionalmente selecione a opção para receber atualizações sobre descontos e promoções. Em seguida, clique em **Enable**.

{% include image.html post=page.path file="step5-enable-huawei-cloud-services.jpg" alt="Enable Huawei Cloud Services" %}

### 5. Vincular Número de Celular

Vincule um número de celular válido para a segurança da conta e verificação de identidade. Insira seu número de telefone, clique em **Send Code**, insira o código de verificação recebido por SMS e clique em **Next**.

{% include image.html post=page.path file="step6-bind-mobile-number.png" alt="Bind Mobile Phone Number" %}

### 6. Completar as Informações da Conta

Preencha as informações solicitadas. Informe o CNPJ e os demais campos serão preenchidos automaticamente (os dados são obtidos por meio de uma API integrada com a Serasa).

{% include image.html post=page.path file="step7-complete-account-information.png" alt="Complete Account Information 1" %}

### 7. Ativar Sua Conta (Não obrigatório)

A ativação da conta pode não ser necessária, dependendo dos serviços selecionados.

{% include image.html post=page.path file="step8-enable-your-account.png" alt="Enable your account" %}
