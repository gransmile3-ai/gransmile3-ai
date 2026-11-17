<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/gransmile3-ai/gransmile3-ai/main/assets/header-dark.svg">
  <img src="https://raw.githubusercontent.com/gransmile3-ai/gransmile3-ai/main/assets/header-light.svg" width="100%" alt="gransmile3-ai">
</picture>

<br>

연합학습을 공부하고 실험하는 학생입니다. 요즘은 클라이언트마다 데이터 분포가 다른 Non-IID 상황에서 FedAvg가 왜 흔들리고 FedProx가 어떻게 잡아주는지 직접 돌려보고 있습니다.

|  연합학습 | 로보틱스 | 음악 AI |
| --- | --- | --- |
| Flower, PyTorch<br>FedAvg · FedProx 비교 실험 | TurtleBot4, ROS 2<br>실제 로봇으로 만들어 보는 중 | MIDI 기반<br>곡 생성 모델 실험 |

### [federated-learning-experiments](https://github.com/gransmile3-ai/federated-learning-experiments)

CIFAR-10을 Dirichlet α=0.3으로 두 클라이언트에 나눠 FedAvg와 FedProx를 30라운드씩 비교했습니다. FedAvg는 8라운드쯤 정점을 찍고 내려갔고, μ를 키울수록 그 하락이 줄었습니다.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/gransmile3-ai/gransmile3-ai/main/assets/chart-dark.svg">
  <img src="https://raw.githubusercontent.com/gransmile3-ai/gransmile3-ai/main/assets/chart-light.svg" width="100%" alt="μ별 최종 정확도: FedAvg 51.06%, FedProx μ=0.05 56.62%">
</picture>

조건마다 시드 1회 실행이라 작은 차이는 우연일 수 있고, 0.05보다 큰 μ는 아직 시험하지 않았습니다. 설정과 한계는 [SWEEP30.md](https://github.com/gransmile3-ai/federated-learning-experiments/blob/main/NonIID/SWEEP30.md)에 적어두었습니다.

### Tech

`Python` `PyTorch` `Flower` `ROS 2` `Linux` `Git`
