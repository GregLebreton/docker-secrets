                              ###### docker-secrets ######
      

  A) création des secrets:
  
      $ echo "myuser" | docker secret create pg_user -

      $ echo "mysupersecretpassword" | docker secret create pg_password -

      $ echo "mydatabase" | docker secret create pg_database -
      
      
  B) déployement du service:
  
      $ docker stack deploy -c docker-postgres-secrets.yml postgres-secret
      
  C) visiter http://127.0.0.1:8080 et choisir le type postgres dans le menu déroulant
  
  D) utiliser les acréditations passées dans les secrets pour vous connectez à la base de donnée
