      ###### docker-secrets ######
      
      
# processus

  A) création des secrets:
  
      $ echo "myuser" | docker secret create pg_user -

      $ echo "mysupersecretpassword" | docker secret create pg_password -

      $ echo "mydatabase" | docker secret create pg_database -
      
      
  B) céation de du fichier postgres-secrets.yml
  
      $ 
