# 우심운까 | Frontend Contribution Archive 🏃

### 우리 심심한데 운동이나 할까?

지역·운동 취향·현재 상황을 바탕으로 운동 장소를 추천하고,  
운동 기록과 캐릭터·운동방·친구 기능을 통해  
다음 운동으로 다시 이어지도록 설계한 생활체육 웹 서비스입니다.

> 이 저장소는 팀 프로젝트 **「우심운까」 전체를 개인 프로젝트로 복제한 저장소가 아닙니다.**
>
> 프로젝트 개발 과정에서 제가 담당하거나 직접 수정·개선한  
> **M4 / PAGE1 및 Frontend 관련 작업을 기록하기 위한 개인 기여 아카이브**입니다.

---

## Project

**우심운까 (WoosimWoonkka)**  
우리 심심한데 운동이나 할까?

운동을 하려고 마음먹은 사용자가

**운동할 곳 탐색 → 선택 → 실제 운동 → 기록 → 보상 → 재참여**

까지 자연스럽게 이어갈 수 있도록 만든 팀 프로젝트입니다.

초기에는 지역 및 친구 간 운동 경쟁을 활용한  
**지역 랭킹 PAGE1**을 중심으로 개발을 시작했습니다.

이후 팀 통합 과정에서 서비스 구조가 변경되면서  
최종 서비스는 다음과 같은 사용자 흐름을 중심으로 발전했습니다.

`HOME → MOVE → DIARY → FRIENDS → PROFILE`

따라서 이 저장소에는 다음 내용을 구분하여 기록합니다.

1. 제가 담당했던 초기 **M4 / PAGE1 구현 기록**
2. 팀 통합 이후 Frontend에서 제가 참여한 작업
3. 개발 과정에서 발생한 문제와 수정 과정
4. 직접 제작하거나 수정한 Visual Asset 및 Motion Test

---

# My Role

## Frontend · M4 / PAGE1

초기 역할 분담에서 **M4 / PAGE1 Frontend**를 담당했습니다.

PAGE1의 목적은 단순히 지역 순위를 보여주는 것이 아니라,

**지역 경쟁을 보여주고 → 운동 동기를 만들고 → 운동추천 화면으로 연결하는 것**

이었습니다.

### 초기 M4 담당 범위

- 대한민국 지역 지도 UI
- 지역별 운동 랭킹 시각화
- 시·군·구 상세 랭킹 Popup
- 내 지역 상태 표시
- 상승 지역 및 상위 지역 강조
- 친구 운동 랭킹 UI
- 지역 마스코트 연동
- TOP1 캐릭터 강조
- 지도 Hover / Popup Interaction
- 운동추천 CTA
- 로그인 상태에 따른 CTA 이동 분기
- 현재 위치 / 사용자 지정 위치 추천 CTA·선택 흐름
- Mock 데이터 및 API 교체를 고려한 Frontend 구조
- 반응형 PAGE1 UI

---

# 01. 대한민국 지역 랭킹 지도

초기 PAGE1의 핵심 기능은  
대한민국 지도를 이용한 지역 운동 랭킹 시각화였습니다.

단순한 순위표 대신 사용자가 지도를 직접 선택할 수 있도록 구성하여

**“어느 지역이 더 많이 움직이고 있는가?”**

를 한 화면에서 확인할 수 있도록 했습니다.

지역 Hover Interaction,  
지역 이름 표시,  
지역 선택 이벤트 등을 적용했습니다.

개발 과정에서는 지도 비율과 지역 데이터 누락 문제를  
반복적으로 확인하고 수정했습니다.

울릉도와 독도도 지도 표시 범위에 포함했습니다.

---

## 당시 구현 화면

### PAGE1 초기 디자인

![PAGE1 초기 화면](./docs/screenshots/page1_before_theme.png)

### PAGE1 컬러 및 UI 개선

![PAGE1 컬러 개선](./docs/screenshots/page1_color_full.png)

---

# 02. 지역 상세 랭킹 Popup

지도에서 특정 지역을 선택하면  
해당 지역의 시·군·구 정보를 확인할 수 있는  
상세 Popup UI를 구성했습니다.

Popup에서는 다음 정보를 표현하도록 했습니다.

- 지역명
- 지역 순위
- 순위 변화량
- 상승 상태
- 지역별 마스코트
- 운동추천 화면 이동 CTA

### 지역 Popup

![지역 상세 Popup](./docs/screenshots/page1_popup_seoul.png)

---

# 03. 랭킹 변화 시각화

운동 랭킹을 단순한 숫자로만 보여주지 않고  
사용자가 변화 상태를 시각적으로 느낄 수 있도록 구성했습니다.

상승 중인 지역에는 별도의 강조 효과를 적용하고,  
1위 지역은 일반 지역과 다른 상태로 표현했습니다.

랭킹 데이터의 상태에 따라 UI가 달라질 수 있도록 구성하여

**데이터 → UI 변화**

가 자연스럽게 연결되는 화면을 만들고자 했습니다.

---

# 04. TOP1 Character

지역 경쟁이라는 서비스 컨셉을  
조금 더 친근하게 전달하기 위해  
지역 마스코트와 캐릭터 연출을 활용했습니다.

특히 전국 1위 지역에는

- TOP1 Badge
- Trophy / Medal
- Character Highlight
- Popup Animation

등을 적용하여 일반 지역과 구분했습니다.

### TOP1 Popup

![TOP1 Character](./docs/screenshots/page1_popup_top1_suwon.png)

---

# 05. 운동추천 CTA

PAGE1의 목적은 순위를 보여주는 것에서 끝나는 것이 아니라  
사용자가 실제 운동 행동으로 이동할 수 있도록 연결하는 것이었습니다.

대표 메시지로

> **그래서 오늘 운동 안 할 거야?**

를 사용하고 운동추천 CTA를 배치했습니다.

이후 추천 화면으로 이동하는 방식을 두 가지로 분리했습니다.

### 현재 위치 기반 추천

사용자의 현재 위치를 기준으로  
추천 화면으로 이동할 수 있는 흐름을 구성했습니다.

### 원하는 지역 기반 추천

사용자가 원하는 지역을 직접 선택한 뒤  
해당 지역을 기준으로 추천 화면으로 이동할 수 있도록 구성했습니다.

![위치 선택 CTA](./docs/screenshots/page1_location_cta.png)

이 위치 선택 개념은 이후 최종 서비스의 MOVE 화면에서도

**지역 선택 / 현재 위치**

두 가지 방식으로 이어졌습니다.

> 초기 연결본에서는 실제 추천 로직 및 현재 위치 기반 API 실행이 완성된 상태가 아니었으며,  
> PAGE1에서 추천 화면으로 이동하는 CTA와 선택 흐름을 중심으로 작업했습니다.

---

# 06. 팀 통합 이후 Frontend 변경

프로젝트 후반부에는 팀 전체 UI와 서비스 구조가 크게 변경되었습니다.

초기 M4의

`대한민국 지도 → 지역 경쟁 → 운동추천`

중심 구조에서,

최종 서비스는

`HOME → MOVE → DIARY → FRIENDS → PROFILE`

형태로 재구성되었습니다.

따라서 초기 PAGE1 화면 자체가  
현재 최종 서비스에 그대로 남아 있는 것은 아닙니다.

본 저장소에서는 이 차이를 숨기지 않고

**초기 담당 구현과 최종 통합 이후 참여 범위를 구분하여 기록합니다.**

---

# 07. 최종 Frontend 통합 단계 참여

후반 Frontend 통합 과정에서도  
사용자 화면과 UX 수정에 참여했습니다.

팀 최종 저장소에서는 역할이

**Frontend · 발표자료**

로 구분되어 있으며,

서비스 화면 구현 및 사용자 경험 구성을  
Frontend 팀원과 함께 진행했습니다.

---

## Character Gender UI

프로젝트 후반에는  
캐릭터 성별 선택 UI와 화면 연동 수정에 참여했습니다.

프로필에서 선택한 캐릭터 타입이

- PROFILE
- HOME
- MOVE

등의 캐릭터 이미지에 연결될 수 있도록 하는  
Frontend 흐름을 함께 수정했습니다.

```text
FEMALE CHARACTER
        ↕
CHARACTER TYPE
        ↕
MALE CHARACTER
```

---

# 08. Visual Asset Contribution

프로젝트 후반에는 캐릭터 커스터마이징을 위한  
이미지 제작 및 적용 테스트에도 참여했습니다.

제가 직접 제작하거나 수정한 주요 작업은 다음과 같습니다.

- 여성 / 남성 한복 캐릭터 이미지
- Level 5 해금용 운동복 시안
- 겨울 / 여름 의상 Sheet
- 포즈별 의상 적용 이미지
- 캐릭터와 의상을 분리하기 위한 의상 전용 PNG
- 캐릭터 걷기 및 움직임 테스트
- Motion GIF 제작 및 적용 가능성 검토

초기에는 캐릭터 전체 이미지를 교체하는 방식으로 작업했지만,  
실제 커스터마이징 적용을 고려하면서  
캐릭터와 의상을 분리하는 방향으로 작업을 확장했습니다.

자세한 이미지와 테스트 자료는 아래 문서에서 확인할 수 있습니다.

➡️ [Visual Asset Contribution](./docs/visual-assets/)

---

# 09. Development Process

이 프로젝트는 한 번에 완성된 화면을 만든 것이 아니라

```text
요구사항 확인
        ↓
Prototype
        ↓
문제 발견
        ↓
수정
        ↓
팀 공유
        ↓
통합
        ↓
재수정
```

과정을 반복하며 개발했습니다.

특히 팀 프로젝트에서는  
제가 구현한 화면이 다른 팀원의 코드와 병합되고,  
전체 디자인 시스템과 서비스 구조가 변경되면서  
최종 코드의 형태도 크게 달라지는 경험을 했습니다.

이를 통해

**최종 코드에 몇 줄이 남아 있는가보다  
프로젝트에서 어떤 문제를 맡아 해결했는가가 중요하다**

는 점을 배웠습니다.

---

# Troubleshooting

## 지도 비율 문제

### Problem

화면 크기에 따라 대한민국 지도 형태가 찌그러지는 문제가 발생했습니다.

### Solution

SVG ViewBox와 부모 컨테이너의 비율,  
반응형 크기 설정을 조정하여  
화면 크기가 변경되어도 지도 형태가 유지되도록 수정했습니다.

---

## 지역 데이터 누락

### Problem

일부 지역이 지도 또는 랭킹에서 누락되는 문제가 발생했습니다.

### Solution

지역 데이터와 지도 요소의 매핑을 다시 확인하고  
누락된 지역 정보를 보완했습니다.

---

## Popup Interaction

### Problem

Popup 크기와 Hover 효과,  
Border Animation이 의도한 영역과 다르게 표현되는 문제가 있었습니다.

### Solution

Popup 구조와 CSS Layer를 반복적으로 수정하여  
효과가 의도한 영역에서 표현되도록 조정했습니다.

---

## Login Routing

### Problem

같은 운동추천 CTA라도  
로그인 여부에 따라 이동 경로가 달라야 했습니다.

### Solution

비로그인 사용자는 로그인 화면으로,  
로그인 사용자는 운동추천 화면으로 이동하도록  
사용자 상태에 따른 흐름을 분리했습니다.

---

# Tech Stack

### Frontend

- HTML
- CSS
- JavaScript
- Django Templates

### Collaboration

- GitHub
- Team-based Development

### Project Environment

- Python
- Django
- PostgreSQL

> Backend와 데이터 파이프라인 전체를 제가 구현했다는 의미가 아니며,  
> 위 기술은 팀 프로젝트의 전체 실행 환경을 포함합니다.

---

# Contribution Scope

## 직접 담당

### 초기 M4 / PAGE1

- 대한민국 지역 지도
- 지역 랭킹 UI
- 지역 상세 Popup
- 지역 마스코트
- TOP1 UI
- 친구 랭킹 화면
- 운동추천 CTA
- PAGE1 Interaction
- 위치 선택 CTA 흐름
- 반응형 PAGE1

## 팀 통합 과정에서 참여 / 개선

### 최종 Frontend

- 사용자 화면 및 UX 수정
- 캐릭터 성별 선택 UI 및 화면 연동
- 한복 캐릭터 Visual Asset 제작
- Level 5 운동복 이미지 제작
- 캐릭터 / 의상 분리 PNG 제작
- 포즈별 캐릭터 적용 이미지 제작
- Motion Test 및 GIF 제작
- 현재 위치 / 지역 선택 기반 추천 UX 검토
- 발표자료 및 서비스 화면 정리

Django Backend,  
추천 알고리즘 전체,  
공공데이터 수집 Pipeline,  
Database 설계 등은  
다른 팀원의 주요 담당 영역이므로  
개인 기여로 주장하지 않습니다.

---

# Repository Structure

```text
.
├─ README.md
│
├─ archive/
│  └─ page1-m4/
│     ├─ 2026-09-11-core/
│     ├─ 2026-09-11-v3/
│     ├─ 2026-09-14-final/
│     └─ 04_region_popup_CTA_2026-09-14/
│
├─ docs/
│  ├─ screenshots/
│  ├─ visual-assets/
│  │  └─ motion-tests/
│  └─ CONTRIBUTION_EVIDENCE.md
│
└─ final-integration/
   └─ README.md
```

---

# More Details

- [M4 / PAGE1 Contribution Archive](./archive/page1-m4/)
- [Visual Asset Contribution](./docs/visual-assets/)
- [Final Frontend Integration](./final-integration/README.md)
- [Contribution Evidence](./docs/CONTRIBUTION_EVIDENCE.md)

---

# Repository Notice

본 저장소의 초기 PAGE1 화면은  
팀 통합 이전 제가 M4를 담당하던 시점의 작업물입니다.

이후 팀 프로젝트의 방향과 Frontend 구조가 변경되면서  
현재 최종 서비스와 디자인 및 기능 구성이 달라졌습니다.

따라서 이 저장소는

**현재 우심운까 전체 서비스의 복제본**

이 아니라

**팀 프로젝트에서 제가 담당하고 참여했던 Frontend 개발 과정과  
Visual Asset 작업을 기록한 개인 기여 아카이브**

입니다.

팀 프로젝트의 다른 구성원이 담당한 기능을  
개인 작업으로 표현하지 않습니다.
