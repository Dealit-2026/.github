

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
  <a href="https://bow-snail-89d.notion.site/d913942c81e343339927bc654bb0b158?pvs=4](https://www.notion.so/2dd02d41af3480f5b26ce06e11f5c00b?source=copy_link">팀 노션</a>
  &nbsp; | &nbsp; 
  <a href="https://www.youtube.com/watch?v=CkGmaPMyGKs">시연 영상</a>
  &nbsp;
</p>



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

## 실시간 경매 시스템

* SSE(Server-Sent Events)를 활용한 실시간 입찰 상태 반영
* 최고 입찰가 및 경매 상태를 실시간으로 사용자에게 전파
* Redis Pub/Sub 기반 이벤트 처리 구조 적용

## Redis Lua Script 기반 동시성 제어

* Redis Hash에 경매 상태를 저장하여 실시간 입찰 판단 처리
* Lua Script를 통해 입찰 검증 및 최고가 갱신을 원자적으로 수행
* 동시 입찰 상황에서도 데이터 정합성 보장

## 검색 기능

* OpenSearch 기반 상품 검색 기능 구현
* 상품명 및 키워드 기반 검색 지원
* 검색 성능 향상을 위한 검색 엔진 분리 구조 적용

## 결제 및 예치금 시스템

* 입찰 예치금 및 거래 금액 관리 기능 구현
* 경매 종료 후 자동 정산 및 환불 처리 구조 설계
* 트랜잭션 분리를 통한 안정적인 결제 흐름 관리

## 배포 및 운영 환경 구축

* AWS EC2 기반 서비스 배포
* Docker 및 Docker Compose 기반 컨테이너 환경 구성
* NGINX Reverse Proxy 및 HTTPS 환경 적용
* GitHub Actions 기반 CI/CD 자동 배포 구축

---

# 기술적 도전


---

# 시스템 구조도

<img width="2440" height="1120" alt="image" src="https://github.com/user-attachments/assets/c19d6429-4cee-47e6-816c-477b19cd0be6" />

