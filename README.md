# 데이터 엔지니어링 중급 실습

> 데이터 엔지니어링 중급 과정 실습을 위한 페이지 입니다.

## [1일차. 데이터 엔지니어링 기본](https://github.com/siyoungoh/data-engineer-intermediate-training/tree/master/day1/README.md)

## [2일차. 아파치 스쿱 테이블 수집](https://github.com/siyoungoh/data-engineer-intermediate-training/tree/master/day2/README.md)
        
## [3일차. 아파치 스파크](https://github.com/siyoungoh/data-engineer-intermediate-training/tree/master/day3/README.md)

## [4일차. 아파치 하이브](https://github.com/siyoungoh/data-engineer-intermediate-training/tree/master/day4/README.md)
        
## [5일차. 지표 생성 프로젝트](https://github.com/siyoungoh/data-engineer-intermediate-training/tree/master/day5/README.md)

## 1. 클라우드 장비에 접속

> 개인 별로 할당 받은 `ubuntu@vm[number].aiffelbiz.co.kr` 에 putty 혹은 terminal 을 이용하여 접속합니다


### 1-1. 원격 서버로 접속합니다
```bash
# terminal
# ssh ubuntu@vm001.aiffelbiz.co.kr
# password: ******
```

### 1-2. 패키지 설치 여부를 확인합니다
```bash
docker --version
docker-compose --version
git --version
```

<details><summary> :green_book: [실습] 출력 결과 확인</summary>

> 출력 결과가 오류가 발생하지 않고, 아래와 같다면 성공입니다

```text
Docker version 20.10.6, build 370c289
docker-compose version 1.29.1, build c34c88b2
git version 2.17.1
```

</details>

## 2. 실습자료 Git 으로 가져오기
1. 초기 설정 - clone
    ```bash
    # git 설치 확인 - 버전이 뜨면 정상 설치되어있는 상태
    git --version
    # 원하는 폴더로 이동
    cd ~/work
    # clone 해오기
    git clone {git repo 주소}
    
    # clone 되었는지 확인 - git repo이름의 폴더가 생겼다면 된 것
    ls
    ```

2. 내가 수정한 내역을 없애고 업데이트된 자료 가져오기 
```bash
# 원하는 폴더로 이동
cd ~/work/{폴더명}

# 내가 작업한 수정사항 없애버리기 - 로컬 repo의 이전 commit 의 파일상태로 돌아가기
git checkout -- .

# 상태를 확인해보기 - 변경사항이 없다고 보임
git status -sb

# 그동안 원격 repo-github 의 수업자료-에서 추가된 commit 내역 가져오기
git pull
```
