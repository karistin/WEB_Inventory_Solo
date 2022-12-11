# Inventory

<image src = "./image/erp.jpg"
width=300
height =300>  
[pptLink](https://github.com/karistin/WEB_Inventory_Solo/blob/master/InventoryPPT.pptx)

## 목표

창고정리는 **군내에서 복잡하고 어려운 물류관리를 쉅게 하기위해** 만든 프로젝트 입니다.

- 창고에 쌓인 **재고을 추가하고 제거하거나 찾을수도** 있다.
- 재고가 창고에서 이동하는 경우 **그 기록이 남는다.**
- 재고 각 각의 **상태확인 및 입고**가 가능하다.
- 기존의 엑셀이나 군에서 일일이 손으로 작성한 장부보다와 달리 데이터의 로그가 기록하여 물류체계의 어려움을 극복할 수 있다.  

---

## 참여 인원

### 팀이름 :인벤토리

- **육군 일병 강성준**  seongjung1109@gmail.com /
- 개발기간  **2019/10/21~2019/10/24(3일)**

### 구성 환경및 의존성

- chrome 사용 권장(localhost)
- node > 6.9.0
- Vue.js

```json
"dependencies": {
    "axios": "^0.19.0",
    "core-js": "^3.3.2",
    "element-ui": "^2.12.0",
    "vue": "^2.6.10",
    "vue-arc-counter": "^3.1.0",
    "vue-material-checkbox": "^2.2.0",
    "vue-router": "^3.1.3",
    "vuex": "^3.1.1"
  }
```

### 실행

``` bash
> git clone <https://github.com/karistin/WEB_Inventory_Solo.git>
> npm install    # 의존성 설치
> npm run serve  # (localhost:8080)
```

## 소개

### 1. 창고에 재고 추가(mainpage)

> 창고에 새로운 물품이 오면 Product-Name에 마우스를 오버하면 추가 삭제 기능이 나온다. 여기서 물품을 추가하면 추가한 기록이 History에 저장된다. 또한 각 물품의 일렬번호가 있다면 Repair창에서 입력할 수 있다. 새로운 재고는 4가지 정보를 입력해야 된다. 물품 이름 , 갯수 , 구식/신식 ,날짜를 입력받는다. 검색 기능의 경우 재고의 이름으로 검색할 수 있고 재고를 클릭시 재고의 상태를 볼수도 있다.

<image src = "./image/mainpage.jpg"
width=600
height =300>

- 메인 페이지  
- 현제 기록된 재고물품 상태
- 통계 데이터
- 새로운 상품 추가  

<image src = "./image/add.jpg"
width=300
height =250>

- 상품 이름과 수량 타입(구식, 신식) 날짜를 기록 가능
- mainpage에서 추가가능  

---  

### 2. 정보 수정하기 (/repair)

<image src = "./image/repair.jpg"
width=200
height =150>

> 각 각의 재고의 일렬번호를 추가하고 일렬번호 삭제 추가가 가능하다. 삭제시 여러개를 한번에 삭제가 가능하다.

### 3. 로그 페이지(/history)

<image src = "./image/history.jpg"
width=200
height =150>

> 상품의 추가 날짜에 대한 로그를 볼 수 있다.  

## 파일 정보 및 목록 (File Manifest)

    @/src
      Views: 프로젝트에 사용된 컴포넌트 폴더
      Home:  첫화면  폴더  
        **Home.vue:  테이블을 구성하는 컴퍼넌트**
        **Rmenu.vue/Lmenu.vue/Midmenu.vue/date.vue:  Home 을 구성하는 내용이 있는 컴퍼넌트**
        **ArcCounter.vue:  그래프를 표시하기 위한 내용이  있는 컴포넌트**
        **Graph.vue :  그래프의 데이터가 있는 컴퍼넌트**
        **Footer.vue:  페이지 아래에 대한 내용이 있는 컴포넌트**
        **About.vue : about에 대한 내용이 있는 컴퍼넌트**
      History.vue: history에 대한 내용이 있는 컴퍼넌트
      Repair.vue : repair 에 대한 내용이 있는 컴퍼넌트
      components : 로직이 들어간 폴더
      Addstorge.vue : ProductName추가를 위한 내용이 있는 뷰
      Router.js : 라우팅 기능
      main.js : 확장자 입력 등등
      App.vue : 탭 기능 구현
      GlobalBus.js : 데이터 저장소

## 알려진 버그 (Known Issues)

- 탭을 더불 클릭시 경고가 뜸

## 문제 발생에 대한 해결책 (Troubleshooting)

- none  

## 크레딧 (Credit)

Core by **[Vue.js](https://vuejs.org/)**  
UI by **[element-ui](https://element.eleme.io/)**  
Thanks to **[국방부오픈소스아카데미](https://osam.kr/)**  
[웹동네](http://webdongne.com) **김춘경 멘토**님 감사드립니다.

## 업데이트 정보 (Change Log)

- ver 1.0.0

## 후기

> 지금와서 돌아보면 vue.js에 대한 개념도 없는 상태로 3일만에 어떻게 했는지 놀라웠고 아숴웠던 것은 생각보다 사전에 팀을 구성한 사람들이 많이 있었고 너무 늦게 깨달았다. 우리 부대에서는 내가 처음으로 진출했던 해커톤이기에 내심 좋았다.  
