# Docker

[1. Tổng quan về docker](#docker_overview)

[2. Docker file](#docker_file)

<a name = "docker_overview"></a>
## 1. Tổng quan về docker 

### Docker image

* **Pull *docker image* từ *docker hub***

```
docker pull image_name
```
* **List các images** 

```
docker images 
```
* **Xóa image** 

```
docker rmi image_id
```
* ***Note:*** Không xóa được image mà container tương tứng với nó vẫn đang hoạt động. Do đó, trước khi xóa image đó, ta cần xóa container trước.
   - **List container up** 
   ```
   docker ps
   ```
   - **Remove container** 
   ```
   docker rm --force container_id
   or
   docker rm -f container_id
   ```
* **Tạo containers từ images** (1 image => 1 or nhiều containers)
```
docker run -d container_name 
```

* **Tắt container** 

```
docker stop container_id 
```
* **Bật container** 

```
docker start container_id
```
* **Docker volume**
```
-v host_volumne: container_volume
```
* **Detach container**

```
Ctrl + p, Ctrl + q
```
* **Attach container**

```
docker attach container_id
```
<a name = "docker_file"></a>
## 2. Docker file

* Là file dạng text, không có đuôi, giúp thiết lập cấu trúc cho *docker image* nhờ chứa một tập hợp các câu lệnh.
* Do đó, *docker file* quy định *docker image* khởi tạo từ đâu và chứa những gì trong đó.

![docker_file_1](https://user-images.githubusercontent.com/63502091/163532464-ea02a772-ad9e-45dd-9b5f-51da68000c8c.png)


