[[ 고객정보관리시스템 ]]

1. 고객이 할 일을 부여받는다.
    I - 고객 정보 입력
    C - 현재 고객 정보 조회
    P - 이전 고객 정보 조회
    N - 다음 고객 정보 조회
    U - 고객 정보 수정
    D - 고객 정보 삭제
    Q - 프로그램 종료
    
2. 입력
- I : input
- 고객정보 :  이름, 성별, 이메일, 출생년도를 딕셔너리에 입력받는다.
- 이름 
> 제약조건 : 이름의 최소글자수와 최대글자수  
> 이름의 글자수 제한에 관한 이유 : 가장 긴 이름으로는 ‘박 하늘별님구름햇님보다사랑스러우리’(17자)  
원문보기: 
http://www.hani.co.kr/arti/society/society_general/399615.html#csidxdf72b571760f66eb89e6145c0fb803c   
> 이름에 들어갈 수 있는 데이터의 종류
- 성별
> F, f, M, m으로 성별 받는다.
> 제약조건 : 숫자, 한글, f와 m을 제외한 다른 문자가 들어왔을 때 오류안내 후 다시 입력받아야함
- 이메일
> 고객정보의 고유한 조건으로 사용한다.  
> 제약조건 : 이메일의 형식인 a@a을 만족해야한다. 아닐시 오류안내 후 다시 입력 
> 이메일이 중복되는것인지 확인하는 로직 추가  
- 출생년도
> 제약조건 : 출생년도의 4자리를 입력받아야한다. 아닐시 오류안내 후 다시 입력  
> 숫자만 들어가야한다. 다른 문자가 들어가면 오류출력  
- 고객정보를 모두 입력받으면 고객정보리스트에 삽입한다.  
- 고객정보를 입력받을 시 인덱스도 1씩 증가시킨다.  

3. 조회 
3-1. C : 현재 정보 조회 
- 고객정보 입력받을 시 증가된 인덱스를 이용하여 현재 정보를 조회한다.  
> 인덱스명 : page  
3-2. P : 이전 정보 조회
- 현재 정보의 인덱스를 이용해 이전 정보를 조회한다.  
> page -= 1  
> 제약조건 : 현재정보가 첫번째 정보일 경우 이전 정보를 조회할 수 없다는 오류안내  
3-3. N : 다음 정보 조회 
- 현재 정보의 인덱스를 이용해 다음 정보를 조회한다.  
> page += 1  
> 제약조건 : 현재정보가 마지막 정보일 경우 다음 정보를 조회할 수 없다는 오류안내  

4. 삭제
- D : delete
- 고객에게 삭제하고자하는 고객정보의 이메일을 입력받음. 
- 이유 : 이메일이 고유한 값이라서
- 고객리스트에서 입력받은 이메일이 있는지 검토 후 그 정보가 있는 위치(i)를 찾는다.
- 찾은 위치를 이용해 삭제
> del custlist[i]
- 삭제 후 그 고객정보를 삭제했는지 플래그변수에 저장
> 제약조건 : 입력받은 이메일이 존재하지 않는 경우 등록되지 않은 이메일이라는 오류안내

5. 수정
- U : update
- 고객에게 수정하고자하는 고객정보의 이메일을 입력받음
- 고객리스트에서 입력받은 이메일이 있는지 검토 후 그 정보가 있는 위치(idx)를 찾는다.
- name, sex, birthyear 중 어떤 정보를 수정할 건지 입력받는다. 
- idx 위치의 고객정보에 고객에게 입력받은 수정값을 저장한다.
> 제약조건 : 입력받은 이메일이 존재하지 않는 경우 등록되지 않은 이메일이라는 오류안내
>           수정할 항목을 입력받을 시 name, sex, birthyear 중 다른 항목을 입력하면 존재하지 않는 항목이라는 오류안내

6. 종료
- Q : quit
- Q를 입력받으면 고객정보프로그램을 종료한다.


7. 수정사항
- 현재 절차적으로 작성된 프로그램을 함수를 사용하여 각 기능을 분리시킨다.
