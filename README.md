# helm
helm install
helm list
NAME    NAMESPACE       REVISION        UPDATED STATUS  CHART   APP VERSION
musaevan@cloudshell:~/mysql (indigo-cirrus)$
mysql image version 
kubectl get deployments -o yaml | grep -i strategy
vim myvalues.yaml
head myvalues.yaml
cp mysql/values.yaml myvalue.yaml
head myvalue
kubectl 
helm ] 
kubectl get deployments 
kubectl get deployments -o yaml | grep -i -A2 
helm install mydb3  --set strategy.type="RollingUpdate" stable/mysql
helm delete mydb3
grep -i maxSurge myvalues.yaml
kubectl get deployments -o yaml | grep -i myvalues.yaml
grep -i maxSurge myvalues.yaml
less mysql/values.yaml

 Upgrade:
 helm upgrade mydb  --set strategy.type="RollingUpgrade" stable/mysql
 helm list
 kubectl get pvc
 helm list 
 helm install --set
 helm install mydb3 --set persistent.enabled=false stable/mysql
 helm list
 kubectl get pvc
 helm upgrade mydb3  --set persistence.enabled=false. --set persistence.size=50Gi stable/mysql
 kubectl get pvc
 
 cd mysql
 mkdir custommysql
 cp -r mysql/* custommysql
 ls cu
 kubectl run nginx --image=nginx --dry-run -o yaml > pod.yaml
 ls pod.yaml
 cat pod.yaml
 vim pod.yaml
 apiVersion: v1
 kind: Pod
 metadata: 
   labels: nginx
   name: nginx
 spec: 
   containers: 
     name: nginx
     image: nginx
     
     
 helm install test my-pod/
 kubectl get pod
 
 
 
 cat template/
 vim template 
 helm install test2 my-chart/
 kubectl get pods test2-pod
 cat templates 
 apiVersion: v1
 kind: Pod
 metadata: 
    labels; 
      release-name: {{. Release.Name }}
      run: {{. Release.Name }}nginx
    name: {{. Release.Name }}-nginx   
 spec:
   containers:
   - image: {{. Values.image }} {{Values.tags}}
     name: {{. Values.image }} 
     
     cat values.yaml
      image: "nginx"
       tag: "1.21"
       
     cat Chart.yaml
     apiVersion: v2
     name: my-pod
     description: A Helm chart for Kubernetes
     type: application
     version: 1.0.0
     apiVersion: "1.21"
     
     
     kubectl get pod test3-nginx
     kubectl get pod  test3-nginx -o yaml | grep image
     kubectl get pods
     helm upgrade test4 --set container1.tag=1.20 my-chart/
     kubectl get pod test4-nginx
     kubectl get pod test4-nginx -o yaml | grep nginx
     kubectl edit pod test4-nginx
     ( k8s upgraded now that's why it works )
     
     
     helm install mysql > { mysql-pod < Pvc < pv}
     helm upgrade mysql:5.8  X {mysql-pod < pvc < pv }
     deployment {mysql-pod:5.7 <> PV (RWO)}
     helm upgrade
     deployment {mysql-pod:5.7 <> PV(RWO) X mysql-pod:5.7 }
     
     
     
