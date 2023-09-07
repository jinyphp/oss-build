# 지니 정적 사이트빌더
지니빌더는 라라벨 기반의 정적 웹사이트 빌더 입니다. 복잡한 route 를 추가하지 않고, `resources/views/pages` 폴더안에 마크다운 또는 blade 파일을 만들어 넣기만 하면 됩니다.

## 설치 및 초기화
지니빌더는 공개된 깃허브 저장소와 손쉬운 설치를 위한 composer 프로젝트로 구성되어 있습니다. 다음과 같이 명령을 입력합니다.

```
composer create-project jiny/builder my-site
composer update
```

> 컴포저를 사용하기 위해서는 먼저 시스템에 php와 composer가 설치되어 있어야 합니다.


## 서버실행
지니빌드는 `laravel`을 기반으로 제작된 프로젝트입니다. 따라서, 데이터베이스를 포함하는 완성된 백엔드 서버 프레임으로 확장하여 사용이 가능합니다.

```
php artisan serve
```

> 라라벨의 공식 문서를 활용하여 기능을 확장할 수 있습니다.


## 정적 빌드
지니빌드는 만들어 놓은 리소스를 변환하여 일반적으로 정적 html 파일로 생성합니다.  

artisna의 `build:make` 명령어를 제공합니다. 
```
php artisan build:make
```

명령을 실행하게 되면, 루트 디렉터리에 `/docs` 폴더가 생성되며, 이곳으로 리소스가 변환되어 복제되게 됩니다.

> 생성된 `/docs`를 `github pages`로 변환하여 사이트를 실행할 수 있습니다.

