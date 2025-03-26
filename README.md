## Giải thích chi tiết:
### 1. Volumes:
   - `./jenkins_home:/var/jenkins_home`: Lưu trữ dữ liệu Jenkins persistent
   - `/var/run/docker.sock:/var/run/docker.sock`: Cho phép Jenkins build Docker image

### 2. Ports:
   - `8080`: Web UI Jenkins
   - `50000`: Kết nối agent

### 3. Cấu hình quan trọng:
   - `user: root`: Quyền truy cập đầy đủ
   - `privileged: true`: Cho phép Docker inside Docker
   - `restart: unless-stopped`: Tự động khởi động lại

### 4. Bước tiếp theo:
#### 1. Chạy `docker-compose up -d`
#### 2. Truy cập `http://localhost:8080`
#### 3. Cấu hình ban đầu và cài plugin Docker Pipeline

## Cài đặt Jenkins Plugins
### 1. Github
### 2. Docker

