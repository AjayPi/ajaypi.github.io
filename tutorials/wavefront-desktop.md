# Adding Observability Using Python in a Kubernetes Environment with Wavefront

## Introduction

**Wavefront** is a cloud-based monitoring and analytics platform. It allows you to collect, visualize, and analyze metrics, traces, and histograms from your applications and infrastructure. To use Wavefront, you need to have a **Wavefront account**. As "the Company" has a corporate account, you should be able to sign in to Wavefront using your corporate credentialshas a subscription.

You also need to have a <div class="hover-text">Left
  <span class="tooltip-text left">Tooltip Text</span>
  
</div><div class="tooltip">test
  <span class="tooltiptext">A Wavefront cluster is a dedicated instance of Wavefront that hosts your data and dashboards.</span>
</div>
 **Wavefront cluster** and an **API token**.  An API token is a secret key that allows you to send data to and query data from your Wavefront cluster.

To send data to Wavefront, you need to use a Wavefront sender. A Wavefront sender is a library or a tool that collects and formats data from your sources and sends it to Wavefront. Wavefront supports various types of senders, such as SDKs, agents, proxies, and integrations. You can choose the sender that best suits your needs and environment.

To query data from Wavefront, you need to use the Wavefront Query Language. The Wavefront Query Language is a powerful and expressive language that allows you to manipulate and analyze data in Wavefront. You can use the Wavefront Query Language to create charts, alerts, and dashboards. You can also use the Wavefront UI or the Wavefront API to interact with the Wavefront Query Language.
This document provides a guide on how to add observability for desktop users using Python to connect to a Kubernetes environment. The observability portion will be handled by Wavefront.

## Prerequisites
- Python 3.x installed on your desktop
- Access to a Kubernetes environment
- Wavefront account

## Setting Up Your Environment

### Python Setup
Ensure that Python is correctly installed on your desktop. You can verify the installation by running the following command in your terminal:

```
python --version
```

### AWS Setup

To connect to AWS, you need to install and configure the AWS CLI (Command Line Interface). Here’s a basic guide:
1.	**Install the AWS CLI**: You can download and install the AWS CLI from the official AWS website. The installation process varies depending on your operating system.
2.	**Configure the AWS CLI**: Once the AWS CLI is installed, you can configure it by running the `aws configure` command in your terminal. You’ll be prompted to enter your AWS Access Key ID, Secret Access Key, default region name, and default output format.
   
```
aws configure
AWS Access Key ID [None]: YOUR_ACCESS_KEY
AWS Secret Access Key [None]: YOUR_SECRET_KEY
Default region name [None]: YOUR_REGION
Default output format [None]: json
```
Replace `YOUR_ACCESS_KEY`, `YOUR_SECRET_KEY`, and `YOUR_REGION` with your actual AWS Access Key ID, Secret Access Key, and default region name.

### Kubernetes Setup

To connect to a Kubernetes environment hosted in AWS, you can use the AWS CLI and kubectl. Here’s a basic guide:
1.	**Install kubectl**: You can download and install kubectl from the official Kubernetes website. The installation process varies depending on your operating system.
2.	**Connect to your Kubernetes cluster**: After configuring the AWS CLI, you can connect to your Kubernetes cluster using kubectl. First, you need to update the kubeconfig file for your cluster. You can do this with the following command:

```
aws eks --region region update-kubeconfig --name cluster_name
```

Replace region with your AWS region and cluster_name with the name of your Kubernetes cluster.

### Wavefront Setup

To set up your Wavefront account, follow the steps described below:

1.	**Sign in to Wavefront** : As we have a corporate account, you should be able to sign in to Wavefront using your corporate credentials.
2.	**Create a new user**: Once signed in, you can create a new user for yourself. Navigate to `Browse > Users` and click on `Add User`. Enter your details and click on `Create`.
3.	Assign roles to the user: After creating a new user, you need to assign roles to the user. Roles determine what permissions the user has. Navigate to `Browse > Roles`, select a role, and add your user to the role.

## 
