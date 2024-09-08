git : https://github.com/Entropy1110/Lending_solidity/blob/main/src/UpsideAcademyLending.sol

commit : `304ffd41b89fa28a479f0b49914d462c0a5e8904`

| **ID** | **요약** | **위험도** |
| --- | --- | --- |
| Ent-001 | `initializeLendingProtocol` 함수에서 `usdc` 주소를 원하는 대로 수정할 수 있습니다. | High |

# Description

`initializeLendingProtocol`함수를 누구나 호출할 수 있기 때문에 `usdc` 주소를 원하는 토큰 주소로 조작이 가능하며 이로 인해 다른 기능을 정상적으로 사용할 수 없게 됩니다.

# Impact

### High

잘못된 `usdc` 주소 변경으로 인해 사용자들의 가용성이 침해됩니다.

# Recommendation

- `openzeppelin` 에서 제공하는 Ownable 컨트랙트를 사용하여 컨트랙트 소유자만 호출 할 수 있도록 수정