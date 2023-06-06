# Storage <!-- omit in toc -->

> [Documentación Oficial](https://kubernetes.io/docs/concepts/storage/volumes/)

> [Access Modes](https://kubernetes.io/docs/concepts/storage/persistent-volumes/#access-modes)

# 1. EBS CSI
https://docs.aws.amazon.com/eks/latest/userguide/managing-ebs-csi.html

## 1.1. Agregar el addon desde consola

## Revisar el addon
```
kubectl get daemonset ebs-csi-node -n kube-system
```
# 2. Storage Class

```
 k get storageclass
```

## 2.1. Crear un PVC: pvc-test.yaml
```yaml
apiVersion: v1
kind: PersistentVolumeClaim
metadata:
  name: pvc-test
  namespace: default

spec:
  storageClassName: gp2
  accessModes:
    - ReadWriteOnce
  resources:
    requests:
      storage: 50Mi
```

## 2.2. revisar PVC
```
k get pvc
```
> STATUS PENDING

## 2.3. revisar PV
```
k get pv
```
> No resources found

## 2.4. Crear un pod que consuma el PVC: pod-test.yaml
```yaml


```
