# Physics-Coding
1주차 2차시입니다.
본 강의에서는 GlowScirpt를 이용하여 벡터를 표현하고 연산하는 것을 배웁니다.
여러분은 화살표 오브젝트(Object)를 이용하여 좌표축을 만들고, 벡터의 연산을 직접 표현해 볼 수 있습니다.
아래 영상의 재생 버튼을 클릭하여 학습을 시작하세요.

▶ 7분 44초 ~ 8분 40초 사이에 동영상에서 게시된 코드 중 일부에 오타가 있습니다.
     b_arrow의 pos=a 이어야 하니 참고 하시기 바랍니다.

< 1주차-1차시 코드 추가 설명 >

▶ # 으로 시작하는 문장은 주석으로 처리되며 컴퓨터가 계산하지 않는다.

▶ myBall = sphere()
  - myBall : 사용자 정의 변수 이름
  - sphere() : 구 객체를 생성하는 함수
  - 객체 생성 함수를 통해 생성한 객체는 반드시 변수에 저장해야 그 이후의 코드에서 생성한 객체를 사용할 수 있음
  - 객체 생성 함수의 괄호 안을 비어두면 객체의 속성이 기본값으로 설정되어 생성됨
  - 모든 함수는 항상 소괄호 () 가 붙음

▶ sphere()
  - 구 객체를 생성하는 함수
  - sphere(pos = vec(0, 0, 0), color = color.red, radius = 2)
    pos : 객체의 위치(x, y, z)를 설정하는 속성
    color : 객체의 색상을 설정하는 속성
    radius : 객체의 반지름을 설정하는 속성

▶ box()
  - 상자 객체를 생성하는 함수
  - myBox = box(pos = vec(5, 0, 0), color = color.blue, size = vec(0.5, 4, 1))
    pos : 객체의 위치(x, y, z)를 설정하는 속성
    color : 객체의 색상을 설정하는 속성
    size : 객체의 크기(가로, 세로, 깊이)를 설정하는 속성

▶ myBall.color = color.green
  - myBall 이라는 객체를 생성하고, 그 이후의 코드에서 myBall의 속성들을 .을 이용해 변경할 수 있음


< 1주차-2차시 코드 추가 설명 >
▶ r = vector(3, 4, 5)
  - 벡터를 생성하는 함수
  - 생성한 벡터는 변수에 저장해야 이후의 코드에서 사용할 수 있음

▶ r_arrow = arrow(pos = vector(0, 0, 0), axis = r, color = color.red, shaftwidth = 0.2)
  - 화살표 객체를 생성하는 함수
  - pos : 화살표의 시작점
  - axis : 화살표의 끝점
  - shaftwidth : 화살표의 굵기

▶ mag(r)
- 벡터 r의 크기(길이)를 계산해서 반환하는 함수

▶ norm(r)
- 벡터 r의 단위 벡터를 계산해서 반환하는 함수

▶ print()
- 화면에 글자를 출력하는 함수
- 괄호를 비어두면 엔터(줄바꿈)을 출력
- print("r : ") : 따옴표 안의 글자는 작성된 그대로 출력
- print(r) : 변수의 값을 출력



#################################################################################################################

< 2주차-2차시 코드 추가 설명 >

▶ attach_arrow(ball, "v", shaftwidth = 0.1, color = color.green)
  - 객체에 화살표를 붙여주는 함수
  - ball : 화살표를 붙일 객체 변수 이름
  - "v" : 화살표의 크기에 반영되는 객체의 속성 이름

▶ scene.waitfor('click')
  - 객체가 그려지는 화면을 scene 이라고 함
  - 첫번째 줄부터 코드를 실행하다가 해당 함수를 만나면 마우스 클릭이 있을 때까지 다음 코드 실행 안함

▶ while t < 4:
  - 같은 코드를 반복하고 싶을 때 사용
  - while 키워드 바로 오른쪽에는 조건(예시에서는 t < 4)을 작성하며 조건이 참인 동안에는 while문 안의 코드를 반복해서 수행
  - 조건이 거짓이 되면 while문 탈출해 while문 다음의 코드를 수행
  - 조건(예시에서는 t < 4) 오른쪽에는 반드시 콜론(:)이 적혀야 함 (콜론이 없을 경우 문법 오류 발생)
  - while의 w를 기준으로 들여쓰기 된 코드만 while문 안에 포함된 코드로 인식



######################################################################################################

< 3주차-1차시 코드 추가 설명 >

▶ attach_trail(ball, type = 'points', pps = 5)
  - 객체의 자취를 그려주는 함수
  - ball : 자취를 그릴 객체
  - type : 자취의 type 설정
  - pps : 점을 몇초마다 그릴 것인지

< 3주차-2차시 코드 추가 설명 >

▶ motion_graph = graph(title = 'position-time', xtitle = 't', ytitle = 'y')
  - 그래프 생성 함수
  - title : 그래프 이름 설정
  - xtitle : x축 이름 설정
  - ytitle : y축 이름 설정

▶ g_bally = gcurve()
  - 그래프의 데이터를 그리는 함수

▶ g_bally.plot(pos(t, ball.pos.y))
  - 그래프에 새 데이터를 추가해 그리는 함수

< 3주차-3차시 코드 추가 설명 >

▶ rList = list()
  - 리스트를 생성하는 함수
  - 괄호 안을 비어두면 비어 있는 리스트를 생성함

▶ rList.append(vec(0, -4, 0))
  - append : rList 리스트에 데이터를 추가하는 함수
  - 리스트 객체에서만 사용할 수 있는 함수로 반드시 리스트객체이름.append() 와 같이 사용해야 함

▶ for i in range(0, 100):
  - while문과 같은 반복문
  - range(0, 100) : 0~99까지 총 100개의 숫자로 구성된 리스트를 반환
  - i 변수에 range() 함수를 통해 반환된 리스트의 숫자를 하나씩 반환해서 저장, 더이상 반환할 숫자가 없으면 반복문 종료
  - while문과 같이 for 키워드가 적힌 문장 제일 오른쪽에는 콜론(:)이 있어야 함(없으면 문법 오류 발생)

▶ for r in rList:
  - rList에 저장되어 있는 데이터(예시에서는 벡터)를 하나씩 반환해서 r에 저장

▶ objList.append(shpere())
  - 리스트의 데이터는 객체도 가능

######################################################################################################
< 4주차 코드 추가 설명 >

# Simulation Loop

while True:
    # while 반복문 시작
    rate(1000)    

    # Forces
    r = Earth.pos - Moon.pos
    Moon.f = G*Earth.mass*Moon.mass/mag(r)**2*norm(r)
    Earth.f = -Moon.f 
        # 연산자
        # 곱하기 * : 2*3 = 6
        # 제곱 ** : 2**3 = 8

    # Time Integration
    Moon.v = Moon.v + Moon.f/Moon.mass*dt
    Earth.v = Earth.v + Earth.f/Earth.mass*dt
    Moon.pos = Moon.pos + Moon.v*dt
    Earth.pos = Earth.pos + Earth.v*dt
    t = t + dt    

    # Collision Check
    if Earth.radius + Moon.radius > mag(r):
        print("Collision!")
        print(t/60/60/24, "days")
        break
            # break : 반복문(while, for)을 종료 시키는 문장
            # continue : 반복문 안에서 해당 문장 아래의 문장들은 수행하지 않고 다음 반복으로 넘어가게 하는 문장
            # 반복문 안에서만 사용 가능

    # while 반복문 끝

