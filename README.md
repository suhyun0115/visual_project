# ✒️서울 지역구별 범죄건수와 경찰서 또는 CCTV의 상관관계 분석
## 👥 Team
- Team name : HEE
- Team members : 함은규, 이수현, 이지우
- * :clock1:시작일 : 2023.12.08(금)
  * ⏰목표일 : 2023.12.11(월)
## :books: skill
- **Programming** <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=Python&logoColor=white"> <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=Python&logoColor=white"> <img src="https://img.shields.io/badge/Matplotlib-3776AB?style=for-the-badge&logo=Matplotlib&logoColor=white"> <img src="https://img.shields.io/badge/Seaborn-3776AB?style=for-the-badge&logo=Seaborn&logoColor=white"> <img src="https://img.shields.io/badge/Folium-3776AB?style=for-the-badge&logo=Folium&logoColor=white">
- **Tools** <img src="https://img.shields.io/badge/jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white"> <img src="https://img.shields.io/badge/googlecolab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white">
- **Git** <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=jupyter&logoColor=white"> <img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white">

## 목차(INDEX)
&emsp;&ensp;Ⅰ. 주제 선정</br>&emsp;&ensp;Ⅱ. Data preprocessing</br>&emsp;&ensp;Ⅲ. 시각화</br>&emsp;&ensp;Ⅳ. 결론</br>&emsp;&ensp;

## Ⅰ. 주제선정
  **1. 서울 지역구별 범죄 건수와 경찰서, CCTV 상관관계 분석**</br>
       &nbsp;&nbsp;&nbsp; 범죄에 영향을 미치는 주요 요인 분석

       
## Ⅱ. 분석
**1. 서울시 구별 범죄율, 경찰서, CCTV 위치 표기</br>
![image](https://github.com/suhyun0115/visual_project/assets/151905249/dc31b4f7-4a44-40d1-9fe0-9860ed8bdf12)


**1. 데이터 기본분석(1)**</br>
       &nbsp;&nbsp;&nbsp; 1) 범죄건수가 많은 지역 : 강남구 > 송파구 > 관악구</br>
       &nbsp;&nbsp;&nbsp; 2) 지역구별 특징 : 강남구 > 마포구 > 서초구 (범죄 유형 : 강간, 강제추행)</br>
   ![image](https://github.com/suhyun0115/visual_project/assets/151905249/640677cb-33f8-486e-b925-1b5c257b05ba)

       
**2. 데이터 기본분석(2)**</br>
       &nbsp;&nbsp;&nbsp; 1) 지역구별 건수 비교 : 범죄건수 vs 경찰서 갯수 vs CCTV 갯수</br>
       &nbsp;&nbsp;&nbsp; 2) 지역구별 비율 비교 : 범죄비율 vs 경철서비율 vs CCTV비율</br>
   ![image](https://github.com/suhyun0115/visual_project/assets/151905249/6092763d-69e0-4322-82e2-909a746b511d)
   ![image](https://github.com/suhyun0115/visual_project/assets/151905249/ad7b712f-a111-497f-8df8-7bbfe69d9ae3)



**5. 중간 결론 : CCTV가 증가하면 범죄율을 줄이는 효과가 있을 수 있다.**</br>
       &nbsp;&nbsp;&nbsp; 1) . 상관계수(0.65)로 보면 범죄율에 따라 CCTV비율이 증가하는 것으로 판단할 수 있으나 비중이 한쪽으로 집중되어 있는 것이 보이며, CI가 확장되어 상호관계가 명확하지 않음</br>
       &nbsp;&nbsp;&nbsp; 2) CCTV증가에 따른 CCTV당 범죄를 확인해 보면 CCTV가 증가함에 따라 범죄율이 줄어는 것을 볼수있다</br>
       &nbsp;&nbsp;&nbsp; 3)  그러나 그 한계점이 있을 것으로 사료된다</br>
    ![image](https://github.com/suhyun0115/visual_project/assets/151905249/6e03a957-bd4a-4d26-99ee-f5fbef35316c)

  

**6. 다른 원인 분석 : 범죄건수 vs 범죄 유형별 vs 인구수, 사업체수, 재산세, CCTV**</br>
       &nbsp;&nbsp;&nbsp; 1)  범죄건수는 폭력과 절도와 강한 상호관계(큰 비증)가 있음(폭력범죄는 절도와 강간·강제추행과 서로 관계성이 있음) </br>
       &nbsp;&nbsp;&nbsp; 2) 범죄건수와 지역구의 인구수와 사업체수에 상호 관계를 갖으나 지역구의 인구수와 사업체수는 서로 독립 변수임다</br>
       ![image](https://github.com/suhyun0115/visual_project/assets/151905249/04804360-7f35-4126-9fbd-e66286880d30)
       ![image](https://github.com/suhyun0115/visual_project/assets/151905249/3a3d87cf-304d-48fe-b465-7d3579fc7659)



**7. 이상값(강남구) 제외 **</br>
       &nbsp;&nbsp;&nbsp; 강남구를 제외하면 CI 구간이 축소되는 것을 확인할 수 있다</br>
       ![image](https://github.com/suhyun0115/visual_project/assets/151905249/2a1e93d2-2641-4d01-a01b-2ce9c0b0914b)

     

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
      
