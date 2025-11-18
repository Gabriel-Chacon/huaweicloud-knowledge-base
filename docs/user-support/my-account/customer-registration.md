---
title: Customer Registration
layout: default
parent: My Account
grand_parent: User Support
permalink: /docs/user-support/my-account/customer-registration
---

# Customer Registration

V1.0 – Nov 2025

| **Version**       | **Author**                          | **Description**      |
| ----------------- | ----------------------------------- | -------------------- |
| V1.0 – 2025-11-17 | Fernando Gabriel Chacon  50037923   | Initial Version      |
| V1.0 – 2025-11-17 | Gabriel Gutierrez  00817435         | Document Review      |

1. Index
{:toc}

## Introduction

Huawei Cloud provides a global and secure cloud platform. Before accessing cloud services, customers must create and activate their accounts through the official registration portal. This guide provides a complete and structured walkthrough for new customers to complete the registration process successfully.

## Registration Flow

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

## Steps

### 1. Enter the Home Page

Access the official Huawei Cloud website: [https://www.huaweicloud.com/intl/en-us/](https://www.huaweicloud.com/intl/en-us/)

{% include image.html post=page.path file="step1-huawei-cloud-home-page.png" alt="Huawei Cloud Home Page" %}

### 2. Open the Registration Page

Open the registration portal:

[https://reg.huaweicloud.com/registerui/intl/register.html?locale=pt-br&service=https://intl.huaweicloud.com/pt-br/](https://reg.huaweicloud.com/registerui/intl/register.html?locale=pt-br&service=https://intl.huaweicloud.com/pt-br/)

{% include image.html post=page.path file="step2-register-page.png" alt="Register Page" %}

### 3. Complete the Verification

Provide the required email or mobile verification code to proceed.

{% include image.html post=page.path file="step3-set-security-phone-number.png" alt="Set Security Phone Number" %}

### 4. Authorize and Log In

Confirm the authorization request and log in to your new account.

{% include image.html post=page.path file="step4-authorize-and-log-in.jpg" alt="Authorize and Log-in" %}

### 5. Enable Huawei Cloud Services

Proceed to enable available Huawei Cloud services for your account.
{% include image.html post=page.path file="step5-enable-huawei-cloud-services.jpg" alt="Enable Huawei Cloud Services" %}

### 6. Bind Mobile Number

Bind a valid mobile number for account security and identity confirmation.

{% include image.html post=page.path file="step6-bind-mobile-number.png" alt="Bind Mobile Phone Number" %}

### 7. Complete Account Information

Fill in the requested information.

Enter CNPJ and other fields will be filled automatically (data is retrieved through an API integrated with Serasa)

{% include image.html post=page.path file="step7-complete-account-information_1.jpg" alt="Complete Account Information 1" %}
{% include image.html post=page.path file="step7-complete-account-information_2.jpg" alt="Complete Account Information 2" %}

### 8. Activate Your Account (Not required)

Account activation may not be necessary depending on the selected services.

{% include image.html post=page.path file="step8-enable-your-account.png" alt="Enable your account" %}

