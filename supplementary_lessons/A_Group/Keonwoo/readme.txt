gameapi 개발
예시 사이트 : http://api.gevolution.co.kr/rank/xml/?aCode=HIJK372129&market=g&appType=game&rankType=1&rank=20
게임 API사이트 : http://www.gevolution.co.kr/geconts/geApi.asp


방향성 설정 : 나는 어떤 gameapi 정보 사이트를 개발할 것인가?
-> 1.나는 gameapi 정보를 고객들에게 제공해주는 game api 홈페이지 사이트를 만들것이다
-> 2.데이터 베이스에 각종 정보들을 저장한것을 보여주기만 하면된다
-> 3.실시간 ( 최소 1시간 단위) 정보가 저장되어야한다
-> 4.저장된 정보를 내 나름대로 가공하여서 고객들이 보기쉽게 제공할 수 있어야 한다 **
-> 5.홈페이지로 연결할 수 있어야한다
-> 6.홈페이지에서는 앱평가 점수 순, 이번주 순위 순으로 볼 수있도록 접근가능하게 해야한다
-> 7.홈페이지에는 이름/앱 대표 아이콘의 이미지 URL/순위/공식 URL 등이 표시 되어야한다.

gameapi홈페이지에서 gameapi 정보를 받아온다

gameapi를 받아온 것을 데이터 베이스에 저장한다

gameapi 데이터베이스 저장하는 함수는 이미 개발하였다 //2번 완료

이제 gameapi에 있는 데이터베이스를 조회하는 함수를 개발하여한다.?

3번의 실시간 저장도 이미 개발하였다
###############################################################################################
앞으로 개발해야할 항목들

4. 저장된 정보를 고객들이 보기쉽게 하는것을 오늘의 목표로 잡는다.
-> 상위 10개 항목들에 한하여 지난 일/주간 순위 비교를 하게 해주는 matplot 표를 작성한다
-> 그표를 저장하고 실시간으로 보여 줄 수 있도록 한다.
###############################################################################################

데이터들의 특성을 한번 더 유심하게 보고 어떤 특성을 가지는지 다시한번 확인한다

데이터들을 다시보자

============================================
이번주 (11-4 ~ 11-10일까지) 해결할 사항 --> 데이터 정제 및 어떤 데이터 표시 해줄것인지, 전처리까지 완료하기


2018-11-3
고객이 원하면 
1. 우선 고객에게 물어본다 . 
 ==> 구글 앱스토어 용, 애플 앱스토어 용 중 어떤 결과를 원할것인지 물어봄 
 ==> 답에 따라서 해당 결과를 제공
 
2. 무료/유료/매출 순위로 게임 데이터를 제공한다.

무료의 차트 제공
유료의 차트 제공
매출순위에 따른 차트 제공

==> 차트를 어떤 순서로 제공할 것인가


<<<<<<<<<<<<<   자동적재 방법   >>>>>>>>>>>>>>>>>>>>

1.Batch 파일 생성
--> 배치파일을 생성하면 , 파이썬 파일 오픈과 동시에 자동적재가 하게 된다 ==> 자동으로 실시간 데이터를 적재할 수 는 없다.
--> 


2.ubuntu 진입

--> 이것이 ubuntu에서 진입하는것이다는 것을 인지하면 ==> 자동 적재 허락
    
    ubuntu에서 자동적재를 하는데 끌수도 있어야한다.==????
    ON/OFF를 할 수 있는 MENU를 만든다
    => console을 통해서 key(parameter  auto = 0 or 1)를 주어서 자동 적재를 ON/OFF한다
    
    2-1 우분투 내 자동 적재 방법 _ 첫번째
    => ubuntu에서 돌리는 파일을 gameapi_API_dev로 한뒤, 접근하는 경로(os.path)가 ubuntu이면 자동적재 ==> 종료하는 OFF만들기 힘듬 => X
    => 실패

    2-2 우분투 내 자동 적재 방법 _ 두번째
    => ubuntu에서 gameapi_MENU_dev로 실행파일을 설정한 뒤 접근하는 경로가 ubuntu이면 
    예시 ) if = 접근하는 경로가 ubuntu이면 :
                if input =1 :
                    gameAPI_API_dev.insertdata()
                else :
                    sys.exit()


    ubuntu에서 자동적재 외에도 콘솔로도 적재할 수있어야한다.





<<<<<<<<<<   추후의 고려 사항들 >>>>>>>>>>>>>>>>>>>>


5. 홈페이지에 연결한다. 홈페이지에서는 저장된 정보들을 실시간으로 업데이트 해 줄 수 있도록 작성해본다

6. 홈페이지에 html을 작성하여서 1위부터 약20위까지의 순위를 모두 조회할 수 있도록한다
   앱평가 점수 순// 이번주 순위 순으로 2가지 항목에 관하여 접근 할 수 있도록 한다

7. 홈페이지를 design함에 있어서 기존에 제공받은 이미지 URL/순위/공식 URL들이 자동으로 업로드 되도록 함수를 
   작성한다
   
 
 
 =>> 모든 함수들에있어서 원칙: 업데이트가 실시간으로 되는 프로그램 
 --  절대로 update시에 개발자인 내가 건드리지 않아도 모든 프로그램들과 함수들이 
     자동으로 업데이트되고 표를 제공/ 홈페이지가 업데이트 되도록 작성한다.




조회 메뉴를 개발한다 -> >????


