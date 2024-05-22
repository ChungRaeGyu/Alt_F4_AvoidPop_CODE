<div align="center"><h1> Alt_F4_AvoidPop</h1>
스파르타코딩클럽C4조 팀과제 입니다. 똥피하기를 만들었습니다.</div>


# 목차
  - [개요](#개요) 
  - [게임 설명](#게임-설명)
  - [게임 플레이 방식](#게임-플레이-방식)
  - [Team Notion](#Team-Notion)
  - [와이어프레임](#와이어프레임)
  - [UML](#UML)
  - [TroubleShooting](#TroubleShooting)
## 개요

|Alt_F4_AvoidPop|2024.05.16 ~ 2024.05.22| 개발언어 : C# <br> 게임엔진 : 유니티|   팀장 : 서정재<br> 팀원 : 정래규<br>  팀원 : 여현빈 <br> 팀원 : 김성훈 |
|:----:|:----:|:----:|:----:|
|프로젝트 이름 |프로젝트 지속기간|개발언어 및 게임엔진|팀원소개|

## 게임 설명
- 하늘에서 떨어지는 똥을 피하며 오래오래 버티는 게임입니다.<br>
- 1인 플레이와 로컬2인플레이를 지원합니다.
- 1인 플레이시 랭킹을 저장하여 최고점수를 나타내 줍니다.
- 2인 플레이시 상대방과 경쟁하여서 누가더 오래 살아남았는지 게임종료시 표시해 줍니다.

### 1인 플레이
|![메인화면](https://github.com/ChungRaeGyu/Alt_F4_AvoidPop/assets/125470068/bc2c365f-99fe-4ef0-8955-812115ea1d39)|![랭킹](https://github.com/ChungRaeGyu/Alt_F4_AvoidPop/assets/125470068/a61becdc-da9f-46af-886f-9808148b418a)|![1인플레이화면](https://github.com/ChungRaeGyu/Alt_F4_AvoidPop/assets/125470068/df6bb7a4-ed57-45cf-9c89-addfacf7a379)|![게임오버](https://github.com/ChungRaeGyu/Alt_F4_AvoidPop/assets/125470068/aba02879-e97f-453f-92ef-01faba82258e)|
|:---:|:---:|:---:|:---:|
|메인화면|랭킹화면|1인플레이화면|게임오버 화면|
|닉네임 입력후 1인플레이를 하거나, 2인플레이로 넘어갈 수 있습니다. <br>왼쪽 하단의 메달을 누르면 랭킹화면이 나옵니다.|랭킹이 나옵니다.|1인플레이 화면입니다.|메인으로 돌아가거나 다시 시작할 수 있습니다.

### 2인 플레이
|![2P선택](https://github.com/ChungRaeGyu/Alt_F4_AvoidPop/assets/125470068/387f2672-1780-4911-b850-94efeab63f6d)|![캐릭터 색 선택](https://github.com/ChungRaeGyu/Alt_F4_AvoidPop/assets/125470068/a09959c7-6915-4823-9533-bf830fa990a9)|![2p 메인](https://github.com/ChungRaeGyu/Alt_F4_AvoidPop/assets/125470068/fe9e3642-1ae8-4a01-96f3-09cd5eaa1541)|![2P결과](https://github.com/ChungRaeGyu/Alt_F4_AvoidPop/assets/125470068/ceba4789-f861-46f2-b5a4-bb85f30d218b)|
|:---:|:---:|:---:|:---:|
|2인플레이선택|플레이어 색 선택 화면|2인플레이 메인화면|2인플레이 결과|
|플레이어의 색을 선택할 수 있게 합니다.|색을 선택 할 수 있습니다.||승, 패 만을 보여줍니다.|


## 게임 플레이 방식
- 1인 플레이 : A, D를 사용하여 좌우로 움직입니다.
- 2인 플레이 : 1번 플레이어는 A, d 2번 플레이어는 화살표 왼쪽, 오른쪽을 사용하여 각각 좌우로 움직입니다.


## Team Notion
https://teamsparta.notion.site/Alt-F4-ee66ec4267dd4809961b3a942f0ffc55


## 와이어프레임
![image](https://github.com/ChungRaeGyu/Alt_F4_AvoidPop_CODE/assets/125470068/5cf3a5bf-8652-4832-958e-7f76d87c0a75)


## UML
https://drive.google.com/file/d/1QHPmVl6Nj8ii2XEyXZDTLgR_nid5XMWm/view?usp=sharing
## TroubleShooting
#### 서정재
- 문제 :  2p 캐릭터 선택 창에서 2p의 캐릭터를 바꿔도 1p 선택 창이 계속 바뀌었던 문제
- 원인 : 선택할 수 있는 캐릭터의 배열이 1개만 생성되어 있어서 2p에서 변경을 하여도 1p의 캐릭터만 인식되고 있었다.
- 해결법 : 2p의 캐릭터를 선택할 수 있는 배열을 하나 더 만들어주고 DataManager에서도 2p의 캐릭터 선택 정보를 읽을 수 있게 변수를 선언해주었다. 
#### 정래규
- [TroubleShooting입니다](./Character/README.md)

#### 여현빈
- 문제 : 플레이 중 시간이 지날수록 렉이 발생하며 게임의 매끄러운 진행의 문제발생
- 원인 : 낙하물 오브젝트가 시간이 지날수록 Hierarchy에 비활성화된 오브젝트가 과잉 생성으로 렉을 유발함
- 해결법: 낙하물 오브젝트 스크립트를 Object Pooling 방식으로 다시 만들어 생성되는 양을 조절해 해결

#### 김성훈
- 문제 : GUI 팝업의 닫기 버튼을 누를 때 효과음이 재생되지 않는 현상 발생
- 원인 : Audio Source를 닫기 버튼 입력 시 비활성화 할 UI에 할당하여 문제 발생
          닫기 버튼 입력 시 GUI 게임 오브젝트를 비활성화 하는데 이 때 Audio Source의 재생을 수행하지 않고 비활성화됨
- 해결법 : Audio 오브젝트를 따로 제작하여 효과음 재생을 담당하는 방식으로 문제 해결
