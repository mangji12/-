# VoiceCloning

생성일: 2021년 10월 1일

### 개요

목소리를 인공지능 기술을 이용하여 복제하는 것을 목표로 한다. 인공지능 모델은 직접 작성한 것이 아닌 깃허브에 공유된 [한국형 음성모방 소스코드](https://github.com/metamin99/tacotron2_wavenet_korean_tts.git)을 사용하였다.

### 참조 문서

[https://github.com/metamin99/tacotron2_wavenet_korean_tts](https://github.com/metamin99/tacotron2_wavenet_korean_tts)

[딥러닝 음성합성 multi-speaker-tacotron(tacotron+deepvoice)설치 및 사용법](http://nblog.syszone.co.kr/archives/9416)

[[코드리뷰]타코트론2 TTS 시스템 2/2 - 새내기 코드 여행](https://joungheekim.github.io/2021/04/02/code-review/)

### 구성 환경

- python = 3.6
- cuda = 8.0
- cudnn = 6.0
- tensorflow / tensorflow - gpu = 1.3.0

### 사용 기술

- Docker
- Tensorflow
- Python

### 프로젝트 과정

1. 학습데이터와 그래픽카드에 실행시킬 파이썬 코드 준비.
2. 도커 이미지를 활용하여 가상의 리눅스 서버 구축.
3. 구성 환경에 맞춰 패키지 설치 (매우 중요)
4. 학습
5. 학습 후 원하는 단어를 말해 줄 모음과 자음으로 나뉘어진 텍스트 파일(.txt) 탑재

### 프로젝트 소개

'VoiceCloning'은 TTS(Text-to-Speech) 기술과 음성 합성 기술을 결합하여 사용자가 원하는 목소리를 생성할 수 있도록 하는 프로젝트이다. 이 프로젝트는 기존의 목소리 생성 기술에서 한계점을 극복하고, 더욱 자연스러운 목소리를 만들어내는 것을 목표로 한다.

### 프로젝트 목표

- 사용자가 원하는 말을 모방할 수 있도록 한다.
- 생성된 목소리가 자연스럽고 현실적이어야 한다.
- 생성된 목소리가 원본 목소리와 최대한 유사해야 한다.

### 프로젝트 결과

- 충분한 모방 모델 생성에 필요한 학습 부족. 생성된 파라미터의 품질과 결과는 학습 량에 비례함. 결과적으로 목표하는 결과와 음성 모방 품질의 격차가 큼.
    
    → 학습에 필요한 그래픽 카드 필요, 학습을 실행시킬 환경 매우 중요.
    
- 학습시킨 모델의 그래프
    
    ![충분하지 않은 학습으로 인한 정제되지 않은 결과](https://github.com/mangji12/FreshMan-s-Individual-1st-time-of-my-department-project/blob/main/%EA%B2%B0%EA%B3%BC%EB%AC%BC%20%ED%8F%B4%EB%8D%94/%EC%A0%81%EA%B2%8C%20%ED%95%99%EC%8A%B5%ED%95%9C%20%EA%B2%B0%EA%B3%BC.png?raw=true)
    
    충분하지 않은 학습으로 인한 정제되지 않은 결과
    
    ![충분한 학습으로 인한 정제된 결과](https://github.com/mangji12/FreshMan-s-Individual-1st-time-of-my-department-project/blob/main/%EA%B2%B0%EA%B3%BC%EB%AC%BC%20%ED%8F%B4%EB%8D%94/%EB%A7%8E%EC%9D%B4%20%ED%95%99%EC%8A%B5%ED%95%9C%20%EA%B2%B0%EA%B3%BC.png?raw=true)
    
    충분한 학습으로 인한 정제된 결과
    
- 모방 결과 .wav 파일
    
    [음성 결과물](https://github.com/mangji12/FreshMan-s-Individual-1st-time-of-my-department-project/raw/main/%EA%B2%B0%EA%B3%BC%EB%AC%BC%20%ED%8F%B4%EB%8D%94/%EC%9D%8C%EC%84%B1%20%EA%B2%B0%EA%B3%BC%EB%AC%BC.wav)
    
- 트레이닝 로그
    
    ![Untitled](https://github.com/mangji12/FreshMan-s-Individual-1st-time-of-my-department-project/blob/main/%EA%B2%B0%EA%B3%BC%EB%AC%BC%20%ED%8F%B4%EB%8D%94/%E1%84%90%E1%85%B3%E1%84%85%E1%85%A6%E1%84%8B%E1%85%B5%E1%84%82%E1%85%B5%E1%86%BC%20%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3.png?raw=true)
    

### 결론

본 프로젝트에서는 TTS(Text-to-Speech) 기술과 음성 합성 기술을 결합하여 사용자가 원하는 목소리를 생성하는 것을 목표로 했다. 

학습 데이터와 그래픽 카드에 합성 시킬 파이썬 코드를 준비하고, 도커 이미지를 활용하여 가상의 리눅스 서버를 구축하였다. 그리고 구성 환경에 맞춰 패키지를 설치한 후 학습을 진행하였다.

하지만 충분한 모방 모델을 생성하려면 그래픽 카드가 필요하며, 학습을 실행시킬 환경이 매우 중요하다는 것을 알게 되었다. 이로 인해 목표하는 결과와 음성 모방의 질이 큰 차이가 나타났다. 

따라서, 모델 학습에 필요한 그래픽 카드와 환경을 더욱 신경써서 구성해야 한다.

본 프로젝트의 향상된 결과가 도출되려면 목소리 생성 기술에서 한계점을 극복하고, 더욱 자연스러운 목소리를 만들어내는 것을 목표로 해야할 것이다.
