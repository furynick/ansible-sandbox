**Start containers**:  
  `docker-compose up -d`

**Connect to ansible Control node**:  
  `docker exec -it ansible_ctrl_1 /bin/bash -c 'exec su - ansible'`

**Stop containers**:  
  `docker-compose stop`
