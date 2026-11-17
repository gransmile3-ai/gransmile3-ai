## gransmile3-ai

연합학습을 공부하고 실험하는 학생입니다. 요즘은 데이터가 클라이언트마다 다른 Non-IID 상황에서 FedAvg가 왜 흔들리고 FedProx가 어떻게 잡아주는지 직접 돌려보고 있습니다. 로봇(TurtleBot4, ROS 2)과 음악 생성 모델도 틈틈이 만지고 있습니다.

### federated-learning-experiments

[Flower](https://flower.ai/)와 PyTorch로 FedAvg와 FedProx를 비교한 실험 모음입니다. CIFAR-10을 Dirichlet α=0.3으로 두 클라이언트에 나눠서, Oracle Cloud A1 한 대에서 돌렸습니다.

30라운드, 학습률 0.005에서 μ를 바꿔 본 결과(마지막 5라운드 평균):

| 전략 | 정확도 |
| --- | --- |
| FedAvg | 51.06% |
| FedProx μ=0.01 | 53.95% |
| FedProx μ=0.02 | 54.11% |
| FedProx μ=0.05 | **56.62%** |

FedAvg는 8라운드쯤 정점을 찍고 내려갔고, μ를 키울수록 그 하락이 줄었습니다. 조건마다 시드 1회라 작은 차이는 우연일 수 있고, 0.05보다 큰 μ는 아직 안 해봤습니다. 설정과 한계는 [SWEEP30.md](https://github.com/gransmile3-ai/federated-learning-experiments/blob/main/NonIID/SWEEP30.md)에 적어두었습니다.

[<img src="https://raw.githubusercontent.com/gransmile3-ai/federated-learning-experiments/main/NonIID/report/sweep30_mu.png" width="640" alt="μ별 정확도 곡선">](https://github.com/gransmile3-ai/federated-learning-experiments)

### 쓰는 것

Python, PyTorch, Flower, Linux, Git
