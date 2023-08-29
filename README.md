# 탈모 진단
탈모 진단 및 제품 추천 시스템 개발

## 📃목차
* 📋[프로젝트 개요](#프로젝트-개요)
* 🙋[팀구성 및 역할](#팀구성-및-역할)
* 📁[데이터 개요](#데이터-개요)
* 🔍[개발과정](#개발과정)
* 💡[기대효과](#기대효과)
  
## 📋프로젝트 개요
* 탈모 환자수 증가 및 탈모 제품 매출 증가 (2020년 대비 2021년 76% 증가 출처:올리브영)


### 프로젝트 목표
* 두피이미지를 통한 탈모 진단 및 제품 추천 시스템 개발하여 관련 제품 매출 증진 및 고객 유치 가능하게 함 (매장 셀프 탈모 진단 기계 설치)


### 탈모 진단 및 제품 추천 process

![image](https://github.com/justdoit93/hair_loss/assets/129941418/c82fc56f-2548-4cc9-8238-34a3528b5086)
![image](https://github.com/justdoit93/hair_loss/assets/129941418/f3a9c7b9-d773-42fb-a2e4-7c83009d0e78)

* 기계의 두피 전용 카메라를 통해 촬영하면 탈모 진단 및 제품 추천
* 기계의 화면과 영수증에 진단 결과 출력

### 결과

모델결과
  
![image](https://github.com/justdoit93/hair_loss/assets/129941418/8dd5eaae-1e55-4d4d-a942-3936418179e4)

* LeNet, ResNet, DenseNet 모두 accuracy 70% 대로 큰 차이를 보이지는 않음
* DenseNet이 약 77%로 가장 높은 정확도
* DenseNet epoch 30번 중 21번째 가장 좋은 성능
* train loss는 21번째 이후 줄어들지만 test loss는 줄어들지 않음 (과적합)

분석결과

![image](https://github.com/justdoit93/hair_loss/assets/129941418/86071a58-5bac-4606-840c-08b303fca7b5)

* test 데이터 5,288개로 예측한 결과 실제 결과 비교
* 탈모 진행 정도 0, 3단계는 비교적 높은 정확도로 진단
* 탈모 진행 정도 2단계 정확도가 제일 낮음

![image](https://github.com/justdoit93/hair_loss/assets/129941418/78d53fa4-37f7-443f-8d6e-70c603462cca)

* 잘못 진단한 이미지 중 랜덤으로 추출 하여 확인
* 실제 3단계 증상 이미지 2개 육안으로도 차이가 큼
* 실제 2단계 증상, 1단계 증상 이미지는 육안으로도 차이 구분 힘듬
* 진단 모델로 높은 정확도의 결과를 내기에는 한계가 있음


## 🙋팀구성 및 역할

* 이성수
  * 두피이미지 및 라벨 데이터 EDA 진행 및 시각화
  * CNN기반 모델 비교, 선정
  * 모델 예측결과 분석 및 개선
* 유효민
  * CNN기반 모델 비교, 선정 및 개발
  * 모델 예측결과 분석 및 개선
  * 프로젝트 일정 및 미팅 관리
* 장호정
  * 추천 제품 데이터 수집 및 EDA 진행
  * 탈모 진단 결과 출력방법 고안
  * 발표자료 제작 및 발표
    
## 📁데이터 개요

* 출처 : AI허브

![image](https://github.com/justdoit93/hair_loss/assets/129941418/b6313627-47bc-419a-bf1f-35e1600e869d)

* Train 이미지 : 18,513개, Test 이미지 : 5,288개
* 탈모 증상 진행 정도(0~3 단계) 라벨 데이터

## 🔍개발과정

* 두피이미지 및 라벨 데이터 EDA 진행 및 시각화
![image](https://github.com/justdoit93/hair_loss/assets/129941418/5799fbfd-b733-434e-a76c-017e53fc9523)

* CNN기반 모델 비교, 선정
![image](https://github.com/justdoit93/hair_loss/assets/129941418/66c9794d-8dbb-4901-9de5-3286f8c1581c)

* 모델 예측결과 분석 및 개선
![image](https://github.com/justdoit93/hair_loss/assets/129941418/97f7171e-414d-48c3-ad95-bdb7b482d21a)
![image](https://github.com/justdoit93/hair_loss/assets/129941418/eb51dffe-0626-45b0-96ca-69b7459bee0e)

## 💡기대효과
