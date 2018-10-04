# PNU_INGRO -> 숫자 맞추기 게임 RFP

## 1. 주요 내용
지금 까지 배운 내용을 토대로 AI 숫자 맞추기 게임을 만듭니다.  
AI가 제시하는 1 ~ 100 사이의 숫자를 추론하여 맞추는 게임 기능을 구현 합니다.  
총 시도 횟수를 기준으로 점수를 구하고 누적 총 합을 구합니다.  
콘솔 모드에서 진행 합니다.  

## 2. 요구사항 - 데이타
게임 정보는 __게임 제목__, __게이머 이름__, __게임 점수__, __총 누적 합__ 이 있습니다.  
25자 이내의 게임 제목과 게이머 이름을 입력받아 본인이 선택한 자료구조에 저장해야 합니다.  
매 게임의 획득 점수와 총 누적 점수를 저장해야 합니다.  

## 2. 요구사항 - 기능
. __게임 정보 입력__
1. 프로그램이 구동되면 "게임의 제목 입력" 이라고 출력됨  
2. 입력하지 않고 엔터를 치면 오류를 출력하고 다시 입력을 요청한다.  
3. 입력한 게임의 제목이 25자를 넘으면 오류를 출력하고 다시 입력을 요청한다  
4. 입력을 받으면 아래처럼 정렬하여 출력  
'''
==================
=   게임 제목   ==
=   v1.0.0      ==
==================
'''
5. 게이머의 이름을 입력받는다 (프럼프트:게이머의 이름을 입력하세요)  
6. 입력않하면 오류  
* * *
. __게임 시작__
7. (프럼프트:0~99사이의 값으만 AI의 값을 예측하여 입력하세요)  
8. 공백을 넣으면 오류  
9. 숫자가 아니면 오류  
10. 값의 범위를 넘으면 오류  
11. 값이 작으면 작다고 출력하고 다시 입력받음  
12. 값이 크면 크다고 출력하고 다시 입력받음  
13. 시도 횟수를 기록  
14. 최종 값을 맞추면 총 x번 시도만에 맞췄다고 출력하고  
    다시 게임을 할것인지 물어본다 다시하면 7번부터 시작  

_* 최종 버전은 객체지향 개념을 적용하여 확장성을 고려한 애플리케이션이 되도록 해야 합니다._