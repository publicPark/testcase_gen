# JSON 제너레이터
링크를 클릭
<https://publicPark.github.io/json-generator/>

테스트 데이터가 필요해서 만든 JSON generator  
그룹이 여러개 있을 수 있고, 각 그룹에는 여러개의 옵션이 있을 수 있습니다.  

### 그룹 리스트 폼

'그룹 추가' 버튼을 누르면 title(String), options(Array)로 이루어진 오브젝트를 추가할 수 있습니다. 그룹 최대 N개 추가했다고 하자.
그리고 옵션 추가 버튼을 눌러 각 그룹에 옵션을 최대 M개 추가.

### 리스트 생성

그룹, 옵션을 입력한 것을 바탕으로 각 그룹의 옵션을 조합한 모든 경우의 수 리스트를 생성합니다. 이건 재귀로 구현.
각 옵션 수를 모두 곱한 수가 리스트의 length가 되겠지.
옵션이 최대 M개, 그룹은 최대 N개니 length는 최대 M의 N제곱이 되겠다.

### 개수 입력

각 조합 항목에 '남은 개수'를 입력할 수 있다.
그 후 테스트에 맞게 데이터를 약간 가공.
데이터의 최종 형태는 이렇게 될 것이다.

```
{
  // titleList: [a, b, c],
  countList: [
    [ combination: [], remainCount: 0 ]
  ],
  groupList: [
    { title: '', options: [] }
  ]
}
```




# 코드 실행 방법   
npm start

# 배포 방법
npm deploy