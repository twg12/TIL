# HW4

1. 수정 사항: range를 적을 경우, 두번째 숫자를 하나 높여서 올려야한다는 것! (a, b)일 경우 a는 이상, b는 미만을 뜻함

```py
class_scores = [{'국어': 80, '영어': 100, '수학': 50}, {'국어': 90, '영어': 70, '수학': 40}]

def grade(class_scores):
    if class_scores in range(81, 101):
        return 'A'
    elif class_scores in range(61, 81):
        return 'B'
    elif class_scores in range(41, 61):
        return 'C'
    elif class_scores in range(21, 41):
        return 'D'
    else:
        return 'F'
```

```py
from grades import grade

def test_grade():
    assert grade(80) == 'B'
    assert grade(100) == 'A'
    assert grade(60) == 'C'
    assert grade(0) == 'F'
```
