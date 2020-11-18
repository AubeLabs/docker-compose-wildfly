# docker-compose-wildfly
1. widlfly 3개 인스턴스(컨테이너) 실행
2. 클러스터링

# docker-compose
docker-compose -f docker-compose-wildfly.yml up -d

docker-compose run -d wildfly-site-in <br>
docker-compose run -d wildfly-site-ex <br>
docker-compose run -d wildfly-down

# wildfly 컨테이너 접속
docker exec -it wildfly-site-in /bin/bash <br>
docker exec -it wildfly-site-ex /bin/bash <br>
docker exec -it wildfly-down /bin/bash

# widlfly user setting
cd wildfly/bin <br>
sh add-user.sh -u admin -p 비밀번호

# log 확인
docker logs --details -ft wildfly-site-in
