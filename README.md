# 소주 가격 상승에 대한 원인 분석 🍾

## 프로젝트 개발 기간
2024.03.14 ~ 2024.05.16

## 프로젝트 설계
주제: 물가 상승에 따른 현대 사회에서 개인이 받는 피해를 데이터 분석을 통해 해결하는 방법

### 소 주제 선정
소주의 가격이 시간에 따라 물가지수 대비 급격한 상승을 보여 개인이 부담을 느끼기 때문에 소주를 소 주제로 선정

## 소주 물가 상승 요인 분석
소주 물가 상승에 영향을 줄 만한 요인을 분석

1. 소주 소비량
2. 알루미늄 가격(소주 병뚜껑의 원자재)
3. 타피오카 가격(소주 주 재료)
4. 유리용기 가격(소주병의 주 원자재)
5. 정제당 가격(소주 주 재료)

이외에도 여러 요인을 생각했지만 데이터를 찾지 못함.

## 데이터 수집 및 전처리
소비자 물가 사이트에서 2012년 ~ 2024년까지의 세 종류의 소주에 대한 가격 데이터를 수집했습니다. 이외에도 여러 물가 사이트와 한국 통계 사이트를 통해 위 5가지 영향을 줄 만한 요인에 대한 데이터를 수집 후 전처리 과정을 거쳤습니다.

## 선형 회귀
소주 가격을 종속변수로 설정하고 영향을 줄 만한 요인들을 각각 독립변수로 설정하여 선형회귀를 진행했습니다. 이후 각각의 요인들이 소주 가격 상승과 연관성이 있는지 파악하기 위해 R^2, p-value를 통해 적합성을 판단했습니다.

1. 소주 가격 & 소주 수요량

![소주 가격 & 소주 수요량](https://github.com/jungoat/soju_price/blob/master/readme_images/Untitled.png)

2. 소주 가격 & 알루미늄 가격

![소주 가격 & 알루미늄 가격](https://github.com/jungoat/soju_price/blob/master/readme_images/Untitled%201.png)

3. 소주 가격 & 타피오카 가격

![소주 가격 & 타피오카 가격](https://github.com/jungoat/soju_price/blob/master/readme_images/Untitled%202.png)

4. 소주 가격 & 유리용기 가격

![소주 가격 & 유리용기 가격](https://github.com/jungoat/soju_price/blob/master/readme_images/Untitled%203.png)

5. 소주 가격 & 정제당 가격

![소주 가격 & 정제당 가격](https://github.com/jungoat/soju_price/blob/master/readme_images/Untitled%204.png)

5가지 요인에 대해 선형회귀 모델에서 연관성이 있는 변수는 소주 수요량과 유리 용기의 가격이었습니다. 모델을 돌리기 전에 예상으로는 주 원재료인 타피오카가 당연히 관련성이 높을 거라 생각했는데 그렇지 않은 결과가 나왔습니다.

## 해결 방안

1. **유리 용기 ⇒ PET 재질로 변경**
   - 유리보다 페트병이 원자재 가격이 2배 이상 저렴하므로 페트병을 사용하면 출고가를 낮출 수 있을 것이라 판단.
   - 제조 비용, 운송 비용 측면에서도 유리보다 PET가 훨씬 편리하기 때문에 비용을 절약할 수 있음.

2. **주류세 조정**
   - 소주 출고가에 대해 선제적으로 주류세 인하를 해야 소비자를 보호할 수 있습니다.

### 개정 전 후 차이
![개정 전 후 차이](https://github.com/jungoat/soju_price/blob/master/readme_images/Untitled%205.png)

### 개정 후 효과
![개정 후 효과](https://github.com/jungoat/soju_price/blob/master/readme_images/Untitled%206.png)

## 배운 점

1. **데이터 수집의 어려움**: 주제를 선정할 때 데이터 수집이 가장 어려운 부분이었습니다. 첫 프로젝트다 보니 데이터 수집에 대한 생각이 미숙해 주제를 선정할 때 데이터의 유무와 필요한 데이터의 양을 고려하는 것이 중요하다는 것을 배웠습니다.
2. **문제 해결 능력**: 일상적인 생활에서 데이터 분석을 통해 문제를 파악 후 해결하는 방법을 배웠습니다. 데이터를 분석하여 문제의 원인을 파악하고 해결책을 제시하는 과정을 경험했습니다.
