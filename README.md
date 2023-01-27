# markdown_20230127
마크다운 설명
### 11. 표
|번호|아이디|이름|레벨|이메일|등록일|
|:--------|:--------|:----------|--------:|:------------------|:-----------:|
|1        |james1    |이상무1    |1        |sangmoo1@gmail.com|2023-01-27   |
|2        |james2    |이상무2    |1        |sangmoo2@gmail.com|2023-01-27   |
|3        |james3    |이상무3    |1        |sangmoo3@gmail.com|2023-01-27   |
|4        |james4    |이상무4    |1        |sangmoo4@gmail.com|2023-01-27   |
|5        |james5    |이상무5    |1        |sangmoo5@gmail.com|2023-01-27   |

### 10. 인라인
문단 중간에 `CODE` 를 넣을 수 있습니다.(고정 폭 폰트를 표시해야 할 때 사용)  
예를 들어 `question_list = Question.objects.order_by('-create_date')`처럼


### 9. 강조
**spring**을 만끽하세요.  
spring을 만끽하세요.
*벚꽃*이 만개하는 계절이니까요.


### 8. 이미지 넣기
![파이참](https://github.com/oyunmintrio95/markdown_20230127/blob/main/doc/img_pycharm.png "파티참 툴팁")

### 7.하이퍼링크
[e클래스](https://cafe.daum.net/pcwk "e클래스의 cafe입니다.")

### 6. 가로 라인
---
***
------

### 5. 코드블록
```
def index(request):
    '''question 목록'''
    # Question.objects.order_by('create_date') #=>ASC
    print('index 레벨로 출력')
    #list order create_date desc
    question_list = Question.objects.order_by('-create_date') # order_by('-필드')=>DESC
    # question_list = Question.objects.filter(id=99)
    context = {'question_list':question_list}
    print('question_list:{}'.format(question_list))

    return render(request,'pybo/question_list.html',context)
```

### 4. 목록
1. 아이템1
2. 아이템2  
  a. 1단계 하위 아이템  
    1) 2단계 하위 아이템 
9. 아이템3

- 아이템 1
+ 아이템 2
  - 1단계 하위 아이템
    * 2단계 하위 아이템
      * 3단계도 있어?

순서 없는 목록  
* 목록이름
  * 상세 목록
    * 상세상세목록 
  * 상세목록
- 목록
+ 목록

순서 있는 목록
1. 목록이름
2. 목록
3. 목록 3번

### 3. 인용문
> 여기에 인용할 내용을 넣으면 됩니다.  
> 빈 줄이 없으면 자동으로 인용 상자에 포함이 됩니다.

### 2. 헤더
# 헤더1
## 헤더2
### 헤더3
#### 헤더4
##### 헤더5

### 1. 문단 구분을 위한 개행.
문단을 작성 합니다.(개행 공백 두개)  
겨울이 가고 봄이 옵니다.
