## backtick을 활용한 코드 표시
- 형태
```
```프로그램명
코드 내용```
```

- 주의 사항 : 프로그램 명을 기재하지 않으면 컬러가 아닌 흑백으로 표시됨

![logo](https://user-images.githubusercontent.com/80403988/136531547-2361d5f1-24bb-4028-a06a-e4ce012f7c2c.png)

<img width="887" alt="스크린샷 2021-10-14 오전 1 04 17" src="https://user-images.githubusercontent.com/80403988/137171683-fbb45d64-9d40-45f2-ad4d-85481fae5857.png">

<img width="796" alt="스크린샷 2021-10-20 오후 1 11 43" src="https://user-images.githubusercontent.com/80403988/138027186-fedb6fa9-1f2f-4f5c-a573-536c2a8331fb.png">

<img width="800" alt="스크린샷 2021-10-20 오후 2 39 10" src="https://user-images.githubusercontent.com/80403988/138034439-6cc1a208-7c93-4701-84a1-9ffc86517a0e.png">

<img width="400" alt="스크린샷 2021-10-20 오후 6 09 38" src="https://user-images.githubusercontent.com/80403988/138064375-4bda5d15-eefb-413d-87d6-1c1f0d543ec5.png">

- API

<img width="700" alt="스크린샷 2021-10-25 오후 1 52 52" src="https://user-images.githubusercontent.com/80403988/138636598-8c8c8aad-1839-411b-9326-a8c914968b84.png">

<img width="700" alt="스크린샷 2021-10-25 오후 1 53 04" src="https://user-images.githubusercontent.com/80403988/138636602-c8961b10-d2cb-4a12-987d-ccbbf801ea5b.png">

<img width="700" alt="스크린샷 2021-10-25 오후 1 53 14" src="https://user-images.githubusercontent.com/80403988/138636608-17c7e50a-6a69-4867-a7da-a9aa9aa80a15.png">

<img width="700" alt="스크린샷 2021-10-25 오후 1 53 33" src="https://user-images.githubusercontent.com/80403988/138636613-1fd60f13-dbd9-4859-a31a-e25c639df8d5.png">

<img width="700" alt="스크린샷 2021-10-25 오후 1 53 43" src="https://user-images.githubusercontent.com/80403988/138636619-e31e8830-891e-424f-93e7-e4cc5fb3ff30.png">

![hometownalba](https://user-images.githubusercontent.com/80403988/141236509-0747eebd-3a81-45dd-b403-222a0e1d5801.png)



```html

  <body>
    <div id="root"></div>
    
    <script type="text/javascript" src="//dapi.kakao.com/v2/maps/sdk.js?appkey=API키&libraries=services"></script>
    
  </body>


```

```js
import React, { useEffect } from "react";
const { kakao } = window;

export default function Map() {

  useEffect(()=>{
    let mapContainer = document.getElementById('map') // 지도를 표시할 div 
    
    // 지도의 옵션 설정
    let mapOption = { 
        center: new kakao.maps.LatLng(33.450701, 126.570667), // 지도의 중심좌표
        level: 3 // 지도의 확대 레벨
    };
  
    // 지도를 표시할 div와  지도 옵션으로  지도를 생성합니다
    var map = new kakao.maps.Map(mapContainer, mapOption); 
  }, [])

  return(
    <div
    id="map"
    style={{
      width: "80%",
      height: "80%",
    }}
    ></div>
  )
}
```



```js
useEffect(()=>{

  axios.get( DB에서 일자리 데이터 불러오기 )

  .then( 기준에 따라 데이터 필터링 )

  .then ( //지도 API 기능 활용

    지도 화면에 띄우기

    지도 이동 이벤트 등록

    렌더링 시점에 지도 위치 지정

    검색 기능 입력

    반복문 : 일자리별 마커 표시하기

    마커에 이벤트 등록하기

  )
}, [지도 위치, 일자리 지원, 데이터 필터링 기준, 검색 키워드])

return (
  필터링 된 데이터 목록에 띄우기
  지도 표시하기
)
```

```js
var iwContent = `
<div>회사명 : ${data.companyName}</div>
<div>근무시간 : ${data.time}</div>
<div>월급 : ${data.monthlyWage}</div>
<button onclick="${eventHandler}">지원하기</button>
`

let infowindowClick = new kakao.maps.InfoWindow({
  content: iwContent,
  removable: true,
    });
```

```js
let iwContent = document.createElement("div")

let companyName = document.createElement("div")
companyName.textContent = `회사명 : ${data.companyName}`

let time = document.createElement("div")
time.textContent = `근무시간 : ${data.time}`

let monthlyWage = document.createElement("div")
monthlyWage.textContent = `예상 월급여 : ${data[i].monthlyWage}`

let btn = document.createElement("button");
btn.textContent = `지원하기`;
btn.onclick = eventHandler;

iwContent.append(
  companyName,
  time,
  monthlyWage,
  btn
);

let infowindowClick = new kakao.maps.InfoWindow({
  content: iwContent,
  removable: true,
});
```

```js
kakao.maps.event.addListener(map, "dragend", function () {
  // 지도 중심좌표를 얻어옵니다
  let latlng = map.getCenter();
  setApplyLocation([]);
  setSearchLocation("");
  setMapLocation([latlng.Ma, latlng.La]);
});
```
