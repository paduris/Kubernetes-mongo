
##### First create the secret so that it can referenced in deployment file

> ``kubectl apply -f mongo-secret.yml``

> ``kubectl get secret ``

 ##### Apply deployment
> ``kubectl apply -f mongo-deployment.yml``

##### Apply Service 
>``kubectl apply -f mongo-service.yml``

   
##### Verify
>``kubectl describe service mongodb-service``
   
>``kubectl get pod -o wide``

>``kubectl get all | grep mongodb``
>
>

##### Apply config & mongo express
>``kubectl apply -f mongodb-configmap.yml  ``

>``kubectl apply -f mongo-express-deployment.yml ``

> ``kubectl get service``

##### if using minikube
 >``minikube service mongo-express-service``    
>
>
>
>
>
######Namespaces

don't use default namespace

group resources in namespaces - for easy classification

for example:

- Database
- Elastic stack
- Nginx-Ingress
- Monitoring 
- Logging
- Multiple teams
- Environments - prod,non-prod
- limit resources by namespaces




###kubens - tool for handling namespace in Kubernetes 

>``brew install kubectx``
>
> ``kubens``
>
>

#####Ingress
- evaluates all the rules
- manage redirections
- entrypoint to cluster
- many third party implementations ( install ingress controller in cluster- K8s Nginix Ingress Controller )


#####Demonstration
##### Install Ingress Controller in Minikube ( starts K8s Nginix Implementation of Ingress)
 
>``minikube addons enable ingress`` 