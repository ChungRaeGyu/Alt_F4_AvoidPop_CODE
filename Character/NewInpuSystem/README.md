# NewInputSystem
새로운 InPutSystem을 사용해 보았습니다.

# 기술 활용
💡 <b>장점 : </b> 다양한 플랫폼에서의 키 입력을 Actions에 설정해주기만 하면 쉽게 받아올 수 있다. 입력을 이벤트로 받아오기 때문에 Update문에서 계속 확인하지 않아도 된다.<br>

### InputSystem구성
![image](https://github.com/ChungRaeGyu/Alt_F4_AvoidPop_CODE/assets/125470068/f1c96e4b-a522-4974-84b4-15c4dd3bc365)

ActionMap을 Player1 ,Player2로 나누어서 각각 A,D와 왼쪽화살표, 오른쪽화살표로 2인로컬플레이가 될 수 있도록 하였다.

# TroubleShooting
![image](https://github.com/ChungRaeGyu/Alt_F4_AvoidPop_CODE/assets/125470068/4a1be6eb-b081-41c8-b7ac-137eefbc3ae6)


# 주요 메서드
### CharacterController
|메서드|설명|
|-------------------------------------------|---|
|OnMove(InputAction.CallbackContext context)|키보드 입력값을 context로 받아오고 Invoke를 통해서 같은 오브젝트안에 있는 컴포넌트에 보내준다.|
<br>

### CharacterMovement

|메서드|설명|
|-------------------------------------------|---|
|Start()|InputSystem에서 Invoke로 보내주는 값을 받아줄 핸들러를 등록한다.|
|Move(Vecotr2 direction)|핸들러이고,  실제 움직임을 담고 있다.|
<br>

### CharacterAnimationController

|메서드|설명|
|-------------------------------------------|---|
|Start()|InputSystem에서 Invoke로 보내주는 값을 받아줄 핸들러를 등록한다.|
|Anim(Vecotr2 vector)|핸들러이고,  움직임에 따라서 애니메이터의 값을 변경해준다.|
