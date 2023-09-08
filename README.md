# -Microservices-App-K8s-cluster
Online Boutique
is a cloud-first microservices demo application. Online Boutique consists of an 11-tier microservices application. The application is a web-based e-commerce app where users can browse items, add them to the cart, and purchase them.

Screenshots
<img width="1439" alt="Screenshot 2023-09-08 at 4 05 55 PM" src="https://github.com/Tushar240503/-Microservices-App-K8s-cluster/assets/98592305/b4ce09d1-384f-4c35-9fce-3af140166566">
<img width="901" alt="Screenshot 2023-09-08 at 4 04 53 PM" src="https://github.com/Tushar240503/-Microservices-App-K8s-cluster/assets/98592305/0fddb02b-64ba-46f1-bb9b-38f3c085faf6">
<img width="1288" alt="Screenshot 2023-09-08 at 4 05 10 PM" src="https://github.com/Tushar240503/-Microservices-App-K8s-cluster/assets/98592305/879c49b5-f874-401d-bd76-cefd849decac">


Deployment Configurations
Email Service Deployment
The Email Service is deployed as a Kubernetes Deployment.

Name: emailservice
Container Image: gcr.io/google-samples/microservices-demo/emailservice:v0.2.3
Port: 8080
Recommendation Service Deployment
The Recommendation Service is deployed as a Kubernetes Deployment.

Name: recommendationservice
Container Image: gcr.io/google-samples/microservices-demo/recommendationservice:v0.2.3
Port: 8080
Dependencies: Product Catalog Service
Payment Service Deployment
The Payment Service is deployed as a Kubernetes Deployment.

Name: paymentservice
Container Image: gcr.io/google-samples/microservices-demo/paymentservice:v0.2.3
Port: 50051
Product Catalog Service Deployment
The Product Catalog Service is deployed as a Kubernetes Deployment.

Name: productcatalogservice
Container Image: gcr.io/google-samples/microservices-demo/productcatalogservice:v0.2.3
Port: 3550
Currency Service Deployment
The Currency Service is deployed as a Kubernetes Deployment.

Name: currencyservice
Container Image: gcr.io/google-samples/microservices-demo/currencyservice:v0.2.3
Port: 7000
Shipping Service Deployment
The Shipping Service is deployed as a Kubernetes Deployment.

Name: shippingservice
Container Image: gcr.io/google-samples/microservices-demo/shippingservice:v0.2.3
Port: 50051
Ad Service Deployment
The Ad Service is deployed as a Kubernetes Deployment.

Name: adservice
Container Image: gcr.io/google-samples/microservices-demo/adservice:v0.4.1
Port: 9555
Cart Service Deployment
The Cart Service is deployed as a Kubernetes Deployment.

Name: cartservice
Container Image: gcr.io/google-samples/microservices-demo/cartservice:v0.2.3
Port: 7070
Dependencies: Redis
Checkout Service Deployment
The Checkout Service is deployed as a Kubernetes Deployment.

Name: checkoutservice
Container Image: gcr.io/google-samples/microservices-demo/checkoutservice:v0.2.3
Port: 5050
Dependencies: Product Catalog, Shipping, Payment, Email, Currency, Cart, Recommendation, and Ad Services
Frontend Deployment
The Frontend is deployed as a Kubernetes Deployment.

Name: frontend
Container Image: gcr.io/google-samples/microservices-demo/frontend:v0.2.3
Port: 8080
Dependencies: Product Catalog, Currency, Cart, Recommendation, Shipping, Checkout, and Ad Services
Redis Cart Deployment
Redis Cart is deployed as a Kubernetes Deployment and uses the Redis container image.

Name: redis-cart
Container Image: redis:alpine
Port: 6379
Service Configurations
Email Service Service
The Email Service is exposed as a Kubernetes ClusterIP service.

Name: emailservice
Port: 5000
Recommendation Service Service
The Recommendation Service is exposed as a Kubernetes ClusterIP service.

Name: recommendationservice
Port: 8080
Payment Service Service
The Payment Service is exposed as a Kubernetes ClusterIP service.

Name: paymentservice
Port: 50051
Product Catalog Service Service
The Product Catalog Service is exposed as a Kubernetes ClusterIP service.

Name: productcatalogservice
Port: 3550
Currency Service Service
The Currency Service is exposed as a Kubernetes ClusterIP service.

Name: currencyservice
Port: 7000
Shipping Service Service
The Shipping Service is exposed as a Kubernetes ClusterIP service.

Name: shippingservice
Port: 50051
Ad Service Service
The Ad Service is exposed as a Kubernetes ClusterIP service.

Name: adservice
Port: 9555
Cart Service Service
The Cart Service is exposed as a Kubernetes ClusterIP service.

Name: cartservice
Port: 7070
Checkout Service Service
The Checkout Service is exposed as a Kubernetes ClusterIP service.

Name: checkoutservice
Port: 5050
Frontend Service
The Frontend is exposed as a Kubernetes NodePort service.

Name: frontend
Port: 80 (NodePort: 30006)
Redis Cart Service
The Redis Cart is exposed as a Kubernetes ClusterIP service.

Name: redis-cart
Port: 6379
