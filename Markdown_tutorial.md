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

