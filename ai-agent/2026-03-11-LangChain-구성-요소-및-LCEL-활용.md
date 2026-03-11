### Context
오늘은 LangChain의 주요 구성 요소인 Prompt Templates, ChatModels, 그리고 Chains를 학습하며, 특히 LangChain Expression Language(LCEL)를 활용한 텍스트 요약 체인을 복습하는 시간을 가졌습니다. 이러한 구성 요소들은 단순히 텍스트를 던지는 방식이 아니라, 구조화된 프롬프트와 모델을 결합하여 일관된 응답을 이끌어내는 데 중요한 역할을 합니다.

### Core
- **Prompt Templates & ChatModels**: 구조화된 프롬프트 생성과 이를 이용한 모델 결합을 통해 더 높은 응답의 일관성을 확보.

- **LCEL 흐름**: `|` (Pipe) 연산자를 이용해 데이터를 흐르는 파이프라인으로 설계하여 복잡한 로직을 선언적으로 단순화. 이는 마치 n8n의 코드 버전 같은 역할을 합니다.

- **LangChain V0.3 vs V1.0+**:
  * **레거시 체인(Legacy Chains)**: 클래스를 중심으로 했던 과거 방식에서 LCEL을 이용한 선언적 설계로 변화.
  * **가독성**: 복잡한 상속 구조에서 벗어나 파이프를 이용한 직관적인 설계.
  * **안정성**: 업데이트로 인한 Breaking Change 위험을 줄이고, 핵심 패키지를 분리하여 인터페이스의 안정성을 강화.
  * **스트리밍**: First-class 지원으로 스트리밍 구현을 손쉽게 최적화.

### Insight
LangChain V0.3와 V1.0+의 가장 큰 차이점은 시스템의 유연성과 안정성입니다. V1.0 이후로 레거시 체인들이 폐기 예정이며, LCEL 방식은 이제 선택이 아닌 필수로 자리 잡았습니다. V0.3 시절은 주로 제공되는 클래스를 '라이브러리'로 사용하는 반면, V1.0+부터는 LCEL을 통해 '프레임워크'처럼 자신의 커스텀 체인을 조립하는 것이 주를 이룹니다.

**출처:** [LangChain Official Documentation](https://docs.langchain.com/v1.0/), [LangChain v1.0 Features](https://github.com/langchain/langchain/releases/tag/v1.0)