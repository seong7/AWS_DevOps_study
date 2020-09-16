## AWS Basics

### AWS 계정

- Root User

  - 회원가입한 email 계정
  - 해당 계정에 대한 모든 권한을 가지고 있다.
  - 해당 계정의 권한을 제한하기는 너무 어렵다.
  - AWS 에서는 Every day use 에서 해당 계정 사용을 권장하지 않는다.
  - "Billing" Service 에 접근할 수 있는 유일한 계정이다.

- IAM (Identity and Access Manager)

  - 직원 한명 한명 또는 서비스 하나 하나에 해당하는 계정
  - IAM Policy 라는 document 를 사용해 해당 계정의 권한을 설정할 수 있다.

    - **one IAM Policy** for **one IAM Group**  
      IAM 계정 하나하나에 해당하는 Policy 를 관리하기는 복잡할 수 있다.  
      여러 IAM 계정을 하나의 Collection 으로 묶어 Policy 를 설정할 수 있다.

    - **IAM Role**  
      권한 위임에 사용된다.  
      예) AWS EC2 에 role 을 적용하고 해당 계정이 AWS 의 다른 서비스를 이용하도록 설정 가능  
      **=> 앞으로 더 자세히 다룰 예정**

    - IAM ID 만들어 보기  
      **IAM ID :** dct-beginners / **Name :** Seongjin

### Authentication 방법 (Access 방법)

1. Programmatic 방법: Access Key 를 사용해 API 에 접속 (Code 나 console 에서 사용 가능)

2. AWS Management Console 방식

### Billing Alarm 설정하기

[> 강의 링크](https://www.udemy.com/course/introduction-to-cloud-computing-on-amazon-aws-for-beginners/learn/lecture/21190052#overview)

### AWS Public and Pravate Services

![image](https://user-images.githubusercontent.com/52827441/93058751-c0ef4180-f6aa-11ea-951b-a580497016e3.png)

어떤 서비스가 Public 이고 Private 인지 살펴 보기

- Public services 는 public IP address 또는 endpoint 를 갖는다.

- Private services 는 public IP address 들을 가질 수도 있지만 여전히 **VPC** (Virtual Private Cloud) 에 존재한다.

> - VPC : resource 를 launch 할 수 있는 가상 공간 (각 Region 당 하나씩 가질 수 있다.)
> - Availability Zone : 하나의 물리적 Data center 라고 보면 된다.
> - Subnet : Availability Zone 에 존재하는 공간 (EC2 와 같은 서버를 배포할 수 있는 공간)
> - Route Table : 하나의 VPC 내에서 각 Subnet 의 주소를 저장하고 통신을 담당
