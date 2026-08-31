# 01. 캐릭터 시스템 & 구조도 (Characters & Systems)

## 1. 캐릭터 핵심 시스템 구조도

```mermaid
flowchart TD
    subgraph Character[캐릭터 스펙 & 장비]
        A[캐릭터 본체] --> B[전용 무기: 고유 외형/기본 액션]
        A --> C[전용 퍽: 캐릭터 보유 패시브]
        A --> D[보호구 슈트: 스탯 강화 & 인챈트]
    end

    subgraph PartyCombat[4인 파티 전투]
        E[메인 조작 / 태그 교체] --> F[일반 공격 & 스킬 사용]
        F --> G[통찰 Insight 스탯 기반]
        G --> H[(파티 공용 통찰 게이지)]
    end

    subgraph Fever[특이점 관측: 피버타임]
        H -- 100% 완충 시 --> I[적 전체 약점 완전 노출]
        I --> J[방어력 급감 & 폭딜 타임]
    end

    subgraph PerkSystem[데바데식 퍽 계승]
        C --> K[전용 퍽 전수 해금]
        K --> L[타 캐릭터의 빈 퍽 슬롯에 장착]
        M[인게임 4성 범용 퍽] --> L
    end
