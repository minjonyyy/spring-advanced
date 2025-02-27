# SPRING ADVANCED

## 필수기능
### LV.1 코드 개선

1. Early Return</br>
 : 해당 이메일이 존재하는지 먼저 확인한 이후에 password 인코딩을 진행하는 순서로 변경하여 불필요한 메서드 동작이 일어나지 않도록 하였다.

2. 불필요한 if-else 피하기</br>
 : if문에서 에러를 잡아낼 수 있는 상황이기 때문에 else문을 작성하지 않고 가독성을 높인다.</br>
 : 불필요한 메모리 낭비를 막기 위해서 if문으로 예외처리 이후에 배열에 저장하도록 수정하였다.

3. Validation 적용하기</br>
: validation 을 활용하여 dto에서 잘못된 입력에 대한 처리를 진행하도록 하였다.


### LV.2 N+1 문제</br>
: `@EntityGraph`을 활용하여 불필요한 쿼리가 실행되지 않도록 수정하였다.</br>
`@EntityGraph(attributePaths = {"user"})`으로 user 객체를 조회하도록 했기 때문에 메서드명을 `findById`로 바꾸어 주었다.
