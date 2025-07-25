# Kubernetes Storages: 

When managing containerized environments, Kubernetes storage is useful for storage administrators, because it allows them to maintain multiple forms of persistent and non-persistent data in a Kubernetes cluster. This makes it possible to create dynamic storage resources that can serve different types of applications.

- Volumes
Volumes are basic entities in Kubernetes, used to provide storage to containers. A volume can support all types of storage, including network file system (NFS), local storage devices, and cloud-based storage services. You can also build your own storage plugins to support new storage systems. Access to volumes can be achieved directly via pods or through persistent volumes

Kubernetes store data in pv (persistent volume ) and pvc (persistent volume claim)
- PersistentVolume (PV) is a storage element in a cluster, defined manually by an administrator or dynamically defined by a storage class (explained below). A PV has its own lifecycle, separate from the lifecycle of Kubernetes pods. The PV API captures storage implementation details for NFS, cloud provider-specific storage systems, or iSCSI.

- PersistentVolumeClaim (PVC) is a user’s storage request. An application running on a container can request a certain type of storage. For example, a container can specify the size of storage it needs or the way it needs to access the data (read only, write, read/write, with one-time or ongoing access)
Beyond storage size and access mode, administrators can offer PVs with custom properties, such as the type of disk (HDD vs. SSD), the level of performance, or the storage tier (regular or cold storage). Users can request storage based on these custom parameters without knowing the implementation details of the underlying storage. This is achieved using the StorageClass resource.

* Kubnetes storage Access mode 
ReadWriteOnce : RWO
the volume can be mounted as read-write by a single node. ReadWriteOnce access mode still can allow multiple pods to access (read from or write to) that volume when the pods are running on the same node. For single pod access, please see ReadWriteOncePod.
ReadOnlyMany : ROX
the volume can be mounted as read-only by many nodes.
ReadWriteMany: RWX
the volume can be mounted as read-write by many nodes.
ReadWriteOncePod: RWOP
the volume can be mounted as read-write by a single Pod.