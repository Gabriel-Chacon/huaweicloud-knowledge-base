---
title: Mounting OBS Bucket on Windows using Rclone
layout: default
parent: Object Storage Service (OBS)
grand_parent: Storage
permalink: /docs/storage/obs/mount-obs-bucket-on-windows-using-rclone
---

# Mounting OBS Bucket on Windows using Rclone

V1.0 – July 2025

| **Version**       | **Author**                          | **Description**      |
| ----------------- | ----------------------------------- | -------------------- |
| V1.0 – 2025-07-31 | Fernando Gabriel Chacon  50037923   | Initial Version      |
| V1.0 – AAAA-MM-DD | XXXXXXXXXXXX YYYYYYYY               | Document Review      |

1. Index
{:toc}

## Introduction

Object Storage Service (OBS) is a scalable and secure cloud storage solution provided by Huawei Cloud. 
In many scenarios, users may want to access their OBS buckets directly from a local file system, especially 
on Windows machines. This is useful for browsing, reading, and even uploading files as if they were stored locally.

Rclone is a powerful open-source command-line tool that supports mounting cloud storage services as virtual drives. 
This guide will walk you through the process of mounting an OBS bucket on Windows using Rclone, enabling seamless 
access to your cloud storage directly through the Windows Explorer.

## Creating IAM User and User Group for OBS mounting

It’s recommended to create an exclusive IAM User for mounting in order to restrict access to OBS only.

[Create user](https://console-intl.huaweicloud.com/iam/#/iam/users/create)

Select **Access Type**: Programmatic access, and **Credential Type**: Access key


{% include image.html post=page.path file="create-user" alt="Create a new user" %}

Click on “**create new groups**” to create an User Group for this IAM User and then select it.

{% include image.html post=page.path file="create-user-group" alt="Create a new user group" %}

{% include image.html post=page.path file="select-new-user-group-created" alt="Select new user group created" %}

Download the Access Key (this is the only time it’s available). File “credentials.csv” will be saved.

{% include image.html post=page.path file="download-keys" alt="Download the Access Key" %}

{% include image.html post=page.path file="default-security-group.jpg" alt="Security group default" %}

{% include image.html post=page.path file="security-group-rules-remote-access.jpg" alt="Rules in the security group for remote access" %}

## Configuring ECS

Access ECS through the Huawei Cloud console by clicking “Remote Login” and log in with the “root” user and password configured when creating the ECS.

{% include image.html post=page.path file="ecs-remote-login.jpg" alt="Remote login to ECS" %}

Update the ECS packages by typing the following command:

```shell
apt update && apt upgrade -y
```

Install the XRDP package, which allows Linux instances to be accessed
through Windows Remote Desktop.

```shell
apt install xrdp -y
```

The GDM3 interface manager is used by default on Linux
instances. If desired, other lighter managers can be installed, such as SLiM or LightDM. If prompted, change SLiM
or LightDM to the default manager.

```shell
apt install lightdm -y
```

Install the desired visual interface. In this step-by-step, the visual interface installed will be Ubuntu Desktop.

```shell
apt install ubuntu-desktop
```

Restart the XRDP service to allow Remote Desktop access.

```shell
service xrdp restart
```

Enable the XRDP service to enable the XRDP service to start at system boot.

```shell
systemctl enable xrdp
```

Start the installed interface manager.

```shell
systemctl start lightdm.service
```

Log in to the instance via Remote Desktop. Under “Session”,
select “Xorg”.

{% include image.html post=page.path file="windows-remote-desktop-connection.jpg" alt="Remote Desktop on Windows" %}

{% include image.html post=page.path file="xrdp-login.jpg" alt="xrdp login interface" %}

{% include image.html post=page.path file="remote-desktop-linux.jpg" alt="Remote Desktop with Linux GUI" %}

**Important: It is worth noting that the graphical interface installed on Linux
does not work well with Huawei Cloud Console Remote Login. It is
recommended that Remote Login on the console be used only with
the Linux terminal.**

