## [ Spark의 데이터 처리 단위 : RDD  ]

데이터셋을 추상적으로 다루기 위한 RDD (Resilient Distributed Dataset: 내결함성 분산 데이터셋)이라는 데이터셋이 있으며, RDD가 제공하는 API로 변환과 액션 기능을 구현한다.

**RDD(Resilient Distributed DataSet)) :**

​	Spark 에서 처리되는 데이터는 RDD 객체로 생성하여 처리한다
​	RDD 객체 는 두 가지 방법으로 생성 가능하다
​	(1) Collection 객체를 만들어서
​	(2) HDFS 의 파일을 읽어서

### RDD
객체의 특징 : Read Only(immutable)
						1~n 개의 partition 으로 구성 가능
						병렬적 분산 ) 처리가 가능하다
						RDD 의 연산은 Transformation 연산과 Action 연산으로 나뉜다
						Transformation 은 Lazy execution 을 지원한다
						lineage 를 통해서 fault toleran t 결함 내성 를 확보한다