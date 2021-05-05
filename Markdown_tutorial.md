# Markdown Syntax 

## **< Heading ; 제목 >**
>  `# heading level 1`
>  `## heading level 2`
>  `### headling level 3`
- 제목은 1~6까지 6개의 단계가 존재

- 1->6 으로 갈 수록 글자의 크기 감소

- **#의 수**는 **사용하려는 제목의 단계**와 일치해야함


> `Heading level 1`
> `==================`
> `Heading level 2`
> `------------------`

- 대체구문 ) 1단계 제목의 경우 텍스트 아래줄에 '=' 문자 1개 이상 추가
- 대체구문 ) 2단계 제목의 경우 텍스트 아래줄에 '-' 문자 1개 이상 추가
>
>
    ※ 주의
    기호 # 와 제목 이름 사이에 '공백'을 두어라

> # heading level 1
> ## heading level 2
> ### heading level 3
> #### heading level 4
> ##### heading level 5
> ###### heading level 6

## **< Paragraphs ; 단락 >**
> I am a student at Soongsil University..
>
> Soongsil University is located in Dongjak-gu, Seoul.
- **빈 줄**을 사용하여 하나 이상의 텍스트 줄 구분
>
>
    ※ 주의
    목록에 단락을 내는 경우가 아니라면 단락 앞에 탭이나 공백을 사용하지 않음

## **< Line Breaks ; 줄바꿈 >**
> First line with two spaces after.
And the next line.
- 앞 문장의 **맨 뒤**에 **두 개 이상의 공백**을 추가
>First line with the HTML tag after.`<br>`
And the next line.
- 앞 문장 끝에 `<br>` 을 입력
>
>
    ※ 권장하지 않는 두 가지 옵션
        1. 줄 끝에 슬래시(\) 입력
            - 모든 Markdown 응용프로그램이 지원하는 것이 아니라 권장 X
>
## **< Emphasis ; 강조 >**
- 텍스트를 Bold체나 Italic체로 변경 가능

    ### < Bold ; 굵은 체 >
    > This is a bold type `**with an asterisk**`.
    > This is a bold type **with an asterisk**.

    > This is a bold type `__with an underscore__`.
    > This is a bold type __with an underscore__.

    > Its`**MIDDLE**`bold.
    > Its**MIDDLE**bold.

    - 단어나 구문 **앞 뒤**에 **2개의 별표나 밑줄**을 추가
    - 단어 **중간**을 굵게 표시하려면 문자 주위에 **공백 없이 별표 두개** 추가
    >
        ※ 주의
        Markdown은 단어 중간에 있는 밑줄을 처리하지 않음
        -> 별표 사용하기

    ### < Italic ; 이탤릭 체 >
    > This is an Italicized text type `*with an asterisk*`.
    > This is an Italicized text type *with an asterisk*.

    > This is an Italicized text type `_with an underscore_`.
    > This is an Italicized text type _with an underscore_.

    > Its`*MIDDLE*`Italicized.
    > Its*MIDDLE*Italicized.

    - 단어나 구문 **앞 뒤**에 **1개의 별표나 밑줄**을 추가
    - 단어 **중간**에 기울임 꼴을 표시하려면 문자 주위에 **공백 없이 별표 1개** 추가
    >
        ※ 주의
        Markdown은 단어 중간에 있는 밑줄을 처리하지 않음
        -> 별표를 사용

     ### < Bold and Italic ; 굵은 체와 이텔릭 체 >
     - 굵은 체와 이텔릭 체를 동시에 사용 가능
     - 단어나 구문 앞 뒤에 별표 또는 밑줄을 3개 추가
        - 별표와 밑줄을 합쳐서 3개
    >
        ※ 주의
        밑줄 3개(___)는 사용하지 않는 것이 좋음

## **< Blockquotoes ; 인용구 >**
- **단락 앞**에 `'>'`를 추가
`>` In fact, I am using the quotation box as an example box :).
> In fact, I am using the quotation box as an example box :).

- 여러 단락이 있는 인용구에서는 **단락 사이의 빈줄**에 `'>'` 추가
`>` first block.
`>`
`>` second block.

> first block.
>
> second block.

- 중첩인용구
    - 인용구는 중첩이 가능
    - **중첩하려는 단락 앞**에 `'>>'` 추가

`>` This is nested blockquotoes.
`>`
`>>` hello blockquotoes

> This is nested blockquotoes.
>
>> hello blockquotoes

## **< Lists ; 리스트 >**
- 항목을 정렬 된 목록과 정렬되지 않은 목록으로 구성할 수 있음

    ### < Ordered Lists ; 정렬 된 리스트 >
    > 1. First item
    > 2. Second item
    > 3. Third item

    - 정렬 된 목록을 만드려면 **숫자 뒤에 마침표**가 있는 항목 추가
    - 마침표 뒤에 공백 필요
    - 숫자는 순서대로 쓸 필요는 없지만 **반드시 1**로 시작
    >
        ※ 주의
        1) 2) 는 모든 응용 프로그램에서 지원하는 것은 아니기 때문에 마침표를 사용하는 것이 좋음

    ### < Unordered Lists ; 정렬 되지 않은 리스트 >
    > `-` First item.
    > `-` Second item.
    > `-` Third item.
    - 라인 항목 앞에 `'-'` 나 `'*'` 나 `'+'` 를 추가
    - 중첩이 가능
    >
        ※ 주의
        동일한 목록에서 구분 기호를 혼합하지 않음
        하나를 선택하고 그대로 유지
    - 목록의 연속성을 유지하면서 목록에 **다른 요소를 추가**하려면 **공백 4개또는 탭 1개** 추가

## **< Code Blocks ; 코드 블럭 >**
- 코드 블럭은 일반적으로 공백 4개 또는 탭 1개로 들여 씀
- 목록 안에 있는 경우 공백 8개 또는 탭 2개 들여 씀

## **< Code ; 코드 >**
- 단어나 구를 코드로 표시하려면 백틱으로 묶음
- 백틱 ( ` )
    - < Escaping Backticks ; 백틱 탈출 >
        - 코드로 표시하려는 단어나 구에 백틱이 하나 이상 포함되어있는 경우 단어나 구를 이중 백틱으로 묶을 수 있음

## **< Horizontal Rules ; 수평선 >**
> `***`
>`--------`
>`________________`
- 수평선을 만드려면 **3개** 혹은 **그 이상**의 **별표 또는 대시 또는 밑줄**을 **한 줄에 단독**으로 추가
>
    ※ 주의
    수평선 규칙 앞 뒤에 빈 줄을 넣어야 함

## **< Images ; 이미지 삽입 >**
> ![대체 텍스트](이미지 경로 또는 소스 URL "이미지 설명")

> `![ImageInsertTest](soongsil.jpg)`
> ![ImageInsertTest](soongsil.jpg)
- !를 추가한 다음 [ ]괄호 안에 대체 텍스트를 추가하고 ( )괄호 안에 이미지의 경로 또는 URL 추가
- 선택적으로 " " 안에 설명 추가 가능
    - 마우스를 이미지에 가져갈 시에 뜨는 텍스트
    ### < Linking Images ; 이미지에 링크 삽입>
    > [![대체 텍스트](이미지 경로 또는 소스 URL "이미지 설명")](링크 주소)

    - 이미지에 링크를 추가하려면 마크 다운을 괄호로 묶은 다음 링크를 괄호로 추가

## **< Links ; 링크 삽입 >**
1. URL을 직접 입력하는 방법
> `<주소>`
> `<Email주소>`

> `<http://www.ssu.ac.kr/>`
> < http://www.ssu.ac.kr/>
> `<lucy9480@gmail.com>`
> <lucy9480@gmail.com>
>
2. 텍스트에 링크를 삽입하는 방법
> `[텍스트](주소)`

> `[Soongsil University]( http://www.ssu.ac.kr/)`
> [Soongsil University]( http://www.ssu.ac.kr/)
>
3. 링크에 설명 추가하는 방법
> `[텍스트](주소 "설명")`

>`[Soongsil University]( http://www.ssu.ac.kr/ "Welcome to Soongsil !")`
> [Soongsil University]( http://www.ssu.ac.kr/ "Welcome to Soongsil !")
>
4. 참조 스타일 링크

- 같은 링크 URL을 여러 번 입력해야하거나 글 안의 링크를 따로 관리하고 싶을 때 사용
- 참조 스타일 링크는 **두 부분**으로 구성
    - 첫 번째 부분 , **텍스트로 유지**하는 부분
        > `[텍스트][1]`
        - **두 세트의 대괄호**로 구성
        - 첫번째 대괄호 세트는 **링크가 삽입된 것으로 표시되어야 하는 텍스트** ( ex) [텍스트] )
        - 두번째 대괄호 세트는 문서의 **다른 곳에 저장한 링크**를 가리키는 데 사용되는 **레이블**을 표시 (  ex) [1] )
        >
            ※ 주의
            첫 번째와 두 번째 대괄호 세트 사이에 공백을 포함 할 수 있음
            두 번째 대괄호 세트의 레이블은 대소 문자를 구분하지 않음
            문자, 숫자, 공백 또는 구두점 포함 가능

    - 두 번째 부분, 파일의 **다른 곳에 저장**하는 부분
        > `[1]: Welcome to Soongsil!`
        - **괄호로 묶인 라벨**과 **콜론**과 **하나 이상의 공백**이 옴 (ex) [1] : )
        - 링크의 URL을 선택적으로 괄호로 묶을 수 있음
        - 뒤에 " " 나 ' '로 선택적으로 설명을 덧붙일 수 있음
>
5. 이미지에 링크 삽입
> `[![이미지설명(이미지 소스 URL)]](링크URL)`
>
    ※ 주의
     Markdown은 URL 중간에있는 공백을 처리하지 않음.
     -> 호환성을 위해 공백을 % 20으로 URL 인코딩

     ex) [link](https://www.example.com/my%20great%20page)


Github : https://github.com/seyxxn/GFMpractice
