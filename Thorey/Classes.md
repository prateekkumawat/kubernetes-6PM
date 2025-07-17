# Kubernetes Namespace ::: 
Namespace in kubernets provide isolation. for control your users ,resources, projects and enviornments that can manage isolated. 
1. Default namespace :::  kubernetes resource create if you are not provide then it will create in a default namespace. production cluster we don't create anything in default namespace. 
2. kube-system ::: kubernetes create all key component  create in this 
3. node-lease ::: kubenrente use this namespace for check helath of nodes and status. 
4. kube-public ::: in this namespace all data is public availabel and readable 

# kubernetes Pod  :::
pod is a smallest unit in kubernetes that manage your containers. kubernetes pod is your compute functional unit. A Pod (as in a pod of whales or pea pod) is a group of one or more containers, with shared storage and network resources, and a specification for how to run the containers. A Pod's contents are always co-located and co-scheduled, and run in a shared context.