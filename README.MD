                              ###### docker-secrets ######
 
  A) initialiser docker swarm
  
      $ docker swarm init

  B) création des secrets:
  
      $ echo "myuser" | sudo docker secret create pg_user -

      $ echo "mysupersecretpassword" | sudo docker secret create pg_password -

      $ echo "mydatabase" | sudo docker secret create pg_database -
      
      
  C) déployement du service:
  
      $ docker stack deploy -c docker-postgres-secrets.yml postgres-secret
      
  D) visiter http://127.0.0.1:8080 et choisir le type postgres dans le menu déroulant
  
  E) utiliser les acréditations passées dans les secrets pour vous connectez à la base de donnée
