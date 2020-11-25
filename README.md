
docker rmi `docker images | grep "repos" | awk {'print $3'}`
docker rmi $(docker images --filter "dangling=true" -q --no-trunc)
docker rmi `docker images | grep "openresearch" | awk {'print $3'}`
docker-compose -p "OpenResearch" -f docker-compose-openresearch.yaml up
docker-compose -p "OpenResearch" -f docker-compose-openresearch.yaml up --build
docker build --tag task_service_component:1.0 . && docker run --env-file ./.env --publish 8040:80 --detach --name task task_service_component:1.0
sudo ntpdate time.nist.gov