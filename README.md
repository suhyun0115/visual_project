# ✒️서울 지역구별 범죄건수와 경찰서 또는 CCTV의 상관관계 분석
## 👥 Team
- Team name : HEE
- Team members : 함은규, 이수현, 이지우
- * :clock1:시작일 : 2024.02.26(월)
  * ⏰목표일 : 2023.12.11(월)
## :books: skill
- **Programming** <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=Python&logoColor=white"> <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=Python&logoColor=white"><img src="https://img.shields.io/badge/Matplotlib-3776AB?style=for-the-badge&logo=Matplotlib&logoColor=white"><img src="https://img.shields.io/badge/Seaborn-3776AB?style=for-the-badge&logo=Seaborn&logoColor=white"><img src="https://img.shields.io/badge/Folium-3776AB?style=for-the-badge&logo=Folium&logoColor=white">
- **Tools** <img src="https://img.shields.io/badge/jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white"> <img src="https://img.shields.io/badge/googlecolab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white">
- **Git** <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=jupyter&logoColor=white"> <img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white">

## 목차(INDEX)
&emsp;&ensp;Ⅰ. 주제 선정</br>&emsp;&ensp;Ⅱ. Data preprocessing</br>&emsp;&ensp;Ⅲ. 시각화</br>&emsp;&ensp;Ⅳ. 결론</br>&emsp;&ensp;

## Ⅰ. 주제선정
  **1. 서울지도에 구별 범죄율과 경찰서 위치, CCTV비율을 표기**</br>
       &nbsp;&nbsp;&nbsp; 1) 관련된 다양한 질문과 상황을 제공함으로써 정확하고 신속한 응답을 제공하는게 목표</br>
       &nbsp;&nbsp;&nbsp; 2) 고객의 문의에 신속, 정확하게 답변할 수 있는 시스템 구축</br>
       
  **2. 자료출처**</br>
       &nbsp;&nbsp;&nbsp; Dacon https://dacon.io/competitions/official/236216/overview/description/

## Ⅱ. 배경 
  **1. 서울지도에 구별 범죄율과 경찰서 위치, CCTV비율을 표기**</br>
       &nbsp;&nbsp;&nbsp; 1) 강남구가 가장 범죄건수가 많음</br>
       &nbsp;&nbsp;&nbsp; 2) 범죄율과 경찰서(파출소), CCTV의 상관관계가 보이지 않음</br>
       &nbsp;&nbsp;&nbsp; 3) CCTV 밀집구역 몇 곳 보임</br>
       &nbsp;&nbsp;&nbsp; 4) 경찰서(파출소)는 구도심(사대문 근처)에 포진됨</br>
       
  **2. 자료출처**</br>
       &nbsp;&nbsp;&nbsp; Dacon https://dacon.io/competitions/official/236216/overview/description/


## Ⅱ. 분석
**1. 데이터 기본분석(1)**</br>
       &nbsp;&nbsp;&nbsp; 1) 범죄건수가 많은 지역 : 강남구 > 송파구 > 관악구</br>
       &nbsp;&nbsp;&nbsp; 2) 지역구별 특징 : 강남구 > 마포구 > 서초구 (범죄 유형 : 강간, 강제추행)</br>
       

**2. 데이터 기본분석(2)**</br>
       &nbsp;&nbsp;&nbsp; 1) 지역구별 건수 비교 : 범죄건수 vs 경찰서 갯수 vs CCTV 갯수</br>
       &nbsp;&nbsp;&nbsp; 2) 지역구별 비율 비교 : 범죄비율 vs 경철서비율 vs CCTV비율</br>
       

**3. 데이터 기본분석(3)**</br>
       &nbsp;&nbsp;&nbsp; 1) DataFrame 변경 (id, category 삭제)</br>
       &nbsp;&nbsp;&nbsp; 2) Dataset 증강 (기존 카테고리를 제외하고 다른 카테고리 질문을 추가)</br>
       &nbsp;&nbsp;&nbsp; 3) Tokenizer</br>       

**4. 데이터 기본분석(4)**</br>
       &nbsp;&nbsp;&nbsp; 1) DataFrame 변경 (id, category 삭제)</br>
       &nbsp;&nbsp;&nbsp; 2) Dataset 증강 (기존 카테고리를 제외하고 다른 카테고리 질문을 추가)</br>
       &nbsp;&nbsp;&nbsp; 3) Tokenizer</br>       

**5. 중간 결론 : CCTV가 증가하면 범죄율을 줄이는 효과가 있을 수 있다.**</br>
       &nbsp;&nbsp;&nbsp; 1) . 상관계수(0.65)로 보면 범죄율에 따라 CCTV비율이 증가하는 것으로 판단할 수 있으나 비중이 한쪽으로 집중되어 있는 것이 보이며, CI가 확장되어 상호관계가 명확하지 않음</br>
       &nbsp;&nbsp;&nbsp; 2) CCTV증가에 따른 CCTV당 범죄를 확인해 보면 CCTV가 증가함에 따라 범죄율이 줄어는 것을 볼수있다</br>
       &nbsp;&nbsp;&nbsp; 3)  그러나 그 한계점이 있을 것으로 사료된다</br>
  

**6. 다른 원인 분석 : 범죄건수 vs 범죄 유형별 vs 인구수, 사업체수, 재산세, CCTV**</br>
       &nbsp;&nbsp;&nbsp; 1)  범죄건수는 폭력과 절도와 강한 상호관계(큰 비증)가 있음(폭력범죄는 절도와 강간·강제추행과 서로 관계성이 있음) </br>
       &nbsp;&nbsp;&nbsp; 2) 범죄건수와 지역구의 인구수와 사업체수에 상호 관계를 갖으나 지역구의 인구수와 사업체수는 서로 독립 변수임다</br>

**7. 이상값(강남구) 제외 **</br>
       &nbsp;&nbsp;&nbsp; 강남구를 제외하면 CI 구간이 축소되는 것을 확인할 수 있다</br>

     

## Ⅲ. 최종결론
 &nbsp;&nbsp;&nbsp; 범죄의 건수는 인구수와 사업체수와 강한 상관관계를 보여줌</br>
 &nbsp;&nbsp;&nbsp; 안전한 서울을 위해 인구당 CCTV 비율이 낮을 곳을 위주로 설치(정비)하면 안전한 서울을 만들 수 있을것이라 판단</br>
 ![결론](https://github.com/suhyun0115/crime_project/assets/151902232/314cde95-b0ec-4071-8993-285b5d3a3335)

## IV. 자료출처
 &nbsp;&nbsp;&nbsp; 1) 범죄율 : https://data.seoul.go.kr/dataList/316/S/2/datasetView.do</br>
 &nbsp;&nbsp;&nbsp; 2) 경찰서 : https://www.data.go.kr/data/15054711/fileData.do</br>
 &nbsp;&nbsp;&nbsp; 3) 주소 GPS 변경 : 카카오API (https://developers.kakao.com/)</br>
 &nbsp;&nbsp;&nbsp; 4) CCTV위치 : https://www.bigdata-policing.kr/product/view?product_id=PRDT_468</br>
 &nbsp;&nbsp;&nbsp; 5) 서울 지역구별 지방세 : https://data.seoul.go.kr/dataList/DT201004O140020/S/2/datasetView.do</br>
 &nbsp;&nbsp;&nbsp; 6) 서울 지역구별 인구 : https://data.seoul.go.kr/dataList/419/S/2/datasetView.do</br>
      
