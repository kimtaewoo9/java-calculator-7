# java-calculator-precourse

# Calculator 프로그램 🧮

입력된 문자열에서 **구분자로 구분된 숫자를 파싱하고 숫자의 총합을 반환하는 계산기 프로그램**입니다. 쉼표(,)와 콜론(:)을 기본 구분자로 사용하며, 사용자 정의(커스텀) 구분자도 지원합니다.

---

## **프로그램 기능 구현 목록**

1. **숫자 합산 기능** ➕
   - 구분자와 숫자로 구성된 문자열에서 숫자를 파싱하여 총합을 구합니다.(더하기만 가능)
     - ex) "1,2:3" → 6

2. **사용자 정의(커스텀) 구분자 추가 기능** 🛠️ 

   - 쉼표(,)와 콜론(:)을 기본 구분자 외에 사용자가 정의한 구분자를 사용할 수 있습니다.
   - 사용자 정의 구분자는 `"//[구분자]\\n[숫자]"` 형식으로 지정할 수 있습니다.
     - ex) "//;\n1;2;3" → 6

4. **예외 처리** ❌❌

   **숫자 부분 입력이 잘못된 경우**
   - 숫자 부분이 입력되지 않은 경우
     - ex) "//;\n1;2;"
   - 입력된 문자열이 빈 문자열일 경우 `0`을 반환합니다.
     - ex) "" → 0
   - 숫자가 너무 큰 경우 예외 발생
     - ex) "0x7fffffff", "2,147,483,647"가 넘어가는 숫자
   -  구분자 사이에 숫자가 아닌 값이 들어온 경우 예외 발생
     - ex) "1;!;2"

  
   **커스텀 구분자의 입력이 잘못된 경우**
   - 커스텀 구분자가 숫자로 들어올 경우 예외 발생
     - ex) "//0\n10203"
   - 커스텀 구분자 입력이 두개 이상의 문자로 들어왔을때
     - ex) "//!!\n"
   - 커스텀 구분자의 입력으로 기본 구분자 ",|:" (쉼표, 콜론) 가 들어온 경우.
     - ex) "//,\n1,2"
   - // 커스텀 구분자의 입력 없이 바로 \n이 오는 경우
     - ex) "//\n1"
   
   
---

