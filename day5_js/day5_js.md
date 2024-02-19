## 복습





## 입력 요소에 대한 선택자 연습
가상요소 선택자 : `::marker, ::before, ::after`
체크박스중에 checked(상태) - 상태요소 선택은 기호:
기호: 바로뒤의 인접형제 1개선택

```css
input [type=checkbox]:checked+label{
            color: blue;
        }
```