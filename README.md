# KubePoc.Stack
Arquivos de configuração do cluster Kubernetes/Openshift.



---------
OPENSHIFT
---------

Para criar um template à partir de um projeto já existente no cluster, basta executar o comando:
    oc get -o yaml --export buildConfigs,deploymentConfigs,imageStreams,routes,services > kubepoc_template.yaml

Para adicionar o template, basta importar o yaml via Web Console.

Para criar os objetos do template no cluster, basta executar o seguinte comando:
    oc process kubepoc-template | oc create -f -


Obs.: antes é necessário logar no cluster:
    oc login --token=blablabla --server=https://endereco:6443