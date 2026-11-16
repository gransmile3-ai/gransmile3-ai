<div align="center">

<img src="https://raw.githubusercontent.com/gransmile3-ai/gransmile3-ai/main/banner.svg" width="100%" alt="gransmile3-ai"/>

<br/>

<img src="https://skillicons.dev/icons?i=python,pytorch,linux,git,docker&theme=dark"/>

</div>

<br/>

### 🔬 What I'm working on
| | |
|---|---|
| **연합학습** | Flower + PyTorch로 Non-IID 환경 FedAvg / FedProx 비교 |
| **로보틱스** | TurtleBot4 · ROS2 |
| **음악 AI** | MIDI 작곡 모델 |

### 📌 Featured project: [federated-learning-experiments](https://github.com/gransmile3-ai/federated-learning-experiments)
<div align="center">

<a href="https://github.com/gransmile3-ai/federated-learning-experiments"><img src="https://raw.githubusercontent.com/gransmile3-ai/federated-learning-experiments/main/NonIID/report/sweep30_mu.png" width="80%"/></a>

**FedProx μ=0.05 → 30라운드 최종 정확도 55.8% (FedAvg 51.0%, +4.8%p)**

</div>

| 설정 (lr=0.005, 30라운드) | 최종 정확도 |
|---|---|
| FedAvg | 50.98% |
| FedProx μ=0.01 | 53.93% |
| FedProx μ=0.02 | 54.66% |
| **FedProx μ=0.05** | **55.76%** |

> Flower + PyTorch · Non-IID(Dirichlet α=0.3) · 시드 1회 실행 결과
