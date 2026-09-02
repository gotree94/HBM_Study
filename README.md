# 차세대 HBM Roadmap (2025~2040) 기술 발표회
# KAIST TERALAB 세미나 정리

> **발표자**: 김정호 KAIST 전기및전자공학부 교수 (KAIST TERALAB, 'HBM의 아버지')
> **일시**: 2025년 6월 11일, 온라인 생중계
> **주제**: 차세대 HBM Roadmap (2025~2040) Ver. 1.7
> **영상**:
> - Session 1: Overview of HBM Roadmap (https://www.youtube.com/watch?v=Lm6Xd5YqhgQ)
> - Session 2: HBM4 ~ HBM5 (https://www.youtube.com/watch?v=DeZSJK5iV2Q)

---

## 1. 세미나 개요 및 핵심 테마

### 1.1 핵심 메시지

> **"HBM은 열과 전기 에너지와의 싸움이며, 2038년경 AI 컴퓨팅의 중심이 될 것"** — 김정호 교수

- HBM은 3년마다 대역폭이 2배 이상 개선되는 **'AI 스케일링 법칙'**이 적용됨
- 패키징·냉각 기술이 미래 HBM의 핵심 경쟁력을 가르는 요소
- HBM의 발전 방향: **대역폭 확대 · 용량 증대 · 레이턴시 감소 · 전력 효율 개선**
- 핵심 패러다임: **'HBM의 컴퓨팅 중심화'** — CPU/GPU/HBM이 HBM 중심으로 패키징

### 1.2 HBM의 발전 방향 (1) — 성능·용량

- **높은 대역폭**: 더 많은 인터커넥트, 더 높은 Gbps/라인, 더 많은 TSV, 하이브리드 본딩, 네로우 피치
- **높은 메모리 용량**: LPDDR-HBM, HBF(High Bandwidth Flash) 통합, 계층적 메모리 아키텍처, CXL 메모리 네트워크
- **HBM 내 컴퓨팅**: 니어 메모리 컴퓨팅(NMC), 스트리밍 멀티프로세서, 데이터 압축, 오류 정정

### 1.3 HBM의 발전 방향 (2) — 구조·냉각

- **3D 집적**: 적층 캐시(Stacked Cache), 액티브/임베디드 인터포저, 하이브리드 인터포저(Si/Glass)
- **혁신적 냉각 아키텍처**: 액체 냉각, 액침 냉각(Immersion), 임베디드 쿨링
- **HBM 센트릭 컴퓨팅**: 풀 3D 집적, CPU·GPU·HBM·HBF 통합, 명령어셋·프로그래밍

---

## 2. 세대별 HBM 로드맵

| 세대 | 출시 | I/O 수 | 대역폭 | 적층/용량 | 핵심 특징 |
|------|------|--------|--------|-----------|-----------|
| **HBM4** | 2026 | 2,048 | 2 TB/s | 16-Hi | 커스텀 베이스다이, LPDDR 통합, 일부 GPU 연산 이전 |
| **HBM5** | 2029 | 4,096 | 4.0 TB/s | 16-Hi, 40Gb/die | 3D 이종집적, 3D NMC, 이멀전 쿨링, 캐시 적층 |
| **HBM6** | 2032 | - | - | - | 멀티타워 HBM, 액티브/하이브리드 인터포저 |
| **HBM7** | 2035 | 8,192 | 24 TB/s | 20/24-Hi, 64Gb/die | 하이브리드 HBM(HBM-HBF, 3D LPDDR), 임베디드 쿨링 |
| **HBM8** | 2038 | 16,384 | 64 TB/s | 최대 24단 | 풀 3D HBM 아키텍처, 양면 인터포저 |

### 2.1 세대별 기술 상세

#### HBM5 (2029) 전기 사양
| 항목 | 수치 |
|------|------|
| 데이터 레이트 | 8 Gbps |
| I/O 수 | 4,096개 |
| 총 대역폭 | 4.0 TB/s |
| 적층수 | 16-Hi |
| 용량/다이 | 40 Gb |

#### HBM5 핵심 기술
- **패키징/냉각**: Microbump(MR-MUF), 이멀전 쿨링, Thermal Via(TTV), 서멀 본딩, 베이스다이 온도센서
- **아키텍처**: 3D NMC-HBM + 스택 캐시/디캡 전용 다이, LPDDR + CXL 베이스다이 통합, 비대칭 분산 TSV/TPV/PGV/TTV 배열, Thermal Cu-Cu 하이브리드 본딩
- **AI 디자인 에이전트**: 강화학습 기반 설계 최적화 본격화

#### HBM7 (2035)
- 24 Gbps 데이터 레이트, 8,192 I/O, 20/24-Hi 적층
- HBM-HBF 아키텍처, 고용량 3D-스택 LPDDR + 글래스 인터포저
- 임베디드 쿨링: Thermal Transmission Line(TTL) + 유체 TSV(F-TSV)

---

## 3. 세대별 진화의 기술적 의미

### 3.1 커스텀 HBM 베이스다이 (HBM4 시작)

**핵심 변화**: HBM4부터 GPU의 일부 연산 기능이 HBM 최하층인 **베이스다이**로 이동

- 엔비디아·구글 등 고객사 요구에 맞춰 베이스다이를 커스텀 설계·제작
- HBM이 "표준화 제품"에서 **고객 맞춤형(custom) 제품**으로 전환
- D램 적층보다 **베이스다이 성능**이 HBM 전체 성능을 좌우

**베이스다이 통합 요소:**
- NMC 프로세서 (Near-Memory Computing) — GPU 부하 경감
- LPDDR 메모리 채널 — 고용량·고대역폭 확보
- 캐시(Cache), CXL — 공유 데이터 저장·메모리 확장
- 온다이/적층 디캡(decoupling capacitor), HBM 쉴딩
- 전력 무결성(PI) 최적화 핵심 부위

### 3.2 냉각 기술의 진화

- 팬냉각/히트파이프 → **액체 냉각(HBM5)** → **액침 쿨링(Immersion)** → **임베디드 쿨링(HBM7~)**
- HBM8에서는 양면 인터포저 + 임베디드 쿨링 결합
- 전력 공급·온도 균일성을 동시에 고려한 TSV 설계가 핵심 경쟁력

### 3.3 패키징 기술의 진화

- HBM6~7에서 **Cu-to-Cu 하이브리드 본딩**이 주류로 자리잡을 전망
- 미세 피치 구현 + 열전도성 개선, 기존 마이크로범프 한계 극복
- 실리콘 인터포저 → **하이브리드(Si+Glass) 인터포저**로 발전

### 3.4 HBM 센트릭 컴퓨팅

- HBM이 단순 보조 메모리를 넘어 **메모리-스토리지-컴퓨팅을 통합하는 플랫폼**
- LPDDR D램, 낸드플래시 등 다양한 메모리와 GPU 간 트래픽을 관리하는 **중심 허브**
- HBM8: GPU 상단뿐 아니라 **인터포저 양면**에 HBM 배치 → 풀 3D 구조

---

## 4. Session 2: HBM4 ~ HBM5 깊이 보기

이 세션의 핵심 메시지는 **"HBM4부터 HBM은 커스텀·컴퓨팅 중심으로 진화하고, HBM5에서 그 대격변이 본격화된다"** 입니다.

- 베이스다이에 연산·캐시·LPDDR/CXL 통합
- 발열 해결 위해 이멀전 쿨링·서멀 TSV·하이브리드 본딩 도입
- 설계 자체가 **강화학습 기반 AI 디자인 에이전트로 자동화**

### 4.1 HBM5-LPDDR 아키텍처 (윤지원)

- 커스텀 베이스다이 설계로 HBM5와 LPDDR 직접 연동
- 3D NMC 구조로 **고성능 + 저전력** 동시 달성 목표
- LPDDR 메모리 채널 활용해 고용량·고대역폭 확보
- HBM5 내 3D NMC 아키텍처와 커스텀 베이스다이 설계

---

## 5. AI 디자인 에이전트 — 6개 연구 상세 정리

HBM5 커스텀 베이스다이 설계는 강화학습(RL)과 생성형 AI를 결합해 **자동 최적화**됩니다.
아래는 해당 세션에서 발표된 6개 연구 주제의 상세 내용입니다.

---

### 5.1 하이브리드 ViT 기반 PDN 임피던스 고속 추정 (안현준)

**발표 제목**: Hybrid Vision Transformer Based Chip Design Agent for Fast Estimation of Multi-layer and Multi-power PDN Impedance in Customized Base Die in HBM5

**배경**
- HBM5 커스텀 베이스다이는 다층(Multi-layer)·다중 전력(Multi-power) 도메인을 가진 복잡한 PDN(전력분배망) 구조
- PDN 임피던스는 전력 무결성(PI) 성능을 결정하는 핵심 지표이나, EM 시뮬레이션 기반으로 측정·검증하는 것은 **시간·연산 비용이 매우 큼**
- 설계 반복(iteration)마다 3D EM 시뮬레이터를 돌리는 것은 비현실적

**접근법**
- **하이브리드 Vision Transformer(ViT)** 기반의 칩 디자인 에이전트 구축
- PDN의 구조·형상을 이미지 형태(그리드/레이어 벡터)로 인코딩
- 다층·다중 전력 PDN의 self/transfer 임피던스를 **고속 추정(서로게이트 모델)**
- EM 시뮬레이션을 대체하는 **대리(surrogate) 추정기**로 설계 최적화 루프를 단축

**의의**
- 고속 추정을 통해 검증 단계의 시간/코스트를 획기적으로 절감
- AI(안현준 박사과정)는 SI/PI/AI 전반을 다루며, 상용 EM 툴(AEDT 등) 자동화와 결합해 설계 생산성 향상에 기여

---

### 5.2 강화학습 기반 TSV 배치·IR Drop 최적화 (서은지)

**발표 제목**: Transformer-based Reinforcement Learning for TSV Placement and Design Optimization considering IR Drop in HBM5

**배경**
- HBM은 D램을 수직 적층해 TSV로 데이터와 전원을 연결
- 고속·다이 적층이 늘어나면서 **IR drop(전압 강하)** 이 심화 — 전원(P/G) 전압이 칩 내부로 갈수록 떨어짐
- TSV(특히 Power/Ground TSV)의 **배치 위치**가 IR drop과 전력 무결성에 결정적 영향
- 기존 유전 알고리즘(GA)·랜덤 서치는 조합공간이 커질수록 비효율

**접근법**
- **Transformer 기반 강화학습(RL)** 으로 TSV 배치 문제를 조합 최적화로 정의
- TSV 어레이의 위치 정보를 인코딩하고 실제 전기적 특성(IR drop)을 reward로 학습
- 테라랩은 신호 무결성(SI)을 위한 TSV 어레이 설계에도 **정책 기반 RL(PPO)** 적용
  - CNN 특성추출기 + PPO로 16-High HBM의 1-byte TSV 어레이 최적화 → **Eye Opening 18.2% 향상**
  - DQN보다 3.4%, 랜덤서치보다 9.6% 더 나은 최적성
- HBF 전력 설계에서는 **Conditional MaskGIT 기반 모방학습**으로 P/G TSV 배치 최적화로 확장

**의의**
- 대규모 조합공간에서도 효율적 탐색
- 신호 무결성(SI)뿐 아니라 전달 전력 설계까지 포괄하는 차세대 패키지 설계 자동화

---

### 5.3 Mamba-RL 기반 HBM5 PDN 전력 무결성 최적화 (김병목)

**발표 제목**: Mamba-Reinforcement Learning-based HBM5 Design Agent for Fast PDN Optimization considering Power Integrity

**관련 연구**: *Mamba-based RL for HBM PDN Optimization with Probing Port-Agnostic Policy* (IEEE EP EPS 2025)

**배경**
- HBM PDN의 디커플링 캐패시터(decap) 배치는 전력 무결성(PI)을 결정하는 조합 최적화 문제
- 기존 Transformer 기반 RL은 최적성은 좋지만 **연산 비용이 크고 시퀀스 처리가 무거움**
- probing port 위치가 바뀌면 재학습·재최적화가 필요하다는 재사용성 한계

**접근법**
- **Mamba 아키텍처** (SSM 기반 선형복잡도 시퀀스 모델) 를 RL 정책 네트워크로 채택
- Transformer의 어텐션(O(n²)) 대비 **선형복잡도(O(n))** 로 고속 처리
- **Probing Port-Agnostic Policy**: probing port 위치에 관계없이 동작하는 정책 — 재사용성 향상
- 전력 무결성(PDN 임피던스)을 reward로 한 강화학습으로 HBM5 PDN 신속 최적화

**의의**
- Transformer와 유사한 성능을 유지하면서도 **속도·효율성 향상**
- 커스텀 베이스다이 설계 시 probing port가 달라져도 재학습 없이 적응 가능 → 설계 시간 단축

---

### 5.4 DevFormer + 협력 증류 기반 디캡 배치 최적화 (김혜연)

**발표 제목**: Devformer with Collaborative Distillation for Optimal Decoupling Capacitor Placement in HBM5 Custom Base Die

**관련 연구**:
- *DevFormer: A Symmetric Transformer for Context-Aware Device Placement* (ICML 2023)
- *Collaborative Distillation Meta Learning (CDML) framework for decoupling capacitor placement on PDN*

**배경**
- 디캡(decoupling capacitor) 배치 문제(DPP)는 하드웨어 전력 무결성의 핵심 조합 최적화 문제
- Transformer는 하드웨어 설계에 유망하나 **오프라인 데이터 부족**으로 학습이 어려움
- 실측 전기 성능 평가는 시뮬레이션이 비싸 RL의 잦은 reward 계산에 부적합

**접근법 — DevFormer 아키텍처**
- 다음의 **강한 귀납적 편향(inductive bias)** 도입:
  - **상대 위치 임베딩(Relative Positional Embedding)**: 하드웨어에서 절대위치보다 상대거리가 중요
  - **Action-Permutation 대칭성(AP-Symmetricity)**: 디캡 배치 순서는 성능에 무관
- probing port 위치를 컨텍스트로 포착해 일반화 능력 향상
- 적은 데이터로도 효율적 설계 최적화 가능

**접근법 — 협력 증류(CDML)**
- **Expert Distillation**: GA(유전 알고리즘)가 생성한 고품질 라벨을 모방, 배치 순서를 치환해 라벨 증강
- **Self-Distillation**: 정책 자신이 생성한 데이터와 그 치환 라벨 사이의 확률 유사성 최대화 → 광범위한 액션 공간으로 일반화
- **Equivariant Label Transformation**으로 샘플 효율·일반화 개선

**성능 결과**
- 시뮬레이션·실제 하드웨어 모두에서 SOTA 대비 우수
- **디캡 개수 30% 이상 절감** (GA가 요구하는 40개·AM-CIL 34개 대비 DevFormer는 26개로 동일 성능)
- 전력 노이즈 94.2% 저감 (GA는 40개로 93.5%)
- **Zero-shot 전이(transfer-ability)** 로 재학습 없이 새 문제 대응

---

### 5.5 RL 기반 디캡 배치 최적화 — 다양한 I/O 인터페이스 (박준호)

**발표 제목**: Reinforcement Learning-based Decap Placement Optimization considering Diverse I/O Channel Interfaces in Custom Base Die of HBM5 Memory Pooling Architecture

**관련 연구**: *Transformer Network-based RL for PDN Optimization of HBM* (IEEE T-MTT), *Multi-Chiplet PDN Co-Optimization considering Current Spectrum by DRL-Based Decap Placement* (ECTC 2025)

**배경**
- HBM5 커스텀 베이스다이와 **메모리 풀링(Memory Pooling) 아키텍처**에서는 다양한 I/O 채널 인터페이스가 공존
- 채널별 전류 스펙트럼(switching current)이 달라 동시 스위칭 노이즈(SSN)가 심화됨
- 기존 방법은 단일 objective·단순 문제만 다뤄 실용성이 제한

**접근법**
- **Transformer 기반 RL**로 디캡 배치를 시스템 레벨에서 최적화
- 각기 다른 I/O 채널의 **self/transfer 임피던스**와 전류 스펙트럼 차이를 동시에 고려
- **Context Embedding**으로 probing port 위치·디캡 후보 메타특성을 반영 → 재사용성 확보
- 기존 RL 방법들과 달리 **transfer impedance(결합된 전력 노이즈)** 와 다중 probing port까지 반영

**성능/의의**
- GA·랜덤서치 대비 **최적성·재사용성·시간 효율성** 모두 우수
- Keepout 영역·디캡 개수 변경 같은 **설계 제약 변화에도 적응** (co-optimization)
- 학습 네트워크가 random 데이터로 학습되어 **확장성(scalability)** 확보

---

### 5.6 PSIJ 모델링 + RL 기반 I/O 인터페이스 최적화 (신태인)

**발표 제목**: Power Supply Noise Induced Jitter (PSIJ) Modeling and Reinforcement-Learning based PI Optimization for HBM5 I/O Interface

**관련 연구**:
- *PSIJ based HBM I/O Interface Optimization using Discrete-Continuous Space RL* (KAIST 박사논문)
- *PSIJ-Based Integrated Power Integrity Design for HBM using RL: Beyond the Target Impedance* (DesignCon 2025 **Best Paper Award**)

**배경**
- 전력 공급 노이즈가 타이밍 지터에 전달되는 **PSIJ(Power Supply Induced Jitter)** 는 고속 I/O 성능의 주요 제약
- 기존 전력 무결성 설계는 "target impedance(목표 임피던스)" 기반으로, 타이밍 정보(지터)를 직접 반영하지 못함
- I/O 인터페이스는 **이산(디캡 개수·배치) + 연속(채널 폭·두께, 드라이버 설계)** 파라미터가 혼재

**접근법**
- PSIJ 자체를 설계 지표로 삼아 **Discrete-Continuous 공간 강화학습(RL)** 적용
- PDN 디캡 개수·배치, 채널 파라미터(폭·두께·유전체 높이), I/O 드라이버 설계를 **동시 최적화**
- **Jitter Tracking(지터 전달)** 포함한 시스템 레벨 PSIJ 도출·분석을 통해 각 설계요소의 상대적 영향 정량화
- Switch Transformer 기반 RL로 모델을 키우면서도 연산량은 유지 (sparse activation)

**성능/의의**
- 목표 PSIJ를 만족하면서 **면적·전력 최소화** 달성
- "Target Impedance를 넘어서는(Beyond the Target Impedance)" 새로운 전력 무결성 패러다임 제시
- GA 대비 연산시간·데이터 비용 크게 절감, 신규 문제에 재사용 가능
- **DesignCon 2025 국제학회 Best Paper Award** 수상 — 산업계·학계 주목

---

## 6. 마무리 및 평가

### 6.1 세미나의 의의

- 김정호 교수(테라랩)는 2010년 세계 최초로 HBM 기본 구조를 제시해 국내 반도체 기업의 HBM 사업 초석을 마련
- 현재 한국 기업이 HBM 시장 **90% 이상 점유** 중이나, 미래 주도권을 위해 로드맵 주도 필요성을 강조
- "패스트 팔로워에서 **모델을 제시하는 리더**로 변모해야 한다"

### 6.2 핵심 인사이트 요약

| 주제 | 핵심 내용 |
|------|-----------|
| 대역폭 | 3년마다 2배 이상 개선, HBM4 2TB/s → HBM8 64TB/s |
| TSV | HBM3E 1,024개 → HBM8 16,384개, HBM 면적의 40%까지 차지 전망 |
| 냉각 | 액체→액침→임베디드 쿨링 진화, 열·전력 균일성이 핵심 |
| 베이스다이 | HBM4부터 커스텀화, 연산·캐시·LPDDR/CXL 통합 |
| 컴퓨팅 | HBM 센트릭 컴퓨팅, LPDDR·낸드(HBF) 통합 허브 |
| AI 설계 | 강화학습·생성형 AI로 HBM 설계 자동화 본격화 |

### 6.3 향후 전망 (김정호 교수)

- 10~20년 후 파라미터가 1,000조(Quadrillion)까지 성장 전망
- 통신 속도가 100 Gbps를 넘어서면 **데이터 전송 방식이 광통신**으로 전환될 것
- 미국·중국 사이의 한국 반도체 산업이 **HBM을 중심으로 돌파구**를 찾아야 함

---

## 7. 참고 자료

- KAIST TERALAB: https://tera.kaist.ac.kr/
- KAIST TERALAB HBM Milestone and Roadmap: https://tera.kaist.ac.kr/researches/teralab-hbm-milestone-and-roadmap
- Hyunwook Park et al., *Transformer Network-based RL for PDN Optimization of HBM*, IEEE T-MTT (2022)
- Haeyeon Kim et al., *DevFormer: A Symmetric Transformer for Context-Aware Device Placement*, ICML 2023
- Haeyeon Kim et al., *Collaborative Distillation Meta Learning (CDML) framework*, IEEE T-EMC
- Taein Shin, *PSIJ-based Integrated PI Design for HBM using RL*, DesignCon 2025 (Best Paper)
- Byeongmok Kim et al., *Mamba-based RL for HBM PDN Optimization*, IEEE EP EPS 2025
- Keunwoo Kim et al., *Policy-based RL for TSV Array Design in HBM considering SI*, IEEE T-EMC (2024)
