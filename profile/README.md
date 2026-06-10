<div align="center">

<table>
  <tr>
    <td align="center">
      <img width="650" src="https://github.com/user-attachments/assets/9399d6c8-9de4-49f4-a770-85e73dd8cdd7" />
    </td>
    <td align="center">
      <img width="650" src="https://github.com/user-attachments/assets/ce87c46c-2b6e-4782-bdec-b2026e2aa1e3" />
    </td>
  </tr>
</table>

</div>

배포링크 : www.dealit.site


<p align=center>
  <a href="https://vivacious-asp-af5.notion.site/2dd02d41af3480f5b26ce06e11f5c00b?source=copy_link">팀 노션</a>
  &nbsp; | &nbsp; 
  <a href="https://www.youtube.com/watch?v=CkGmaPMyGKs">시연 영상</a>
  &nbsp;
</p>



## Main Repositories

| Repository | Description |
|---|---|
| [Dealit](https://github.com/Dealit-2026) | 프로젝트 소개 및 문서 |
| [Backend](https://github.com/Dealit-2026/backend) | Spring Boot Backend |
| [Frontend](https://github.com/Dealit-2026/frontend) | Frontend Client |
| [AI](https://github.com/Dealit-2026/ai-server) | AI Recommendation Server |



# 프로젝트 개요


Dealit은 AI 기반 실시간 중고거래 경매 플랫폼입니다.
사용자는 일반 중고거래 방식에서 발생하는 가격 책정의 어려움을 줄이기 위해 AI 가격 추천 기능을 활용할 수 있으며, 실시간 경매 시스템을 통해 시장 반응 기반의 합리적인 거래 가격을 형성할 수 있습니다.

또한 Redis Lua Script 기반 원자적 입찰 처리 구조와 SSE(Server-Sent Events) 기반 실시간 알림 시스템을 적용하여 동시 입찰 환경에서도 안정적인 경매 정합성을 보장하도록 설계하였습니다.

AI 추천, 실시간 경매, 검색 및 배포 인프라를 하나의 서비스 흐름으로 통합하여 실제 서비스 환경과 유사한 구조를 목표로 개발하였습니다.



# 핵심 기능

## AI 기반 상품 분석 및 가격 추천

* Gemini API 기반 AI 모델을 활용하여 상품 카테고리 및 예상 가격 추천
* 사용자 입력 데이터를 기반으로 상품 등록 편의성 향상
* FastAPI 기반 AI 서버와 Spring Boot 백엔드 연동

<p align="center">
  <img src="https://github.com/user-attachments/assets/872f3584-86a4-4f71-bf65-da0eaf426908" width="220"/>
  <img src="https://github.com/user-attachments/assets/e7e3d2b7-f260-4450-8b38-e3abb7b0f0bd" width="220"/>
</p>

## 실시간 경매 시스템

* SSE(Server-Sent Events)를 활용한 실시간 입찰 상태 반영
* 최고 입찰가 및 경매 상태를 실시간으로 사용자에게 전파
* Redis Pub/Sub 기반 이벤트 처리 구조 적용
<p align="center">
  <img src="https://github.com/user-attachments/assets/12586534-ac4b-4214-8a54-107ad242c91f" height="400"/>
  <img src="https://github.com/user-attachments/assets/541804e4-d6ef-4ef2-8b89-73d4a0fc9f5b" height="400"/>
  <img src="https://github.com/user-attachments/assets/36e9a6ef-1890-45bb-833b-bc11445567a1" height="400"/>
</p>

## Redis Lua Script 기반 동시성 제어

* Redis Hash에 경매 상태를 저장하여 실시간 입찰 판단 처리
* Lua Script를 통해 입찰 검증 및 최고가 갱신을 원자적으로 수행
* 동시 입찰 상황에서도 데이터 정합성 보장

<p align="center">
  <img src="https://github.com/user-attachments/assets/dbb196dd-d4b7-4201-a603-ea2b083bd8c9" width="180"/>
  <img src="https://github.com/user-attachments/assets/bfd4adfb-a005-4918-8850-3ed571da832b" width="180"/>
  <img src="https://github.com/user-attachments/assets/bed72f68-3ee2-45ec-ab62-c88ed3e8894d" width="180"/>
  <img src="https://github.com/user-attachments/assets/80f607db-e9c9-4350-b996-51751fd0d226" width="180"/>
</p>


## 검색 기능

* OpenSearch 기반 상품 검색 기능 구현
* 상품명 및 키워드 기반 검색 지원
* 검색 성능 향상을 위한 검색 엔진 분리 구조 적용

<p align="center">
  <img src="https://github.com/user-attachments/assets/740c3db2-e2c7-4de8-b1b6-02e3162690b3" width="180"/>
  <img src="https://github.com/user-attachments/assets/8c9fce45-aaa2-471e-9789-13ff9888043d" width="180"/>
</p>


## 결제 및 예치금 시스템

* 입찰 예치금 및 거래 금액 관리 기능 구현
* 경매 종료 후 자동 정산 및 환불 처리 구조 설계
* 트랜잭션 분리를 통한 안정적인 결제 흐름 관리

<p align="center">

<img src="https://github.com/user-attachments/assets/bf3984e3-0982-4b5f-adbd-61cc4ef53771" width="190" height="388"/>
<img src="https://github.com/user-attachments/assets/993a44fa-1763-4140-b927-054975d24d09" width="190" height="388"/>
<img src="https://github.com/user-attachments/assets/a4f34e62-7ae5-4793-80f5-7a4680504a75" width="190" height="388"/>
<img src="https://github.com/user-attachments/assets/d84ff7d6-8fe1-4a76-9f28-dd9bb0c73c73" width="190" height="388"/>
</p>


## 배포 및 운영 환경 구축

* AWS EC2 기반 서비스 배포
* Docker 및 Docker Compose 기반 컨테이너 환경 구성
* NGINX Reverse Proxy 및 HTTPS 환경 적용
* GitHub Actions 기반 CI/CD 자동 배포 구축

---

# 기술적 도전🧐

## 1. 실시간 경매 기능 구현

<img width="1280" height="720" alt="KakaoTalk_20260610_125158625" src="https://github.com/user-attachments/assets/6d0867c6-b36c-4153-a810-f18a0a32f106" />

* 실시간 경매 환경에서 동시에 여러 사용자가 입찰할 경우 현재가 조회, 입찰 금액 검증, 최고입찰자 갱신 과정 사이에 다른 요청이 개입하며 레이스 컨디션이 발생할 수 있었습니다.
* 초기에는 DB 비관적 락으로만 설계를 해야하나 했지만, 입찰 요청이 몰리는 상황에서 락 점유 시간이 길어지고 응답 지연이 발생할 가능성이 있다고 판단하였습니다.
* 이를 해결하기 위해 Redis Hash 기반으로 실시간 입찰 상태를 관리하고, Redis Lua Script를 활용해 종료 여부 확인, 최소 입찰 금액 검증, 최고 입찰자 갱신 과정을 원자적으로 처리하도록 설계하였습니다.
* 이를 통해 현재가 검증과 최고입찰자 갱신 사이에 다른 요청이 개입하지 못하도록 하여 실시간 입찰 상태의 정합성을 안정적으로 보장할 수 있었습니다.

## 2. OpenSearch 인덱싱 지연으로 인한 상품 수정 API 응답 저하 개선

정상상태
<p align="center">
  <img src="https://github.com/user-attachments/assets/3f460653-c551-44f7-980a-f35297117e0e" width="600"/>
</p>

OpenSearch 1s 지연상태 + 동기 처리
<p align="center">
  <img src="https://github.com/user-attachments/assets/1677e205-df43-476e-8891-1df589f309ce" width="600"/>
</p>


OpenSearch 1s 지연상태 + 비동기 처리
<p align="center">
  <img src="https://github.com/user-attachments/assets/c88b6762-7972-4351-bddc-d56ba1e5eda0" width="600"/>
</p>


* 상품명, 설명, 카테고리 등 검색 대상 데이터가 수정될 경우 PostgreSQL 원본 데이터와 함께 OpenSearch 검색 인덱스도 함께 갱신하고 있었습니다.
* 기존 구조에서는 OpenSearch index/delete 요청이 상품 수정 API 요청 흐름 내부에서 동기적으로 처리되고 있어, OpenSearch 지연이 사용자 응답 시간에 직접 영향을 주는 문제가 있었습니다.
* 실제로 OpenSearch 인덱싱에 지연이 발생하면 상품 수정 자체는 완료되었음에도 사용자는 API 응답이 늦어지는 현상을 경험할 수 있었습니다.
* 이를 해결하기 위해 Spring Event 기반 비동기 이벤트 처리 구조를 적용하여 상품 수정 트랜잭션과 OpenSearch 인덱싱 작업을 분리하였습니다.
* k6 부하 테스트 결과, OpenSearch 인덱싱에 1초 지연을 주입한 환경에서 상품 수정 API의 p95 응답 시간을 약 5.37초 → 59.6ms초 수준으로 개선하며 약 98.9%의 성능 개선을 확인하였습니다.

---

# 시스템 구조도

<img width="2440" height="1120" alt="image" src="https://github.com/user-attachments/assets/c19d6429-4cee-47e6-816c-477b19cd0be6" />

