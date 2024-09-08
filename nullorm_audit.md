git : https://github.com/Null0RM/Lending_solidity/blob/main/src/UpsideLending.sol

commit : `ef1a322f73e57207c0a8b8f42a6e74ba3a14d4f6`

| **ID** | **요약** | **위험도** |
| --- | --- | --- |
| NULL-001 | `repay` 함수 호출 시 빌린 토큰과 관계없이 상환이 바로 가능 | High |

# Description

`repay` 함수 호출 시 `_token`의 수량의 대한 조건만 확인하기 때문에 빌린 토큰의 종류와 상관없이 빌린 금액에 대한 상환이 가능합니다.

# Impact

### High

`_token`의 주소가 `usdc` 주소가 아니여도 상환이 가능합니다.

# Recommendation

- `_token`  주소가 `usdc` 와 동일한지 확인하는 조건 추가