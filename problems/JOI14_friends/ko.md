지학이는 역사의 뒤안길에서 활약하는 요원이며, 세계 평화를 위해 나날이 활동을 계속하고 있습니다. 지구에는 $N$개의 국가가 있으며 각 국가에는 $1$ 이상 $N$ 이하의 자연수 번호가 매겨져 있다. 지학이의 목적은 이러한 $N$개의 국가들 사이에 우호 관계를 쌓아서 세계 평화를 유지하는 것입니다. 지학이는 활동 계획을 세우기 위해 현재의 국제 관계를 나타낸 그림을 그렸습니다.

지학이는 큰 도화지를 한 장 준비하여, 그 위에 각 국가를 나타내는 $N$개의 점을 그렸습니다. 다음에, 현재의 국제 관계를 나타내기 위해 서로 다른 두 국가를 연결하는 화살표 $M$개를 그렸습니다. $a$번 국가를 나타내는 점에서 $b$번 국가를 나타내는 점으로 향하는 화살표는 "현재 $a$번 국가에서 $b$번 국가에 대사를 파견하고 있다"는 것을 나타냅니다. 앞으로  $a$번 국가를 나타내는 점에서 $b$번 국가를 나타내는 점으로 향하는 화살표를 **화살표 $(a,b)$**로 표기하기로 합니다. 이렇게 그린 $N$개의 점들과 $M$개의 화살표들이 현재 국제 관계를 나타낸 그림입니다.

국가 간 우호 관계의 계기로서 두 나라 간의 우호 조약 체결 회의(편의상 앞으로 '회의'라고 합니다)를 실시한다고 생각해 봅시다. $p$번 국가와 $q$번 국가가 회의를 하기 위해서는 두 나라 모두에 대사를 파견하고 있는 같은 국가인 $x$가 중재국으로 필요합니다. 또한 회의를 실시한 후 두 나라는 서로 상대 국가에 대사를 파견합니다. 즉 $p$번 국가와 $q$번 국가가 회의를 위해 화살표 $(x,p)$와 화살표 $(x,q)$가 존재하는 국가 $x$가 존재해야 하며, 회의를 수행한 후에는 화살표 $(p,q)$와 화살표 $(q,p)$가 지도에 새로 그려집니다. 그러나 화살표가 이미 그려져 있는 경우 새롭게 그려 추가하지는 않습니다.

지학이의 임무는 회의 가능한 두 국가와 그 회의의 중재국을 선정하고 회의를 진행하는 것입니다. 그림을 사용해 이 시뮬레이션을 할 때, 세계가 얼마나 평화로운지는 도화지 위에 그려진 화살표의 개수를 기준으로 생각하기로 합니다. 즉 두 개의 국가를 골라 우호 조약 체결을 반복하고, 도화지 위에 그려진 화살표의 개수를 최대 몇 개까지 만들 수 있는지를 알고자 합니다.

### 해야 할 일

이 세상에 있는 국가의 개수와 현재의 국제 관계에 대한 정보가 주어질 때, 두 개의 국가를 선택하여 회의를 진행하는 것을 반복하여 도화지 위에 그려진 화살표의 개수를 최대 몇 개까지 만들 수 있는지 구하는 프로그램을 작성하세요.

### 입력

표준 입력에서 다음 입력을 받습니다.

* 첫 번째 줄에 두 개의 정수 $N$과 $M$이 공백을 사이로 두고 주어집니다. $N$은 도화지 위에 찍혀 있는 점의 개수 (이 세상에 있는 국가의 수)이고, $M$은 도화지 위에 그려진 화살표의 개수입니다.
* 다음 $M$개 줄에 도화지에 그려진 화살표들의 정보가 주어집니다. 이 중 $i$번째 줄 ($1 \le i \le M$)에는 두 개의 정수 $A_{i}$와 $B_{i}$가 공백을 사이로 두고 주어집니다. 이는 도화지에 $A_{i}$번 국가를 나타내는 점에서 $B_{i}$번 국가를 나타내느 점으로 향하는 화살표가 그려져 있다는 것, 즉 $A_{i}$번 국가에서 $B_{i}$번 국가에 대사를 파견하고 있다는 것을 나타냅니다.

### 출력 형식

표준 출력으로 그릴 수 있는 화살표의 개수의 최댓값을 한 줄에 출력합니다. 화살표의 개수는 회의를 통해 새로 그려진 것뿐만 아니라 이미 (입력에서) 그려져 있는 것도 세어야 합니다.

### 제약 조건

입력 데이터의 제약 조건은 아래와 같습니다.

* $1 \le N \le 100,000$
* $0 \le M \le 200,000$
* $1 \le A_{i} \le N$ ($1 \le i \le M$)
* $1 \le B_{i} \le N$ ($1 \le i \le M$)
* $A_{i} \neq B_{i}$ ($1 \le i \le M$)
* $(A_{i}, B_{i}) \neq (A_{j}, B_{j})$ ($1 \le i < j \le M$)

### 서브태스크

#### 서브태스크 1 [5점]

* $N \le 100$

#### 서브태스크 2 [30점]

* $N \le 5,000$

#### 서브태스크 3 [65점]

추가적인 제약 조건이 없습니다.

### 입력 예제


<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>입력 1</th>
   <th>출력 1</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">5 4<br/>
1 2<br/>
1 3<br/>
4 3<br/>
4 5</td>
   <td class="code-font">10</td>
  </tr>
 </tbody>
</table>

예를 들어 아래와 같은 순서로 총 10개의 화살표를 만들 수 있습니다.

* 1번 국가가 중재국이 되어 2번 국가와 3번 국가가 회의를 실시합니다.
* 4번 국가가 중재국이 되어 3번 국가와 5번 국가가 회의를 실시합니다.
* 3번 국가가 중재국이 되어 2번 국가와 5번 국가가 회의를 실시합니다.