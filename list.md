# dia 1
ok repaso contenedores 20min
ok repaso kubernetes 30 min  = 7pm

ok intro eks = 7.30
ok lab 1 instalacion y conexion 1h = 8.30

ok 02 practica  repaso  pods - deploy - svc 1h

# dia 2
ok users & kubeconfig
ok Opciones de computo: spot - fargate - instance type (spot) 20m = 6:20

lab 2 instalación de fargate 45min = 7.05pm
03 practica: instalación desde cero cluster eks 50h = 8:30pm
04 ingress 1h
loadbalancer

# dia 3
lab 4, habilitar lb
05 practica, lb y conectar con ingress
storage
autoscaling

# dia 4
cloud watch
ops view
escalar manualmente el cluster
cluster autoscaling
hpa

ECR
secrets

guard duty
encryption




rbac
> revisar permisos del ususario admin
> Si es necesario Eliminar la restricción de cuarentena por llave ssh

# 3. Crear nuevo usuario AWS
```
NEW_USER=<USER_NAME>
aws iam create-user --user-name $NEW_USER
aws iam create-access-key --user-name $NEW_USER | tee /tmp/create_output.json
aws iam add-user-to-group --group-name EKS  --user-name $NEW_USER

```
