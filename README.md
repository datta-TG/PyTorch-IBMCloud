# Install PyTorch in IBM Cloud

Are you a data scientist using the IBM Cloud? Well, this documentation is for you. It will guide you on how to install PyTorch on the IBM Cloud using the Kubernetes Service. Simple and effective so you can start programming or using your PyTorch based Machine and Deep Learning models.

## Pre-requisites

You must have an account created in IBM Cloud. The account needs to be either be *Pay-As-You-Go* or *Subscription*. Click [here](https://cloud.ibm.com/docs/account?topic=account-accounts "here") to read more.
If you have a Lite account, you can upgrade it. Click [here](https://cloud.ibm.com/docs/account?topic=account-account-getting-started#account-gs-upgrade "here") to learn how to upgrade.

## Step 1: Provision Kubernetes Cluster

* Click on the search section at the top of the main page, type Kubernetes, and then choose Kubernetes Service.

![](Kubernetes1.PNG)

* A new window opens, select between the free and standard type under "Pricing plan". We'll choose the free plan for the purposes of this documentation. Once selected, click on create.

![Screenshot](Kubernetes2.PNG)

* We then wait a few minutes. The following checkmark and the word 'normal' will appear once the Kubernetes Cluster is deployed.

![Screenshot](Kubernetes3.PNG)


## Step 2:  Deploy IBM Cloud Block Storage plug-in

* Click on the search section at the top of the main page, select IBM Cloud Block Storage, and click on it.

![Screenshot](Storage1.PNG)

* A new window opens, select the cluster and enter the name you want for this workspace, in this case, it will be called _storage-example_, accept the terms, click *Install* and wait a few minutes.

![Screenshot](Storage2.PNG)


## Step 3: Install PyTorhc

* Click on the search section at the top of the main page, type PyTorch and click on it.

![Screenshot](contour1.PNG)

* A new window opens, select the cluster and enter the name you want for the Contour workspace, in this case, it will be called _pytorch-example_, accept the terms and click on *Install*. You can modify the different installation parameters at the bottom. We will leave them by default as shown below, but you can read more about setting up the parameters [here](https://cloud.ibm.com/catalog/content/contour-Qml0bmFtaS1jb250b3Vy-global#about "here").

![Screenshot](contour2.PNG)


## Step 4: Verify Installation

* Go to *Resources List* in the Left Navigation Menu and click on *Kubernetes*.

![Screenshot](test1.PNG)

* Click the *Actions* button and select *Web terminal*.

![Screenshot](test2.PNG)

* A window opens to install the web terminal, click on install and wait a few minutes. The window will pop up at the buttom If the web terminal is already installed.

![Screenshot](test3.PNG)

* Once you have installed the terminal, click on the action button again, select web terminal, and type the following commands. It will show you the workspaces of your cluster. You can see *pytorch-example* is now active.

`$ kubectl get ns`

![Screenshot](test4.PNG)

`$ kubectl get pod -n contour-example -o wide`

![Screenshot](test5.PNG)

`kubectl get service -n contour-example`

![Screenshot](test6.PNG)

You have finished the installation, enjoy your Contour installation!

