# Kubernetes Deployment :::
Deployment is provide facilities run your pods with scale and control with your releases. 
- pod is a single unit if load increase deployment help you to create multiple replicas. 
- if you want update or release new version it will help you to contol your replicas template. 
- most of applciation run and deploy over the kubernetes deployment stretgies. 
- deployment using replicasets 

# Kubernetes Daemonset :::
- Daemoset ensure you pod is running on every node. 
- for network storage logging and monitor stack. 
- if you scale your node its auto create pods in node or if you remove auto delete garabage pods and clean.

# kubernetes Statefulsets :::
A StatefulSet runs a group of Pods, and maintains a sticky identity for each of those Pods. This is useful for managing applications that need persistent storage or a stable, unique network identity.
Stable, unique network identifiers.
Stable, persistent storage.
Ordered, graceful deployment and scaling.
Ordered, automated rolling updates.

# kubernetes Replicaset ::: 
A ReplicaSet's purpose is to maintain a stable set of replica Pods running at any given time. Usually, you define a Deployment and let that Deployment manage ReplicaSets automatically.

# kubernetes job and cron ::: 
Jobs represent one-off tasks that run to completion and then stop. 
cron :: A CronJob starts one-time Jobs on a repeating schedule.


# Kubernetes Secret :::

A Secret is an object that contains a small amount of sensitive data such as a password, a token, or a key. Such information might otherwise be put in a Pod specification or in a container image. Using a Secret means that you don't need to include confidential data in your application code.