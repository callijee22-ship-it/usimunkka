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

1. 최종 Frontend 및 Visual Asset 기여
2. 발표자료 제작 및 수정 과정
3. 초기 **M4 / PAGE1** 구현 아카이브
4. 개발 과정과 Troubleshooting
5. 개인 기여 범위 및 팀 작업 구분

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

# Final Frontend & Visual Contribution

초기 M4 / PAGE1 작업 이후에도  
팀 통합 과정에서 Frontend UI와 Visual Asset 작업에 참여했습니다.

프로젝트 후반에는 초기 지역 경쟁 화면과 별개로  
캐릭터 커스터마이징, 캐릭터 디자인 변형, 방 꾸미기 테마,  
Motion Test 등 최종 서비스의 시각적 경험을 확장하는 작업을 진행했습니다.

---

## Character Customization

여성 / 남성 캐릭터를 기반으로  
한복 및 전통 의상 콘셉트와 다양한 캐릭터 디자인 시안을 제작했습니다.

<p align="center">
  <img src="./docs/visual-assets/hanbok-female.png" width="23%">
  <img src="./docs/visual-assets/hanbok-female-2.png" width="23%">
  <img src="./docs/visual-assets/hanbok-male.png" width="23%">
  <img src="./docs/visual-assets/hanbok-male-2.png" width="23%">
</p>

Level 5 해금용 캐릭터 디자인과  
계절별 운동복 및 포즈 적용 시안도 제작했습니다.

<p align="center">
  <img src="./docs/visual-assets/lv5_winter_all_poses.png" width="46%">
  <img src="./docs/visual-assets/lv5_summer_all_poses.png" width="46%">
</p>

---

### Character Redesign Preview

프로젝트 후반에는 기존 캐릭터 스타일을 확장하기 위해  
전통 의상과 색상 조합을 바탕으로 다양한 캐릭터 리디자인 시안을 제작했습니다.

#### Concept Design

<p align="center">
  <img src="./docs/visual-assets/character-redesign/character-concept-sheet-blue-teal.png" width="46%">
  <img src="./docs/visual-assets/character-redesign/character-concept-sheet-red-navy.png" width="46%">
</p>

초기 Concept Sheet를 기준으로  
의상 색상, 장식, 실루엣과 캐릭터 표현 방식을 확장했습니다.

#### Character Redesign

<p align="center">
  <img src="./docs/visual-assets/character-redesign/character-chibi-purple-dress.png" width="23%">
  <img src="./docs/visual-assets/character-redesign/character-fullbody-purple.png" width="23%">
  <img src="./docs/visual-assets/character-redesign/character-chibi-black-red.png" width="23%">
  <img src="./docs/visual-assets/character-redesign/character-chibi-black-red-alt.png" width="23%">
</p>

Concept 단계에서 검토한 전통 의상 요소를  
서비스 캐릭터에 적용할 수 있도록 여러 스타일과 색상으로 변형했습니다.

➡️ [Character Redesign Archive](./docs/visual-assets/character-redesign/)

---

## Room Customization

프로젝트 후반에는 사용자가 자신의 운동방을 꾸밀 수 있도록  
여러 분위기의 방 테마와 가구 Asset을 제작했습니다.

각 테마는 빈 공간과 개별 가구 Asset뿐 아니라  
실제 배치가 완료된 대표 시안까지 함께 구성했습니다.

### Blue Oriental

<p align="center">
  <img src="./docs/visual-assets/room-assets/blue-oriental/final_room.png" width="70%">
</p>

### Mint Oriental

<p align="center">
  <img src="./docs/visual-assets/room-assets/mint-oriental/final_room.png" width="70%">
</p>

### Pink Oriental

<p align="center">
  <img src="./docs/visual-assets/room-assets/pink-oriental/final_room.png" width="70%">
</p>

### Dark Oriental

<p align="center">
  <img src="./docs/visual-assets/room-assets/dark-oriental/final_room.png" width="70%">
</p>

### Oriental Retro

<p align="center">
  <img src="./docs/visual-assets/room-assets/oriental-retro/final_room.png" width="70%">
</p>

각 테마는 방 배경과 개별 가구 Asset을 조합해  
서로 다른 분위기의 운동방을 구성할 수 있도록 제작했습니다.

➡️ [Room Asset Archive](./docs/visual-assets/room-assets/)

---

## Motion Test

캐릭터가 정적인 이미지에 머물지 않도록  
걷기 및 움직임 표현을 위한 프레임과 GIF 테스트도 진행했습니다.

➡️ [Character Motion Tests](./docs/visual-assets/motion-tests/)

---

# Presentation Development

프로젝트 발표자료의 구성 및 수정 작업에도 참여했습니다.

발표자료는 단순히 슬라이드의 디자인을 변경하는 방식이 아니라,  
프로젝트 전체 구조와 데이터 처리 과정을 이해하고  
발표자가 실제 발표에서 설명하기 쉬운 형태로 내용을 재구성하는 방향으로 작업했습니다.

---

## Presentation Revision Overview

<p align="center">
  <img src="./docs/presentation/presentation_revision_overview.png" width="95%">
</p>

발표자료는 다음 과정을 거쳐 수정되었습니다.

```text
Preliminary Draft
        ↓
Initial Full Version
        ↓
Revised Version
        ↓
Presenter Feedback
        ↓
Pipeline Concept Revision
        ↓
Final Expected Version
