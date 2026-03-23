# Docker
Docker Study

# 왜 도커를 사용하는가 
  - 매번 귀찮은 설취 과정을 일일이 거치지 않아도 된다.
  - 항상 일관되게 프로그램을 설치할 수 있다. (버전, 환경, 옵션, 운영 체제 등)
  - 각 프로그램이 독립적인 환경에서 실행되기 떄문에 프로그램 간에 서로 충돌이 일어나지 않는다
-----------------------------
   
<img width="786" height="302" alt="image" src="https://github.com/user-attachments/assets/d0bff8e0-0d63-4e6a-83a2-54244338304c" />

### docker 설치후 nignx로 흐름 살펴보기

<img width="918" height="460" alt="image" src="https://github.com/user-attachments/assets/a41d97f8-37b7-4093-a4e0-e3635645e8ac" />

## Dockerhub
- image를 다운받을수 있는 저장소 __"github와 유사"__
- Tags -> 이미지의 특정 버전

### image 삭제해보기
/명령어/
- docker image rm (image ID 4자이상)
  - Error response from daemon: conflict: unable to delete dec7a90bd097 (must be forced) - image is being used by stopped container f562952b09ac -> image가 실행되었다 중단된 상태여서 해당 image 종료 못함
  - docker image rm -f (image ID 4자이상) __-f__ 중단된 image 삭제 명령어
- docker image ls -> 리스트 확인
- docker image rm $(docker image -q) 컨테이너에서 사용하고 있지 않은(실행 or 중단) 전체 image 삭제
- docker image rm -f $(docker image -q) 중단된 image 삭제
