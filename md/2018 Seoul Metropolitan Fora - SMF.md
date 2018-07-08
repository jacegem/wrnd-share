---
customTheme : "my-theme"
theme : "night"
transition: "slide"
transitionSpeed: 'slow'
highlightTheme: "darkula"
---

## 2018 Seoul Metropolitan Fora (SMF)

2018.07.06(금)

![](https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Seoul_Museum_of_History.JPG/580px-Seoul_Museum_of_History.JPG)

---

## Integrating 3D Models, Sensors, and Simulations with the Smart District Data Infrastructure

Tomas Kolbe (Professor, Technical University of Munich, Germany)

토마스 콜베 (교수, 뮌헨공과대학교, 독일)

--

### The Urban Challenge

- More than 50% of all humans live in cities
  - likely to increase to 70% until 2050
- Climate change - energy and environment
  - most energy is consumed in/by cities
  - cities & the urban work and life are responsibel for the majority of the emissions of green house gases
  - reduction of emissions urgently required
- Concentration of production and traffic
  - stress of the local envrionmental (air and water pollution, noise)
  - mobility / traffic flows
- Urban development must consider all these aspects simultaneously - and at the same time getting more efficient

--

### Smart Cities

- `Working Definition` of the British Standards Institute:
  - 'Smart cities' is a term denoting the effective integrations of physical, digital and human systems in the built environment to deliver a sustainable, prosperous and inclusive futuer for its citizens.
- potential turnover world wide of 'Smart Citieis' until 2020: 1.5 trillion US Dollars
- strongly driven and propagated by ITC companies & research institutions, nowadays increasingly adopted by municipalities

---

## CityGML

- 홈페이지: https://www.citygml.org/
- [CityGML 2.0, 3.0 주요 개념 및 구조](https://sites.google.com/site/bimprinciple/in-the-news/citygml30juyogaenyeommichgujo)
- [CityJSON](http://www.cityjson.org/en/0.6/)
- https://github.com/3dcitydb/tutorials

---

## val3dity

- https://github.com/tudelft3d/val3dity

val3dity---pronounced 'val-three-dity'---allows us to validate 3D primitives according to the international standard ISO19107.
Think of it as [PostGIS ST_IsValid](http://postgis.net/docs/ST_IsValid.html), but for 3D primitives (PostGIS only validates 2D primitives).

In short, it verifies whether a 3D primitive respects the definition as given in [ISO19107](http://www.iso.org/iso/catalogue_detail.htm?csnumber=26012) and GML/CityGML.
All the 3D primitives of GML are supported:

- `<gml:MultiSurface>`
- `<gml:CompositeSurface>`
- `<gml:Solid>`
- `<gml:MultiSolid>`
- `<gml:CompositeSolid>`

Unlike many other validation tools in 3D GIS, inner rings in polygons/surfaces are supported and so are cavities in solids (also called voids or inner shells).
However, as is the case for CityGML, only planar and linear primitives are allowed: no curves or spheres or other parametrically-modelled primitives are supported. There is no plan to support these geometries, because val3dity is developed with 3D city models in focus.

val3dity accepts as input:

- [CityGML](https://www.citygml.org)
- [CityJSON](http://www.cityjson.org)
- [GML files](https://en.wikipedia.org/wiki/Geography_Markup_Language) of any flavour
- [OBJ](https://en.wikipedia.org/wiki/Wavefront_.obj_file)
- [OFF](<https://en.wikipedia.org/wiki/OFF_(file_format)>)

---

## 통합공간정보시스템(SDW)사례 소개

Smart City 기본 인프라는?

- 공간정보(GeoSpatial Information)

각 부서에서 관리하는 공간정보를?

- 누구나 쉽게 찾고 활용 할 수 있는 시스템 필요

공간(**S**patila) + 데이터(**D**ata) + 창고(**W**arehouse)

--

## SDW, Data 제공은?

8 개 부서 613 종 제공

- 빅데이터플랫폼 (45)
- 도로굴착복구시스템 (74)
- 디지털시민시장실(202)
- 열린데이터광장 (108)
- 도로관리시스템 (47)
- 토지관리과 (3)
- 주차관리시스템 (75)
- 119 종합전산정보시스템 (59)

--

## Voxel

![복셀 엔진 에디터로 만든 Nod의 어택 바이크](https://namu.wiki/w/%ED%8C%8C%EC%9D%BC:external/goto2020.cdn1.cafe24.com/04.gif)

- 복셀은 2 차원적인 픽셀(도트)을 3 차원의 형태로 구현한 것
- Voxel 은 Volume + Pixel 의 합성어로 '**부피를 가진 픽셀**'
- 작은 정육면체 또는 부피요소로 나눠질 수 있는 오브젝트를 렌더링하는 기술
- 하나의 공간을 빈틈없이 채울 수 있는 정육면체

복셀그래픽에서 모든 복셀의 모양과 크기는 동일하며 하나의 복셀은 하나 이상의 특성값(파라미터)을 가질 수 있다. 특성값을 전혀 갖지 않는 복셀그래픽도 가능은 하지만 그리 유용하지는 않고(정의하는 복셀 공간 전체가 똑같은 복셀로 가득찬 덩어리 하나만 존재할 수 있는데 유용할리가) 보통 색상값 정도의 특성값 정보는 가지고 있다. 물론 색상값 이상의 정보도 담을 수 있는데, 이 점을 이용하여 복셀 표면의 텍스처 정보를 저장해 만든 것이 바로 마인크래프트이다. 구체적으로는 복셀의 블럭 ID 값과 추가 상태 정보(내구도 등)를 저장하고 있으며 마인크래프트의 렌더링 엔진은 복셀의 블럭 ID 값에 따라 텍스처 라이브러리에서 정육면체 텍스처를 불러와 복셀 표면을 렌더링한다. 단, 블럭에만 한정하고 캐릭터나 엔티티(꽃 같은 것)는 폴리곤 그래픽이다. 산업적으로는 엑스선, 음극선, 자기 공명 영상(MRI) 등에서 복셀그래픽을 사용한다.
