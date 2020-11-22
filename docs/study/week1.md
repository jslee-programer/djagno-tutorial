# 1주차 (11월 17일~11월 22일)

## 11월 17일

### Python 설치

- Python 을 설치하기 전 라이브러리 다운로드
```bash
sudo apt-get install build-essential checkinstall
sudo apt-get install libreadline-gplv2-dev libncursesw5-dev libssl-dev
sudo apt-get install -y openssl
sudo apt-get install -y libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev libffi-dev zlib1g-dev
```
***openssl** 은 꼭 설치하자*

- 기본적인 라이브러리를 세팅한 다음 Python 을 설치하자.
``` bash
wget https://www.python.org/ftp/python/3.8.5/Python-3.8.5.tgz
tar xzf Python-3.8.5.tgz
cd Python-3.8.5
sudo ./configure --enable-optimizations
sudo make altinstall
```

- 설치 후에 설치한 Python 을 기본으로 설정하자
```bash
sudo update-alternatives --install /usr/bin/python python /usr/local/bin/python3.8 1
sudo update-alternatives --config python
```

## 11월 18일

### Interpreter 설정

- 가상환경 생성하기
```bash
python -m venv 경로
```

- 가상환경 생성 후 `interpreter` path 를 생성한 가상환경으로 설정한다.

- 후에 가상환경을 실행한다
```bash
source 가상환경/bin/activate
```

## 11월 19일

### start app polls

- polls 앱 생성하기
```
python manage.py startapp polls
```

## 11월 22일

### models.py

- migrate 실행
```bash
python manage.py migrate
python manage.py makemigrations polls
python manage.py sqlmigrate polls 0001
```

- shell 을 실행하여 models 조작하기

``` bash
python manage.py shell -i ipython
```

- 관리자 생성하기

```bash
python manage.py createsupreuser
```



