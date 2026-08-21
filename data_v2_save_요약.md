# 데이터 요약: data_v2_save.csv

## 개요
- **주제**: 통신사 고객 이탈(Churn) 예측 데이터
- **크기**: 7,027행 × 17열
- **결측치**: 없음

## 컬럼 구성

| 구분 | 컬럼명 | 설명 |
|---|---|---|
| 고객 특성 | gender | 성별 |
| | Partner | 배우자 유무 |
| | Dependents | 부양가족 유무 |
| | tenure | 가입 개월 수 |
| 가입 서비스 | MultipleLines | 다회선 여부 |
| | InternetService | 인터넷 서비스 종류 (DSL / 광랜 / 없음) |
| | OnlineSecurity | 온라인 보안 서비스 가입 여부 |
| | OnlineBackup | 온라인 백업 서비스 가입 여부 |
| | TechSupport | 기술지원 서비스 가입 여부 |
| | StreamingTV | TV 스트리밍 서비스 가입 여부 |
| | StreamingMovies | 영화 스트리밍 서비스 가입 여부 |
| 계약/결제 | Contract | 계약 형태 (월단위 / 1년 / 2년) |
| | PaperlessBilling | 전자청구서 여부 |
| | PaymentMethod | 결제 수단 |
| | MonthlyCharges | 월 요금 |
| | TotalCharges | 누적 총 요금 |
| 목표 변수 | Churn | 이탈 여부 (0=유지, 1=이탈) |

## 핵심 분포

### 이탈률 (Churn)
- 유지(0): 73.4%
- 이탈(1): 26.6%
- 클래스 불균형이 있어 모델 평가 시 accuracy 외에 precision, recall, F1, AUC 등을 함께 확인 필요

### 계약 형태 (Contract)
| 유형 | 인원수 |
|---|---|
| 월단위 (Month-to-month) | 3,866명 |
| 2년 (Two year) | 1,690명 |
| 1년 (One year) | 1,471명 |

### 인터넷 서비스 (InternetService)
| 유형 | 인원수 |
|---|---|
| 광랜 (Fiber optic) | 3,090명 |
| DSL | 2,416명 |
| 없음 (No) | 1,521명 |

## 참고
- 흔히 쓰이는 Telco Customer Churn 데이터셋과 구조가 유사함
- 추가 분석 시 계약 형태, 인터넷 서비스 종류, tenure 등과 이탈률의 상관관계를 살펴보면 유용할 것으로 보임
