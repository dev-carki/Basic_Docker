# Step 1: Specify the base image
# Use an official lightweight image, such as Python, for simplicity
FROM python:3.13-slim

# Step 2: Set the working directory inside the container
# This is where all commands and files will be located during build
# 시작포인트
WORKDIR /app 

# Step 3: Copy the application code into the container
# "." represents the current directory on the host, and "/app" is the container's directory
# 로컬에(현재 작업 디렉토리) 있는것을 /app에 카피함
COPY . /app

# Step 4: Install application dependencies
# Use a requirements.txt file for Python dependencies
# 플라스크 앱 -> 라이브러리 다운 필요
RUN pip install --no-cache-dir -r requirements.txt

# Step 5: Expose a port
# Inform Docker which port the application will listen on
EXPOSE 5000

# Step 6: Specify the default command to run the application
# Replace `app.py` with the name of your main Python script
# 커맨드
CMD ["python", "app.py"]

# app.py -> 뭔가 수정이 일어나면
# docker build -t my-first-docker .
# 빌드를 다시 해주고 (수정사항 반영)
# docker run -p 5001:5000 my-first-docker
# run을 해서 실행