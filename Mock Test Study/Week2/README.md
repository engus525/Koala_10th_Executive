## 2주차 모의테스트 해설
<br>

### A. [최대 상승](https://www.acmicpc.net/problem/25644)
- 풀이
>간단한 DP 문제였습니다. 가격을 입력받은 배열을 순회하며, 구매 가격이 될 최솟값을 갱신합니다.<br>
현재 가격이 최솟값 이상이라면 이득을 계산하고, 이득의 최댓값을 갱신합니다.<br>
- 예시 코드
>http://boj.kr/6cef76fcfc284536afe68a07ccae2df6

****************************

### B. [미로 만들기](https://www.acmicpc.net/problem/1347)
- 풀이
>최대 이동 횟수가 50회 미만이므로, 크기가 100*100이상인 이차원 배열을 생성하고 시작지점을 (50,50)으로 초기화합니다.<br>
입력받은 문자열을 따라 이동하며, 이동한 지점을 표기함과 동시에 행과 열의 최소,최대 지점을 갱신합니다.<br>
이동을 마치고, 범위의 최소 지점에서 최대 지점을 순회하며 표기된 지점에서는 '.', 표기되지 않은 지점에는 '#'을 출력합니다.
- 예시 코드
>http://boj.kr/21e04b7ab1914c6d8077b57846816492


****************************

### C. [미친 로봇](https://www.acmicpc.net/problem/1405)
- 풀이
>B와 구현 방식이 유사한 DFS 문제였습니다.<br>
최대 이동 횟수가 15회 미만이므로, 크기가 30*30이상인 이차원 배열을 생성하고 시작지점을 (15,15)으로 초기화합니다.<br>
DFS를 진행하며 방문한 지점을 재방문하면 탐색을 멈추고, n번의 이동을 성공하면 이동경로가 단순할 확률에 계산된 확률을 더합니다.<br>
이때, 다음 지점으로 이동할때마다 해당 방향으로의 확률을 곱해줍니다.
- 예시 코드
>http://boj.kr/471153b81aa046faaf31d44b2145cfcf

****************************

### D. [제자리 멀리뛰기](https://www.acmicpc.net/problem/6209)
- 풀이
>뛴 거리의 최솟값이 최대가 되어야하므로, 이진 탐색을 통해 밟은 돌섬이 (n-m)이상일 때에 한하여 뛴 거리의 최솟값을 키워나갑니다.<br>
뛴 거리는 1이상 d이하 이므로, left와 right를 각각 1과 d로 초기화한 후 중간값을 계산합니다.<br>
입력받은 각 돌섬의 거리를 정렬한 후, 다음 돌섬이 현재 서있는 곳의 거리에서 중간값을 더한 값보다 작다면 밟지 않습니다.<br>
반대로 더 크다면 밟은 돌섬의 갯수를 늘려줌으로써 최종적으로 (n-m)과 비교하게 됩니다.<br>
이를 left가 right이하인 동안 반복하여 답안을 도출합니다.
- 예시 코드
>http://boj.kr/4a8a80dd3948484392bd29f4e6da8ed7

