# InputView                                                                        
 - [ o ] 다리길이를 입력 받는다
 - [ o ] 어디로 건널지 (U, D)
 - [ o ] 재시도 여부 (R, Q)

# BridgeMaker ( 다리 만드는 클래스 )                                                   
 
 - [ o ] 길이 만큼 랜덤 값 가져오기 String 으로 가져오기 ex) [1,0,0]

# BridgeGame ( 다리 게임 어디로 건널지 입력 받고 알려주는, 재시도 입력받고 알려주는 클래스 )    
 - [ o ] move -> 이 다리를 건널수 있는지 체크
 - [ o ] retry -> R이면 true, Q이면 false
 
# BridgeShape ( 게임 진행하면서 다리 모양 만들어주는 클래스 )                          
 - [ o ] "   " 상수
 - [ o ] " o " 상수
 - [ o ] " x " 상수
 - [ o ] "]", "[", , "|" 상수
 - [ o ] 어느다리로 갈건지, 거기로 갈수있는지 변수를 받아서 윗다리와, 아랫다리에 각각의 값을 넣어준다.
 - [ o ] 어느다리로 가는지 확인하고 안가는 다리엔 empty를 넣어준다.
 - [ o ] 가는 다리가 갈수 있는지 못가는지에 따라서 o,x를 넣어준다.
 - [ o ] 다리모양 초기화
 - [ o ] "|" 사용하여 구분한다.
 - [ o ] "]", "[" 감싼다.

# OutputView (출력 문 클래스)                                                           

# Verification ( 검증 클래스 )
- [ o ] 3 이상 20이하 인가
- [ o ] U, D 둘 중 하나 인가
- [ o ] R, Q 둘 중 하나 인가

# GameControll (게임을 전반적으로 컨트롤 하는 요소들이 모여있는 클래스)
- [ o ] cnt -> 게임을 몇번 시도했는지
- [ o ] idx -> 몇번째 다리를 건너는지 -> idx ==  size 일때 게임 성공
- [ o ] gamePower -> 게임 전원 버튼 -> 게임성공, 실패 시 게임의 반복문 끄는 역할
- [ o ] gameSucessWheter -> 게임에 성공했는지
- [ o ] 위 요소들 초기화
- [ o ] cnt, idx 1씩증가하는 메서드

# GameRest (게임에 필요한 요소들 리셋 시켜주는 클래스 (리셋버튼))
- [  ] idx, canMove, gamePower 리셋 기능



# 패키지
# domain - 비즈니스에 관련된거 - BridgeMaker, ...
- 클래스
- BridgeGame - 다리를 건널 수 있는지 , 다시 게임 시작할건지 판별해주는 클래스
- BridgeMaker - 다리를 만들어주는 클래스
- BridgeNumberGenerator
- BridgeRandomNumberGenerator

# model 
- 클래스
- Bridge
- BridgeShape
- GameControll

# view
- 클래스
- InputView
- OutputView
- 
# controller - view와 model를 이어주는 패키지
- BridgeSize -> size를 입력받아서 다리를 만든다.
- BridgeMove -> 어디로 갈지 입력 받고 처리한다.
- BridgeRetry -> 다시시작할지 입력 받고 처리한다.
- GameController -> 전반적으로 게임 진행을 해주는 역할.
- GameResultPrint -> 게임의 다리 모양, 최종 결과를 출력해주는 역할

# service
- valification
- constants(Command, Error, Move)