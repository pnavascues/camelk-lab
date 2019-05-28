# Serverless Integration with CamelK

## One liner
Hands-on lab covering deployment of CamelK to an Openshift Cluster and development of a serverless integration between a REST service and a social messaging mobile App.

IMPORTANT: This hands-on lab requires from participants to be able to download and install cli utilities to their laptop. An IDE with code completion is recommended for developing the integration but a simple text editor will suffice.

## Why is this relevant



## What we will do in this lab (TOC)

#### Lab 01: Install developer environment _[TBD mins]_

In this lab you will learn about the client tooling required to work with CamelK and install it in your laptop. Also, you will connect to the labs' Openshift environment and install CamelK in your namespace.   

  - **IDE** or text editor
  - oc cli & **connecting to Openshift**
  - **CamelK cli** and ```kamel init```

[Lab 01 Instructions](https://github.com/pnavascues/camelk-lab/blob/master/labs/lab01-install-dev-environment.md) <br>
[Lab 01 Script](https://github.com/pnavascues/camelk-lab/blob/master/scripts/script01-install-dev-environment.sh)

#### Lab 02: Install applications _[TBD mins]_

In this lab you will learn about the two applications that we will be integrating and gain understanding on the use case you will be implementing.

  - Application **REST** service
  - **Telegram** mobile app account

[Lab 02 Instructions](https://github.com/pnavascues/camelk-lab/blob/master/labs/lab02-install-applications.md) <br>
[Lab 02 Script](https://github.com/pnavascues/camelk-lab/blob/master/scripts/script02-install-applications.sh)

#### Lab 03: Deploy integration _[TBD mins]_

In this lab you will create your first version of the integration function with CamelK. You will deploy it to Openshift and perform initial testing.

  - **Develop MVP** integration
  - Deploy MVP

[Lab 03 Instructions](https://github.com/pnavascues/camelk-lab/blob/master/labs/lab03-deploy-integration.md) <br>
[Lab 03 Script](https://github.com/pnavascues/camelk-lab/blob/master/scripts/script03-deploy-integration.sh)

#### Lab 04: Test developer mode _[TBD mins]_

In this lab you will learn how to automatically refresh the integration function you are developing as you work on it. You will deploy the finished version to Openshift and perform final testing.

  - Run MVP in **developer mode**
  - Develop **finished integration**
  - Test

[Lab 04 Instructions](https://github.com/pnavascues/camelk-lab/blob/master/labs/lab04-test-dev-mode.md) <br>
[Lab 04 Script](https://github.com/pnavascues/camelk-lab/blob/master/scripts/script04-test-dev-mode.sh)

#### Lab 05: Management _[TBD mins]_

In this lab you will learn how to test the use case and get a peek at how to monitor and debug the integration function and applications.

  - **Monitoring** and alerting
  - Debugging and **logs**

[Lab 05 Instructions](https://github.com/pnavascues/camelk-lab/blob/master/labs/lab05-management.md) <br>
[Lab 05 Script](https://github.com/pnavascues/camelk-lab/blob/master/scripts/script05-management.sh)

#### Extra lab 06: CI/CD, Gitops _[TBD mins]_

In this lab you will learn about how to do a simple CI/CD with CamelK.

[Extra lab 06 Instructions](https://github.com/pnavascues/camelk-lab/blob/master/labs/lab06-cicd.md) <br>
[Extra lab 06 Script](https://github.com/pnavascues/camelk-lab/blob/master/scripts/script06-cicd.sh)

<!--
#### Extra lab 07: Multiple runtimes performance comparison _[TBD mins]_)

In this lab you will learn about how to do a simple CI/CD with CamelK.

[Extra lab 07 Instructions](https://github.com/pnavascues/camelk-lab/blob/master/labs/lab07-runtime-performance.md) <br>
[Extra lab 07 Script](https://github.com/pnavascues/camelk-lab/blob/master/scripts/script07-runtime-performance.sh)
)
-->

## Let's Start!

The only thing you need now is the access info to the remote environment where CamelK will run and client software to interact with it. Please ask your instructor for this information.

If you are running this lab by your self keep in mind the following note.

IMPORTANT: This hands-on lab requires and Openshift Cluster, this can come in the form of a minishift instance running in your laptop or a fully fledged Openshift cluster. Due to the bleeding edge nature of these technologies they can only be showcases in a 3.11 version or above cluster.
