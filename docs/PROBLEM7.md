## 기능 정의

1. 친구 명단 만들기 기능
2. 친구가 아닌 사람의 명단 만들기 기능
3. (2) 중에서 친구와 겹치는지인의 명단을 만드는 기능
   - 친구명단에 있는 친구의 친구이며, 본인 또는 본인의 친구가 아닌 친구면 추가
4. 점수를 계산하는 기능

   - 친구의 친구이면 10점 추가
   - 방문한 사람이면 1점 추가

5. 정렬하는 기능

   - 점수가 가장 높은 순으로 정렬
   - 점수가 같으면, 이름 순으로 정렬

6. 예외처리
   - 점수가 0점이면 추천하지 않음
   - 최대 5명만 추천하도록 제한함.

## 🚀 기능 요구 사항

레벨 2의 팀 프로젝트 미션으로 SNS(Social Networking Service)를 만들고자 하는 팀이 있다. 팀에 속한 크루 중 평소 알고리즘에 관심이 많은 미스터코는 친구 추천 알고리즘을 구현하고자 아래와 같은 규칙을 세웠다.

- 사용자와 함께 아는 친구의 수 = 10점
- 사용자의 타임 라인에 방문한 횟수 = 1점

사용자 아이디 user와 친구 관계를 담은 이차원 배열 friends, 사용자 타임 라인 방문 기록 visitors가 매개변수로 주어질 때, 미스터코의 친구 추천 규칙에 따라 점수가 가장 높은 순으로 정렬하여 최대 5명을 return 하도록 solution 메서드를 완성하라. 이때 추천 점수가 0점인 경우 추천하지 않으며, 추천 점수가 같은 경우는 이름순으로 정렬한다.

### 제한사항

- user는 길이가 1 이상 30 이하인 문자열이다.
- friends는 길이가 1 이상 10,000 이하인 배열이다.
- friends의 각 원소는 길이가 2인 배열로 [아이디 A, 아이디 B] 순으로 들어있다.
  - A와 B는 친구라는 의미이다.
  - 아이디는 길이가 1 이상 30 이하인 문자열이다.
- visitors는 길이가 0 이상 10,000 이하인 배열이다.
- 사용자 아이디는 알파벳 소문자로만 이루어져 있다.
- 동일한 친구 관계가 중복해서 주어지지 않는다.
- 추천할 친구가 없는 경우는 주어지지 않는다.

### 실행 결과 예시

| user   | friends                                                                                                                         | visitors                                      | result                    |
| ------ | ------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------- | ------------------------- |
| "mrko" | [ ["donut", "andole"], ["donut", "jun"], ["donut", "mrko"], ["shakevan", "andole"], ["shakevan", "jun"], ["shakevan", "mrko"] ] | ["bedi", "bedi", "donut", "bedi", "shakevan"] | ["andole", "jun", "bedi"] |
