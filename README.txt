
Running wordpress with persistent volumes:

- type "kubectl apply -f /home/ubuntu/wordpress-sql/sql-pv.yaml
this will create a persistent volume for the sql server

- type "kubectl apply -f /home/ubuntu/wordpress-sql/wordpress-pv.yaml"
this will do the same thing with a wordpress persistent volume

- type "kubectl apply -k /home/ubuntu/wordpress-sql/"
this command will use the kustomization.yaml file to create the service, the
persistent volume claim and the deployment for wordpress

- type "kubectl get services" which should show which port the service is
running on (a number over 30000).

- go into chrome browser and type http://192.168.10.105:<port_number> to access
the wordpress page
