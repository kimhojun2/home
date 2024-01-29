# 기존에 사용하던 이미지를 베이스 이미지로 지정
FROM gimojuni/django_image

# Gunicorn 설치
# 작업 디렉토리 설정
WORKDIR /app

# 의존성 설치
COPY requirements.txt .
RUN pip install -r requirements.txt

# 소스 코드 복사
COPY . .

# Gunicorn 실행 명령어
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "tsetpjt.wsgi:app"]