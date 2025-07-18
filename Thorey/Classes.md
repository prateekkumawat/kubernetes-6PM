# Kubernetes Namespace ::: 
Namespace in kubernets provide isolation. for control your users ,resources, projects and enviornments that can manage isolated. 
1. Default namespace :::  kubernetes resource create if you are not provide then it will create in a default namespace. production cluster we don't create anything in default namespace. 
2. kube-system ::: kubernetes create all key component  create in this 
3. node-lease ::: kubenrente use this namespace for check helath of nodes and status. 
4. kube-public ::: in this namespace all data is public availabel and readable 

# kubernetes Pod  :::
pod is a smallest unit in kubernetes that manage your containers. kubernetes pod is your compute functional unit. A Pod (as in a pod of whales or pea pod) is a group of one or more containers, with shared storage and network resources, and a specification for how to run the containers. A Pod's contents are always co-located and co-scheduled, and run in a shared context.

# kustomize method or Helm chart 
apiVersion: v1  // kubernete componente manage that call by api like netwowk storage or apps 
kind: Pod       // resource name that manage by kubernetes pod deploument namespace 
metadata:       // information that provide name namespace labels 
  name: myapp
  labels:
    app.kubernetes.io/name: myapp
spec:            // specification of related pod and containers and storage affinity taint 
  volumes: 
  - name: vol
    persistentVolumeClaim:
      claimName: pvname
  affinity
  - noderelasebaseaffinity
    - relasenoderolleoutaffinity
      - effcect: NoSchdule
        key: part1
        value: 'app'    
  containers:                  // containers part 
  - name: myapp
    image: <Image>
    resources:              // limitation 
      limits:
        memory: "128Mi"
        cpu: "500m"
    ports:
      - containerPort: <Port>