Déployons notre première application sur Kubernetes avec la commande `kubectl create`.

Nous devons fournir le nom du déploiment et l'image du conteneur à deployer.

`kubectl create deployment myfirstapp --image=nginx`{{execute}}

Parfait! Nous venons de deployer notre première application.

Pour lister les depoiements:

`kubectl get deployments`{{execute}}

Nous pouvons voir le déploiement qui execute une instance de nginx sur un noeud.