# Lab 01: Install Developer Environment

This lab is about getting you ready to start working with the applications!

After finishing Lab 01 you should have accomplished the following:

  * You have the project's files cloned from github.com and something to edit them with
  * You have Openshift's client ``oc`` installed and have logged into your Openshift environment
  * You have CamelK's client ``kamel`` installed and have installed CamelK operator in your project

The process is simple and straightforward, just follow the steps bellow.   

> REQUIREMENTS:
* You must be able to download a binary to your $PATH and execute it.
* You must be able to allow Openshift's client to establish HTTPS connections to port 8443 in the remote Openshift cluster.     
* You should have some form of git client tooling installed. We'll assume you are using the ``git`` command.  

## Github repo's files and IDE

Start by cloning the labs github repo to your harddrive.

    git clone https://github.com/pnavascues/camelk-lab.git

Navigate to the repo directory.

    cd camelk-lab

This directory will be the root of all the commands and file paths mentioned in this documentation. We will store it in the environment variable ``${LAB_DIR}``  

    export LAB_DIR=$(pwd)

> IMPORTANT:<br>
  If you start a new shell remember to execute this command again in the repo's home directory before following this lab's instructions.  

Take a look at the repo's content and familiarize yourself with it. The most noteworthy items are:

* ``labs``directory contains the labs documentation in Markdown and PDF files like this one you are reading right now!
* ``files`` directory contains any support material required like the REST application we will deploy in Lab 02: Install Application
* ``scripts`` directory contains a script per lab that when executed will complete the tasks in the lab. This is provided in case you are running behind and want to catch up to the class. Each script will reset the environment completely and execute the steps required to leave it as the current lab would have if completed.  

To end this section make sure **you have something available to edit the labs files**. It really doesn't matter what you use for the labs editing as you will be copying and pasting the code. Therefore vi, gedit, etc. are fine, but to get the best experience you can install a proper IDE with Camel Language integration, Openshift Integration, etc. We suggest [Red Hat CodeReady Studio](https://developers.redhat.com/products/codeready-studio/download/) or [Visual Studio Code](https://code.visualstudio.com/download).

## Openshift client

`oc` is the command of the Openshift client. In the scope of this labs is used to provide connectivity and authentication against the Openshift cluster. It can also be used to get an insiders view on the workings of CamelK, we will include some of the commands when appropriate.   

To install it start by downloading the 3.11 client appropriate to your system from one of this sources:
* [Red Hat Customer Portal Official Release Page](https://access.redhat.com/downloads/content/290/ver=3.11/rhel---7/3.11.98/x86_64/product-software)
* [Openshift Comunity Client Downloads Page](https://access.redhat.com/downloads/content/290/ver=3.11/rhel---7/3.11.98/x86_64/product-software)

Open the downloaded file, depending on your system it will be a .zip file or a tar.gz. Within you will find the ``oc`` binary file. Copy it to your harddrive into a directory that is in your ${PATH} variable so that you can execute it from any path from you command line.

To test if this worked you are going to connect and login into your Openshift account. Let's test this worked.

      > cd ${LAB_DIR}
      > oc login ${OPENSHIFT_CLI_URL} -u ${OPENSHIFT_USER} -p ${OPENSHIFT_PASSWORD} --insecure-skip-tls-verify
      Login successful.

      You don't have any projects. You can try to create a new project, by running

          oc new-project <projectname>

If that worked you should get access to an empty environment. Commands like `oc get pods` or `oc get projects` will return that you have nothing deployed yet. Try it out!

> IMPORTANT:
  This step is critical. If you can't connect ask your instructor for help and don't skip the step.

As a last step you will create the project where you will later deploy the sample REST service, CamelK and the integrations developed.

Projects names are unique in an Openshift cluster, so to avoid using the same name as your companions choose a project name and substitute the variable ``${PROJECT_NAME}`` with it.

    >oc new-project ${PROJECT_NAME}
    Now using project "${PROJECT_NAME}" on server "https://192.168.42.177:8443".

    You can add applications to this project with the 'new-app' command. For example, try:

        oc new-app centos/ruby-25-centos7~https://github.com/sclorg/ruby-ex.git

    to build a new example application in Ruby.

Let's continue!

## CamelK client

`kamel` is the CamelK client that will allow us to deploy CamelK to your project in the Openshift cluster and also deploy and configure our integrations.

To install it start by downloading the 0.3.3 client appropriate to your system from:
* [CamelK Community 0.3.3 Release Page](https://github.com/apache/camel-k/releases/tag/0.3.3)

Open the downloaded file, depending on your system it will be a .zip file or a tar.gz. Within you will find the `kamel` binary file. Copy it to your harddrive into a directory that is in your ${PATH} variable so that you can execute it from any path from you command line.

To test if this worked you are going to attempt to install CamelK into your project in the Openshift cluster. Just type at your shell:

    >kamel install                                       
    Camel K installed in namespace ${PROJECT_NAME}

If that worked you should get access to an empty CamelK environment. Commands like `kamel get`will return that you have no integrations deployed yet. Try it out!

If that worked **Congratulations!**

This concludes Lab 01! You can now continue to [Lab 02](https://github.com/pnavascues/camelk-lab/blob/master/labs/lab02-install-applications.md) or go to the [Lab Index](https://github.com/pnavascues/camelk-lab/blob/master/README.md)
