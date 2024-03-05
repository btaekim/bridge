# PRM README
### update
2024-02-19
------------------
```
```

# 1. 가상화
```
$ cd prm
$ python3 -m venv .venv

$ .\.venv\Scripts\activate
```

# 2. pip install
### pip requirements install
### 메세지대로 pip 업그레이드, visual c++ 개별 설치 (odbc 때문)
```
$ pip install -r requirements.txt

# 현재 설치된 pip를 requirements.txt 에 버전 목록화
$ pip freeze > requirements.txt
```

```
F:\Python\fastapi\bridge> uvicorn main:app --reload

F:\Python\fastapi\bridge\frontend> npm run dev

<!-- uvicorn 강제 종료 -->
F:\Python\fastapi\bridge> npx kill-port 8000
```

### 리비전 파일 생성
```
<!-- 처음 실행할때만 -->
alembic init migrations

<!-- 수정사항이 있을때 -->
alembic revision --autogenerate
alembic upgrade head

```


# 3. .env write
### 프로젝트 열때 윈도우 환경변수 자동으로 불러오게 하기 위함. 프로젝트 폴더의 최상위에 만들어 둘것.
### python-dotenv -> 2번에서 pip 설치가 되어 있어야 함
### .env 파일을 만들고 아래 내용을 복붙. APP_CONFIG_FILE 파일 경로는 수정 해야함.
```
FLASK_APP=prm
FLASK_ENV=development
FLASK_DEBUG=True
DEBUG=development
FLASK_RUN_HOST=0.0.0.0
FLASK_RUN_PORT=8080

APP_CONFIG_FILE=F:\Python\flask\prm\config\development.py
```


# 4. SECRET_KEY 생성 

The secret key is needed to keep the client-side sessions secure. You can generate some random key as below:
클라이언트 측 세션을 안전하게 유지하기 위해서는 비밀키가 필요하다. 다음과 같이 임의의 키를 생성할 수 있다.

ex)
```
>> python3
>> import os
>> os.urandom(24)
>> b'\xfd{H\xe5<\x95\xf9\xe3\x96.5\xd1\x01O<!\xd5\xa2\xa0\x9fR"\xa1\xa8'
```

### SECRET_KEY = b'\xe6u\x88\xad~,v5q\xfa\xdb}v\xa4\xf0\x0c\xb2\rf\x8e|\xb4\xdd\x95'

------------

# 5. flask run
### 설치 완료되면 바로 프로젝트를 실행한다.
### $ .\.venv\Scripts\activate 가상화가 실행 되어 있어야 함.
```
$ flask run
```




# ubuntu hostname 변경
```
sudo hostnamectl set-hostname 바뀔이름

sudo reboot
```

# ubuntu date 변경
```
sudo ln -sf /usr/share/zoneinfo/Asia/Seoul /etc/localtime
```