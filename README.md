# BigData
BigData work
정규 표현식이라?
문자열 패턴을 표현하고 검색, 대체, 분할, 매칭 등의 작업을 수행하는 강력한 도구입니다. 파이썬에서는 re 모듈을 사용하여 정규표현식을 다룰 수 있습니다.

정규표현식은 다양한 메타문자와 특수 시퀀스를 사용하여 문자열의 패턴을 표현합니다. 몇 가지 주요한 메타문자와 특수 시퀀스는 다음과 같습니다:

    . (점): 어떤 문자 하나와 매치됩니다.
    *: 앞의 패턴이 0번 이상 반복되는 부분과 매치됩니다.
    +: 앞의 패턴이 1번 이상 반복되는 부분과 매치됩니다.
    ?: 앞의 패턴이 0번 또는 1번 등장하는 부분과 매치됩니다.
    ^: 문자열의 시작과 매치됩니다.
    $: 문자열의 끝과 매치됩니다.
    []: 대괄호 안의 문자들 중 하나와 매치됩니다.
    |: 둘 중 하나의 패턴과 매치됩니다.
    () : 그룹을 나타내며, 그룹에 매치된 문자열을 추출할 수 있습니다.
    
    
    
코드 예제
import re
// 문자열 매치
pattern = r"apple"
text = "I have an apple"
match = re.search(pattern, text)
if match:
    print("매치되었습니다!")
else:
    print("매치되지 않았습니다.")

// 패턴 추출
pattern = r"(\d+)-(\d+)-(\d+)"
text = "Date: 2023-05-24"
match = re.search(pattern, text)
if match:
    year = match.group(1)
    month = match.group(2)
    day = match.group(3)
    print(f"Year: {year}, Month: {month}, Day: {day}")

// 패턴 대체
pattern = r"apple"
text = "I have an apple. It's an apple tree."
replaced_text = re.sub(pattern, "orange", text)
print(replaced_text)

// 패턴 분할
pattern = r"\s+"
text = "Hello    World"
splitted_text = re.split(pattern, text)
print(splitted_text)
