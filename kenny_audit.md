git : https://github.com/55hnnn/Lending_solidity/blob/main/src/DreamAcademyLending.sol

commit : `e24fbed56616a4a316f437292a0cf2911260dfc1`

| **ID** | **요약** | **위험도** |
| --- | --- | --- |
| KENNY-001 | `repay` 함수 호출 시 빌린 토큰과 관계없이 상환이 바로 가능 | High |

# Description

`repay` 함수 호출 시 `token`의 수량의 대한 조건만 확인하기 때문에 빌린 토큰의 종류와 상관없이 빌린 금액에 대한 상환이 가능합니다.

# Impact

### High

`token`의 주소가 `usdc` 주소가 아니여도 상환이 가능합니다.

# Recommendation

- `token`  주소가 `usdc` 와 동일한지 확인하는 조건 추가