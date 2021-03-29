# makdown extended syntax (GFM)

## 1. table
  확장된 문법에선 파이프라인(|)을 이용해 테이블을 만들 수 있다.
  
  ex)
  \| sex \| male \| female |<br>
  | :--: | :---: | :---: |<br>
  | height | 174 | 165 |<br>
  | weight | 65 | 58 |
  
  result)
  | sex | male | female |
  | :--: | :---: | :---: |
  | height | 174 | 165 |
  | weight | 65 | 58 |
  
  1. makrdown에서 파이프라인 사용시, 자동으로 줄을 맞춰서 표를 그려준다.<br>
  2. 또한 2번째 줄에서 쓰이는 -- 부분을 구분자라고 하는데, 이 부분에서 콜론(:) 기호를 이용해 좌, 우, 중앙 정렬이 가능하다.<br>
  3. 똑같이 내부에서 2번 이상의 띄어쓰기는 무시된다<br>
  4. 칸 안에 이스케이프 문자를 쓰면 그대로 적용돼서 테이블이 안 만들어진다
  5. 테이블 이후에 다른 블록과 구분하지 않고 markdown 코드를 쓰면 테이블이 무너진다
  6. 첫행과 구분자행 간에 cell 개수는 맞춰줘야한다.
  7. 자료가 써진 행의 열수 > 첫행 열수 : 초과된 자료는 무시된다. 반대의 경우, 빈칸에 공백이 들어간다
  8. 구분자 행 이후 아무것도 써있지 않으면 body가 없는 테이블이 만들어진다.

## 2. tasklist
  확장된 문법에선 업무 리스트를 만들고 체크 여부를 만들 수 있다.
  
  ex)
  하이픈(-) 이후에 대괄호를 쓰고 그 안을 공백 or x로 채운 뒤 업무를 쓰면<br>
  \- [ ] Web bulletin board development<br>
    (tab)\- [ ] jsp study<br>
    (tab)\- [x] socket programming<br>
  \- [x] certification
  
  result)
  - [ ] Web bulletin board development
    - [ ] bar
    - [x] baz
  - [x] certification
  
  또한 들여쓰기를 통해 다중 업무 리스트도 만들 수 있다.
 
 
## 3. strikethrough
  확장된 문법에선 물결표시(~)를 이용해 취소선을 만들 수 있다. 취소할 문장을 두 ~로 감싸라
  
  ex)
  
  \~~Assignment is so terrible~~ Aren't you?
  
  result)
  
  ~~Assignment is so terrible~~ Aren't you?
  
  ps. ~~ 강조 구문 내에서 엔터 두 번으로 단락이 새로 생성되면 취소선이 사라진다
  
## 4. autolinks
  확장된 문법에선 꺽새 없이 자동링크를 달 수 있다.<br>
  단, 이런 링크들은 줄의 시작점, 공백 뒤, 구분자(\*, \_, \~, \)) 뒤에 있어야 한다.
  
  www.commonmark.org
  
  Visit www.commonmark.org/help for more information.
  
  Visit www.commonmark.org.
  
  Visit www.commonmark.org./a.b.
  
  이건 모르겠다.....
  
## 5. Disallowed Raw HTML
  확장된 문법에선 tagfilter가 가능하다...?
  
  <title> <style> <em>
  
  <blockquote>
    <xmp> is disallowed.  <XMP> is also disallowed.
  </blockquote>
