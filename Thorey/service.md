# Kubernetes Expose services :

Expose an application running in your cluster behind a single outward-facing endpoint, even when the workload is split across multiple backends.
kubenretes use expose pod using service method. 
- ClusterIP: you can access your application pod inside kubernetes cluster from any cluster machine.  
- NodePort : you can access your pods from worker machine ip but port range is 30000-32767
- LoadBalancer : if you have any loadblanacer or cloud provision add load balancer service and exposes. this method not used due to cost issues and higher cost. 