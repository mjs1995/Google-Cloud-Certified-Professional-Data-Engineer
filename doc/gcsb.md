# Understanding the Professional Data Engineer Certification
- 데이터 엔지니어는 다양한 옵션이 솔루션 운영 및 유지 관리 방식을 어떻게 변경하는지에 더 많이 알아야 함 
- exam guide : https://cloud.google.com/certification/guides/data-engineer/

# Designing data processing systems
## Desing and building 
- Data processing anatomy
  - ![image](https://user-images.githubusercontent.com/47103479/220125000-a4d076e1-ec14-49e3-b93f-3e3e28d7d9ae.png)
- 데이터 엔지니어링 플랫폼  
  - ![image](https://user-images.githubusercontent.com/47103479/220126210-03b17ccd-08e2-41a1-8d9c-2a751351ebd3.png)
  - Integrated services : 일반 응용프로그램이 아닌 데이터 처리를 위해 설계된 프레임워크에서 격리된 서버 데이터베이스 솔루션보다 효율적이고 유연함 
    - Storage and databases : 데이터 저장 및 검색을 가능하게 하는 서비스, 특정 사용 사례에 대해 보다 효율적으로 만드는 다양한 저장 및 검색 방법. 
      - ![image](https://user-images.githubusercontent.com/47103479/220126278-eead3437-abd9-4be5-930e-57a7aa7af6a3.png)
      - Cloud SQL 데이터베이스는 일관된 개별 트랜잭션을 저장하는 데 매우 적합하지만 대량의 비정형 데이터를 저장하는 데는 최적화되어 있지 않습니다.
      - 데이터베이스 서비스는 액세스 방법의 컨텍스트 내에서 데이터에 대해 최소한의 작업을 수행합니다. SQL 쿼리는 검색 쿼리의 결과를 집계, 누적, 계산 및 요약할 수 있습니다.
      - Cloud Firestore는 NoSQL 문서 데이터베이스입니다.자동 스케일링을 위해 제작되었습니다. 고성능과 손쉬운 애플리케이션 개발을 제공하며 Datastore 호환성 모드를 포함합니다
    - Server-based procssing : 서비스 애플리케이션 코드와 소프트웨어를 실행하여 저장된 데이터를 사용하여 결과를 생성하는 작업, 조치 및 변환을 수행할 수 있습니다
  - Artificial intelligence
    - ![image](https://user-images.githubusercontent.com/47103479/220127661-9369cbb4-f2e8-4659-8942-cebd9a52a9e4.png)
    - Pre-and post- processing services : 데이터 정리 또는 처리 후와 같은 처리 전 데이터 및 파이프라인 작업, 데이터 시각화와 같은 사전 및 사후 처리는 데이터 처리 솔루션의 중요한 부분입니다
      - ![image](https://user-images.githubusercontent.com/47103479/220127809-2d7cb5e4-3357-4b8e-9c7e-d46bb84275fd.png)
      - Cloud Data Studio는 데이터 시각화에 사용됩니다.
      - Cloud Data Prep은 데이터를 준비 또는 조정하고 데이터를 처리하기 전에 파이프라인을 준비하는 데 사용됩니다. 
      - Cloud Data Lab은 코드를 보관하고 실행하는 독립적인 작업 공간인 노트북입니다.코드를 작성하고 결과를 표시합니다. 
      - Dialogflow는 챗봇을 만드는 서비스입니다. AI를 사용하여 인간과 데이터의 직접적인 상호 작용 방법을 제공합니다
    - infrastructure services :  데이터 처리 및 IT 요소를 연결하고 통합하는 모든 프레임워크 서비스로 완전한 솔루션, 메시징 시스템, 데이터 가져오기, 내보내기, 보안 모니터링 등으로 변환합니다
      - ![image](https://user-images.githubusercontent.com/47103479/220128078-7385038c-0cf3-448d-8436-01638b7e1eb0.png)
      - Cloud Pub/Sub는 최대 7개의 메시지를 보관할 수 있습니다.
      - 메시징 서비스인 Cloud Pub/Sub는 데이터 수집에서 데이터 도착을 분리하기 때문에 거의 모든 라이브 또는 스트리밍 데이터 솔루션의 기능입니다. 
      - Cloud VPN, 파트너 상호 연결 또는 전용 상호 연결 클라우드의 서비스로 전송해야 하는 온프레미스 데이터가 있을 때마다 역할을 수행합니다. 
      - Cloud IAM, 방화벽 규칙 및 키 관리는 상태와 같은 일부 업종에 매우 중요합니다.
      - 모든 솔루션을 모니터링하고 관리해야 하며 일반적으로 Cloud Console에 표시되는 패널과 스태프 드라이버 모니터링으로 전송되는 데이터가 포함됩니다
- Processing
  - ![image](https://user-images.githubusercontent.com/47103479/220127099-099671cc-2558-486b-a43b-4f71e8672968.png)
- Data processing services 
  - ![image](https://user-images.githubusercontent.com/47103479/220127213-cd99b858-b06f-4362-a982-e3b7cd6d5627.png)
  - 데이터 처리 서비스는 스토리지와 컴퓨팅을 결합하고 데이터 처리의 스토리지 및 컴퓨팅 측면을 자동화합니다
  - Cloud Dataproc에서 Spark의 데이터 추상화는 RDD(Resilient Distributed Data set)이고 처리 추상화는 DAG(Directed Acyclic Graph)입니다.

## Design flexible data representations 
- 
