# Docker

## Virtual Machine 이란?

![image](https://user-images.githubusercontent.com/52827441/91009459-96661780-e61b-11ea-8eb3-963a177cb347.png)

### Virtual Machine 의 장점

- Hypervisor 를 사용해 하나의 서버를 여러개의 가상 하드웨어 (CPU, RAM, HDD(SSD), Network Interface Card 등의 그룹) <sub>실제로는 여러개의 할당량으로 나눈다고 보면 된다.</sub> 로 나누어 운영할 수 있다.
- 나눠진 VM 은 다른 Server 로 쉽게 옮겨 사용할 수 있다. (서버가 고장났을 때 다른 서버로 VM 을 옮겨 app 을 실행할 수 있다.)

### Virtual Machine 의 문제점

- <mark>모든 Virtual Machine 은 OS 가 필요하다. OS 는 많은 Resource 를 사용한다.</mark>

## Container 란?

![image](https://user-images.githubusercontent.com/52827441/91010613-c3b3c500-e61d-11ea-81bc-9ffca4ba1c95.png)

하나의 물리적 Server 에 의존하고 있는 하나의 OS 위에 다양한 Container 들을 사용할 수 있다.

### Container 의 장점

- 각각의 Container 들은 독립적이다. 즉 Container 들끼리 서로의 존재를 알지 못한다.
- Container 는 Code, Setting, Dependency 등 App 을 실행하는데 필요한 모든 것을 포함하고 있다.
- Container 는 OS 를 포함하고 있지 않기 때문에 시작이 매우 빠르다.
- Container 는 가지고 있는 App 을 실행하는데 필요한 memory 만을 필요로 하므로 resource 사용에 매우 효율적이다.

### 대표적인 Container Management System

- [Docker](https://www.docker.com/)
- [Kubernetes](https://kubernetes.io/ko/docs/home/)

> 둘 다 Go 언어로 이루어짐
