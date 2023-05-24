# BigData
BigData work
정규 표현식이라?
문자열 패턴을 표현하고 검색, 대체, 분할, 매칭 등의 작업을 수행하는 강력한 도구입니다. 파이썬에서는 re 모듈을 사용하여 정규표현식을 다룰 수 있습니다.

정규표현식은 다양한 메타문자와 특수 시퀀스를 사용하여 문자열의 패턴을 표현합니다. 몇 가지 주요한 것들은 다음과 같습니다

    . (점): 어떤 문자 하나와 매치됩니다.
    *: 앞의 패턴이 0번 이상 반복되는 부분과 매치됩니다.
    +: 앞의 패턴이 1번 이상 반복되는 부분과 매치됩니다.
    ?: 앞의 패턴이 0번 또는 1번 등장하는 부분과 매치됩니다.
    ^: 문자열의 시작과 매치됩니다.
    $: 문자열의 끝과 매치됩니다.
    []: 대괄호 안의 문자들 중 하나와 매치됩니다.
    |: 둘 중 하나의 패턴과 매치됩니다.
    () : 그룹을 나타내며, 그룹에 매치된 문자열을 추출할 수 있습니다.
   
정규 표현식 기본 사용 방법

    1.정규표현식 패턴 컴파일하기: 정규표현식을 사용하기 전에 먼저 패턴을 컴파일해야 합니다. re.compile() 함수를 사용하여 패턴을 컴파일할 수 있습니다.
      컴파일된 패턴 객체를 반환하고 이를 사용하여 패턴 매치 작업을 수행합니다.
      
      import re
      pattern = re.compile(r"패턴")
      
    2.문자열 매치 검사하기: 주어진 패턴이 문자열과 매치되는지 확인하기 위해 re.match() 또는 re.search() 함수를 사용할 수 있습니다.
      re.match(pattern, string): 문자열의 시작 부분부터 패턴과 매치되는지 확인합니다.
      re.search(pattern, string): 문자열 전체를 검색하여 패턴과 매치되는지 확인합니다.
      
      import re
      pattern = re.compile(r"apple")
      text = "I have an apple."
      // match 메서드를 사용하여 문자열의 시작 부분부터 매치 검사
      match = pattern.match(text)
      if match:
      print("매치되었습니다!")

      //search 메서드를 사용하여 문자열 전체를 검색하여 매치 검사
      match = pattern.search(text)
      if match:
      print("매치되었습니다!")
      
    3.매치된 결과 얻기: re.match() 또는 re.search() 메서드를 사용하여 매치된 결과를 얻을 수 있습니다. match.group() 메서드를 사용하여 매치된 부분 문자열을 추출할 수 있습니다.
   
      import re
      pattern = re.compile(r"(\d+)-(\d+)-(\d+)")
      text = "Date: 2023-05-24"

      match = pattern.search(text)
      if match:
      year = match.group(1)
      month = match.group(2)
      day = match.group(3)
      print(f"Year: {year}, Month: {month}, Day: {day}")
      
   4.패턴 대체하기: 문자열 내에서 패턴과 일치하는 부분을 다른 문자열로 대체하려면 re.sub() 함수를 사용할 수 있습니다.
     
     import re
     pattern = re.compile(r"apple")
     text = "I have an apple. It's an apple tree."
     replaced_text = pattern.sub("orange", text)
     print(replaced_text)
     
      
    
    

