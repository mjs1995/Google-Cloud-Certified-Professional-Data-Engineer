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
- 행' 및 '열'이라는 용어를 사용하여 문제를 설명하는 경우 SQL에서 사용되므로 Cloud SQL 또는 Cloud Spanner와 같은 SQL 데이터베이스를 생각할 수 있습니다.
- 플랫 직렬화 데이터는 작업하기 쉽지만 구조가 부족하므로 의미가 없음
  - ![image](https://user-images.githubusercontent.com/47103479/220348797-6db30e16-b960-44d9-94e0-3c225e9f660d.png)
  - "쉼표로 구분된 값"을 의미하는 CSV는 테이블 형식 데이터를 저장하는 데 사용되는 간단한 파일 형식
  - "extensible markup language"를 의미하는 XML은 데이터를 저장하고 전송하도록 설계되었으며 자체 설명이 가능하도록 설계되었습니다. 
  - JSON은 "JavaScript Object Notation"을 의미하며 경량 데이터 교환 형식 기반입니다.
  - Avro : 의미 있는 구조를 가진 데이터 개체가 있는 경우 먼저 데이터를 평면화하고 직렬화하여 데이터가 0과 1이 되도록 하는 방법이 필요합니다.그런 다음 전송 및 저장이 가능합니다. 그리고 검색될 때 구조를 의미 있는 데이터 개체로 복원하기 위해 데이터를 역직렬화해야 합니다. 이를 수행하는 소프트웨어의 한 예
    - Avro는 Apache의 Hadoop 프로젝트 내에서 개발된 원격 절차 호출 및 데이터 직렬화 프레임워크입니다. JSON을 사용하여 데이터 유형 및 프로토콜을 정의하고 데이터를 압축 이진 형식으로 직렬화합니다
    - 주요 용도는 Apache Hadoop에서 영구 데이터에 대한 직렬화 형식과 Hadoop 노드 간 및 클라이언트 프로그램에서 Hadoop 서비스로의 통신을 위한 유선 형식을 모두 제공할 수 있습니다.
- BigQuery datasets, tables, and jobs
  - ![image](https://user-images.githubusercontent.com/47103479/220349196-3b240246-2440-4739-8425-511d306e6c4e.png)
  - 프로젝트는 리소스 사용을 신용 카드에 연결하는 것입니다. 리소스를 청구 가능하게 만드는 것입니다. 그런 다음 BigQuery에서 데이터 세트 내부에 저장된 데이터와 데이터 세트에는 테이블이 포함됩니다.
  - 테이블에는 열이 포함됩니다. 데이터를 처리하면 BigQuery가 작업을 생성합니다. 데이터를 사용하여 지원되는 일부 업데이트 및 유지 관리 활동이 있지만 종종 작업은 SQL 쿼리를 실행합니다.
  - ![image](https://user-images.githubusercontent.com/47103479/220349447-3e2401e5-73bc-4a45-a25c-9318d3bdf565.png)
    - BigQuery는 '열 저장소'라고 합니다. 즉, 행이 아닌 열을 처리하도록 설계되었습니다. 열 처리는 BigQuery에서 매우 저렴하고 빠르며 행 처리는 느리고 비용이 많이 듭니다. 대부분의 쿼리는 소수의 필드에서만 작동하며 BigQuery는 관련 열만 읽으면 됩니다.
- Dataflow terms and concepts: PCollection
  - ![image](https://user-images.githubusercontent.com/47103479/220350136-eaa6ec01-e0a4-474b-89d2-7eb9a82308d2.png)
  - Cloud Dataflow에 대해 알아야 할 여러 가지 개념이 있습니다. 데이터 및 데이터 흐름은 PCollection에 표시됩니다.
  - 파이프라인은 BigQuery에서 데이터를 읽고, 여러 처리를 수행하고, 출력을 클라우드 저장소에 씁니다. Dataflow에서 각 단계는 변환이며 변환 모음은 파이프라인을 만듭니다.
  - 전체 파이프라인은 "러너"라는 프로그램에 의해 실행됩니다. 개발을 위해 로컬 러너가 있습니다. 프로덕션에는 클라우드 러너가 있습니다. 파이프라인이 클라우드에서 실행될 때 각 단계는 각 변환은 PCollection에 적용되며 PCollection이 됩니다. 따라서 PCollection은 파이프라인을 통과하는 데이터 단위이며 각 단계는 탄력적으로 확장됩니다. 아이디어는 Python 또는 Java 코드를 작성하는 것입니다.
  - 확장 가능한 서버리스 컨텍스트에서 파이프라인을 실행하는 Cloud Dataflow에 배포합니다. Cloud Dataproc과 달리 클러스터를 시작하거나 클러스터를 확장할 필요가 없습니다.
- Dataflow does ingest, transform, and load on Batch or Stream 
  - ![image](https://user-images.githubusercontent.com/47103479/220352084-237dab97-676b-414f-b208-afd8b84eb5b9.png)
  - Cloud Dataflow는 일괄 처리와 스트림 처리 모두에 동일한 파이프라인, 동일한 작업, 동일한 코드를 사용하도록 설계되었습니다. 배치 데이터는 "제한된 데이터"라고도 합니다.
  - 배치 데이터에는 끝이 있습니다. 스트리밍 데이터는 "무제한 데이터"라고도 하며 동적으로 생성될 수 있습니다.
  - 필터링 및 그룹화도 지원됩니다. Cloud Dataflow를 사용하면 많은 Hadoop 워크로드를 더 쉽게 실행할 수 있고 유지 관리하기가 더 쉽습니다. 그러나 PCollection과 RDD는 동일하지 않으므로 기존 코드를 재설계하고 조정해야 합니다.

## Desing Data Pipelines
- Dataproc
  - ![image](https://user-images.githubusercontent.com/47103479/220351051-bcc0902c-930d-4474-b316-cc245748d4cc.png)
  - Cloud Dataproc은 관리형 Hadoop 서비스이며 Hadoop 생태계의 표준 소프트웨어를 포함하여 알아야 할 사항이 많이 있습니다. 
  - 클러스터 외부에 데이터를 저장하는 경우 HDFS 유형 데이터를 클라우드 스토리지에 저장하고 HBase 유형 데이터를 Cloud Bigtable에 저장하면 실제로 작업을 처리하지 않을 때 클러스터를 종료할 수 있습니다.
  - Hadoop의 두 가지 문제점 - 첫째, 다양한 종류의 작업에서 효율적으로 실행될 수 있도록 모든 설정을 조정하려고 시도하고 둘째, 활용도를 정당화하기 위해 비용을 지불하려고 합니다.
  - Cloud Dataproc은 Hadoop, Pig, Hive, Spark를 지원합니다.
  - Spark RDD pipeline operations use lazy execution
    - ![image](https://user-images.githubusercontent.com/47103479/220351650-9215228a-e82f-443f-a1e5-41364f2e7df4.png)
    - Spark는 디스크에서 복사하는 대신 메모리에서 파이프라인 처리의 일부를 수행하기 때문에 중요합니다
    - 다른 종류의 작업- 변환 및 작업. Spark는 방향성 그래프라는 추상화를 사용하여 파이프라인을 구축합니다. 각 변환은 그래프에 추가 노드를 빌드하지만 Spark는 파이프라인을 실행하지 않습니다.
    - 행동을 볼 때까지. 아주 간단하게, 스파크는 전체 스토리, 즉 모든 정보를 가질 때까지 기다립니다.
    - 파이프라인을 실행합니다. 변환을 기다리고 작업을 실행하는 프로세스를 지연 실행이라고 합니다. 변환의 경우 입력은 RDD이고 출력은 RDD입니다
- Use Dataproc to run open source software
  - ![image](https://user-images.githubusercontent.com/47103479/220352706-e1c3460a-50dd-4315-a2c1-6c41c1e9fbe8.png)
  - Cloud Dataproc에는 모든 종류의 GCP 리소스에 대한 커넥터가 있습니다.
  - GCP 소스에서 읽고 GCP 소스에 쓸 수 있으며 Cloud Dataproc을 상호 연결 접착제로 사용할 수 있습니다. 클러스터에서 Hadoop 에코시스템의 오픈 소스 소프트웨어를 실행할 수도 있습니다.
  - Kafka는 메시징 서비스이고 GCP의 대안은 Cloud Pub/Sub입니다. 
  - 오픈소스 HBase에 대한 GCP의 대안은 클라우드 빅테이블입니다. 
  - HDFS의 대안은 클라우드 스토리지

## Dataflow pipelines
- Dataflow
  - Java 또는 Python으로 파이프라인 코드를 작성할 수 있습니다. 오픈 소스 Apache Beam API를 사용하여 파이프라인을 정의하고 제출할 수 있습니다.
  - Cloud Dataflow로 전송합니다. 그러면 Cloud Dataflow가 실행 프레임워크를 제공합니다. 병렬 작업은 프레임워크에 의해 자동으로 확장되며 동일한 코드가 실시간 스트리밍 및 일괄 처리를 수행합니다
  - Cloud Dataflow의 한 가지 좋은 점 - 많은 소스에서 입력을 받고 많은 동기화에 출력을 작성할 수 있지만 그 사이의 파이프라인 코드는 동일하게 유지됩니다
  - Cloud Dataflow의 보안은 클라우드에 대한 액세스를 제한하는 역할 할당을 기반으로 합니다.
- ![image](https://user-images.githubusercontent.com/47103479/220353579-922ff5f5-3ab6-4adc-a556-5224b5be2fb0.png)
  - Dataflow 파이프라인은 코드에만 표시되는 것이 아닙니다.GCP 콘솔에 다이어그램으로 표시됩니다
  - 파이프라인은 데이터 처리 솔루션의 진행 상황과 단계 구성을 보여주므로 다른 코드 솔루션보다 훨씬 쉽게 유지 관리할 수 있습니다.
  - 파이프라인의 각 단계는 필터, 그룹화, 변환, 비교, 조인 등을 수행합니다. 변환은 병렬로 수행할 수 있습니다
- Dataflow operations
  - ![image](https://user-images.githubusercontent.com/47103479/220353839-d9578579-a5fe-4f78-aa9a-863553abfbb3.png)
  - GroupByKey는 빅 데이터의 리소스를 사용할 수 있습니다. 이것이 샘플 데이터에서 파이프라인을 몇 번 테스트하여 프로덕션 규모로 실행하기 전에 확장 방법을 알고 있는지 확인하십시오


## BigQuery and Dataflow solutions
- BigQuery
  - ![image](https://user-images.githubusercontent.com/47103479/220365209-ecae27e3-a777-4768-8d92-c654327be117.png)
  - BigQuery는 분석을 수행하는 프런트 엔드 서비스와 스토리지를 수행하는 백엔드 서비스의 두 가지 서비스입니다. 
  - 방대한 데이터 세트에 대한 거의 실시간 분석을 제공합니다. 데이터 스토리지는 내구성이 있고 저렴하며,다양한 데이터 세트를 연결하고 작업하여 새로운 통찰력과 비즈니스 가치를 도출할 수 있습니다. BigQuery는 쿼리에 SQL을 사용하므로 많은 데이터 분석가가 즉시 사용할 수 있습니다.
  - BigQuery는 유연한 수집을 위해 많은 서비스에 연결합니다. 효율성을 위한 중첩 및 반복 필드와 확장성을 위한 사용자 정의 함수를 지원합니다.
  - 스토리지 및 데이터베이스에서 별도의 컴퓨팅 및 처리를 통해 서버리스 운영이 가능합니다.
- BigQuery solutions
  - ![image](https://user-images.githubusercontent.com/47103479/220365572-26437397-6ec7-4b36-abf1-0b0322ff8c29.png)
  - BigQuery에는 콘솔과 BQ의 명령줄에서 사용할 수 있는 자체 분석 SQL 쿼리 프런트 엔드가 있습니다. 그것은 단지 쿼리 엔진입니다. 
  - BigQuery의 백엔드 데이터 웨어하우스 부분 테이블에 데이터를 저장합니다.
  - BigQuery에는 클라우드 스토리지에 대한 커넥터도 있습니다. 이것은 일반적으로 CSV 파일로 직접 작업하는 데 사용됩니다. BigQuery에는 Cloud Bigtable에 대한 커넥터도 있습니다
  - 데이터를 처리할 로컬에 저장하는 것보다 거의 빠르고 경우에 따라 더 빠를 수 있습니다. 즉, 네트워크는 Hadoop과 HDFS의 개념을 거꾸로 뒤집습니다. 처리 리소스와 별도로 데이터를 저장하는 것이 다시 한 번 더 효율적입니다
  - ![image](https://user-images.githubusercontent.com/47103479/220366278-1b361f45-5b59-4d85-afeb-89edf50f4a4a.png)
    - Cloud Dataproc 및 Cloud Data Flow에서 클라우드 스토리지에서 별도의 파일을 CSV 파일로 출력할 수 있습니다. 즉, 데이터를 병렬로 처리하고 결과를 별도의 작은 파일에 기록하는 분산된 노드 또는 서버 세트를 가질 수 있습니다.이것은 나중에 조합하기 위해 분산된 결과를 축적하는 쉬운 방법입니다. 
    - 모든 데이터 처리 서비스에서 모든 스토리지 서비스에 액세스합니다. Cloud Data Flow는 BigQuery를 위한 탁월한 ETL 솔루션입니다.

## Design data processing infrastructure
- Data ingest solutions: CLI, web UI, or API
  - ![image](https://user-images.githubusercontent.com/47103479/220366598-adece2b5-9e10-4197-8ddd-d478d4500616.png)
  - gsutil 명령줄 도구를 사용하여 Cloud Storage에 파일을 로드할 수 있습니다.
  - BigQuery 명령줄 도구인 bq는 대용량 데이터 파일을 업로드하는 데 적합합니다. 데이터 파일 업로드 예약을 위해. 명령을 사용하여 테이블을 만들고, 스키마를 찾고, 데이터를 로드하고, 쿼리를 실행할 수 있습니다. bq 명령어는 Compute Engine 인스턴스에서 사용할 수 있습니다.
  - Cloud Shell에 설치하거나 Google Cloud 소프트웨어 개발 키트(SDK)의 일부로 모든 클라이언트 시스템에 설치할 수 있습니다. GCP 콘솔에서 BigQuery로 데이터를 로드할 수 있습니다.
- Three ways of loading data into BigQuery 
  - ![image](https://user-images.githubusercontent.com/47103479/220366923-62a55d88-c690-4bff-8cfd-463657ba5d34.png)
  - Cloud Dataflow 및 Cloud Logging에서 데이터를 스트리밍하거나 프로그램에서 사후 호출을 사용할 수 있습니다. 그리고 BigQuery가 CSV 및 JSON 형식 파일을 자동으로 감지할 수 있어 매우 편리합니다
- Options for trnasferring storage
  - ![image](https://user-images.githubusercontent.com/47103479/220367178-d65d37cf-31b0-4e00-8db1-592e19277f43.png)
  - 데이터를 수집하기 위해. 간단히 말해서 파일 업로드에는 gsutil을 사용하고, 데이터가 다른 클라우드와 같은 다른 위치에 있을 때는 스토리지 전송 서비스를 사용하고, 데이터가 너무 많을 때는 Transfer Appliance를 사용합니다.

## Pub/Sub solutions 
- Pub/Sub
  - ![image](https://user-images.githubusercontent.com/47103479/220369849-51fe25ee-cac5-4929-bf62-65f921cc87f3.png)
  - Cloud Pub/Sub 메시지 브로커는 완전한 수집 솔루션을 지원합니다. 시스템 간의 느슨한 결합과 시스템 간의 수명이 긴 연결을 제공합니다.
  - Cloud Pub/Sub가 메시지를 보유하는 기간은 최대 7일입니다.
- common appliactions of Pub/Sub
  - ![image](https://user-images.githubusercontent.com/47103479/220370100-8b83fae9-ebcc-4232-b42e-2a3df2f942dc.png)
  - Cloud Pub/Sub는 메시징 인프라를 통해 애플리케이션과 서비스를 연결합니다.
  - Pub/Sub는 동기식 지점 간 연결을 단일 고가용성 비동기식 버스로 대체하여 이벤트 배포를 간소화합니다.
  - Pub/Sub를 사용하면 트래픽 급증에 대한 과잉 프로비저닝을 방지할 수 있습니다.
  - 클라우드 데이터 흐름과 함께 Cloud Pub/Sub를 사용하면 정확히 한 번에 순서대로 처리할 수 있습니다.
  - Cloud Pub/Sub는 정확히 한 번 전송을 처리합니다.
  - 클라우드 데이터 흐름은 중복 제거, 순서 지정 및 기간 설정을 처리합니다
  - 업무 분리는 경쟁 메시징 시스템의 병목 현상을 능가하는 확장 가능한 솔루션을 가능하게 합니다.
- Serverless analytics solution
  - ![image](https://user-images.githubusercontent.com/47103479/220370364-1ff2421b-23b4-4655-ac92-3c462dfcb128.png)
  - 데이터 수집을 위한 Cloud Pub/Sub, 데이터 처리 및 ETL을 위한 클라우드 데이터 흐름, 대화형 분석을 위한 BigQuery.
- Data analytics solution
  - ![image](https://user-images.githubusercontent.com/47103479/220370550-146ed99d-2f1a-4ed6-8927-22dfc7f637e1.png)

## Practice exam
- ![image](https://user-images.githubusercontent.com/47103479/220370773-d215814b-5a3c-44b8-ad73-8c303f02919a.png)
  - 정답은 B입니다. BigQuery를 사용하세요. 
  - 스토리지 솔루션용 및 처리 솔루션용 Cloud Dataproc. 질문에 Apache Spark 코드를 재사용할 계획이 필요하기 때문에 Cloud Dataproc이 맞습니다. CSV 파일은 클라우드 저장소에 있을 수 있습니다.
- ![image](https://user-images.githubusercontent.com/47103479/220371126-851a904d-f934-4fde-9697-00394494f527.png)
  - 답은 A, 입력용 클라우드 Pub/Sub이고 게시자에서 타임스탬프를 첨부합니다.
  - Apache Kafka를 설정하고 유지 관리해야 하므로 이 시나리오에서 Apache Kafka가 권장되는 솔루션이 아니라는 것을 알 수 있습니다
  - 솔루션의 나머지 부분을 구현하려면 타임스탬프가 필요하므로 게시자에서 수집 시 타임스탬프를 적용하는 것이 좋습니다.
