<h1>☕ StarBucks 페이지 따라하기 </h1>

- **배포 링크 :**  [링크](https://668a6d43101d2cc67fef2240--starbuck-css-pra.netlify.app/)

<br>

<div  align="center">
  <img width="60%" height="350px" src="./images/Starbucks_Capture.gif" alt="Starbucks Page Pra">
</div>

<br>

## 기술 스택 

| JavaScript | CSS | HTML | Netlify |
| :--------: | :-: | :--: | :-----: |
| <div style="display: flex; align-items: flex-start;">
<img src="https://techstack-generator.vercel.app/js-icon.svg" alt="icon" width="75" height="75" /></div> |<div style="display: flex; align-items: flex-start;"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTHPlU1ZjmDtTYorXqiip4hYId_heLT4MJ-1A&s" alt="icon" width="65" height="65" /></div> | <div style="display: flex; align-items: flex-start;"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTw7Bg0HAhKWg54R3kgcsBx3cUUbxn6Uz1WDQ&s" width="65" height="65" /></div> | <div style="display: flex; align-items: flex-start;"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRsi0-_0rMS7qCQwJ5p6fVOeFEWnTbmkCAFDg&s" alt="icon" width="65" height="65" /></div> |

<br>
<br>

## 사용한 라이브러리 & 구현 기능
<br>

- ## 라이브러리 :
   > ## swiper
   슬라이드 라이브러리 다운 [Getting Started Swiper](https://swiperjs.com/get-started) 링크 입니다.

   [Swiper Api](https://swiperjs.com/swiper-api) 로 다양한 Swiper를 활용할 수 있습니다.


  ```javascript
  //Swiper 예시

  new Swiper(요소, 옵션);

  new Swiper('.swiper-container', {
  direction: 'vertical', // 수직 슬라이드
  autoplay: true, // 자동 재생 여부
  loop: true // 반복 재생 여부
  });
  ```

  <br />
  <br />
  
  > ## gsap(scrollTo, scrollMagic)

  [Gsap](https://gsap.com/) 자바스크립트로 제어하는 타임라인 기반의 애니메이션 라이브러리 입니다.

  [ScrollToPlugin](https://gsap.com/scrolltoplugin/) 스크롤 애니메이션을 지원하는 Gsap 플러그인 입니다.

    ```javascript

  <!-- Gsap 예시 _ script 연결-->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.5.1/gsap.min.js" integrity="sha512-IQLehpLoVS4fNzl7IfH8Iowfm5+RiMGtHykgZJl9AWMgqx0AmJ6cRWcB+GaGVtIsnC4voMfm8f2vwtY+6oPjpQ==" crossorigin="anonymous"></script>
  
  <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.5.1/ScrollToPlugin.min.js" integrity="sha512-nTHzMQK7lwWt8nL4KF6DhwLHluv6dVq/hNnj2PBN0xMl2KaMm1PM02csx57mmToPAodHmPsipoERRNn4pG7f+Q==" crossorigin="anonymous"></script>


  // Gsap 사용 예시

  gsap.to(요소, 시간, 옵션)
  // or
  TweenMax.to(요소, 시간, 옵션)

  gsap.to(window, .7, {
  scrollTo: 0
  });
  ```

  <br />
  <br />

  >  ## ScrollMagic
  [ScrollMagic](https://scrollmagic.io/docs/) 스크롤에 따른 요소의 상태를 제어하기 위한 자바스크립트 라이브러리 입니다. 
  <br />

  ```javascript
  <!-- ScrollMagic 예시 _ script 연결-->

  <script src="https://cdnjs.cloudflare.com/ajax/libs/ScrollMagic/2.0.8/ScrollMagic.min.js"></script>

  // ScrollMagic 사용 예시

  new ScrollMagic
  .Scene({ // 감시할 장면(Scene)을 추가
  triggerElement: spyEl, // 보여짐 여부를 감시할 요소를 지정
  triggerHook: .8 // 화면의 보여지는 여부 지점 설정. (80%)
  })
  .setClassToggle(spyEl, 'show') // 요소가 화면에 보이면 show 클래스 추가
  .addTo(new ScrollMagic.Controller()) // 컨트롤러에 장면을 할당 (필수 요소)

  ```



  <br />
  <br />

  >  ## Lodash

  [Lodash](https://lodash.com/docs/4.17.15) 다양한 유틸리티를 제공하는 자바스크립트 라이브러리 입니다.
  <br/>
  [LodashThrottle](https://lodash.com/docs/4.17.15#throttle) 외에도 
  (.filter, .map, .debounce, .merge, throttle ...) 등이 있습니다.



  <br />
  <br />
   
  > ## YoutubeApi
  [IFrame Player Api](https://developers.google.com/youtube/iframe_api_reference?hl=ko)를 통해 Youtube 동영상을 제어할 수 있습니다.

  Youtube 동영상이 출력될 위치에 요소를 생성합니다.
  
  [플레이어 매개변수(PlayerVars)](https://developers.google.com/youtube/player_parameters.html?playerVersion=HTML5&hl=ko#Parameters) 에 더 많은 영상 제어 옵션이 있습니다.

  ```html
  <!-- IFrame Player Api 사용 예시 _ 영상 출력 위치에 요소 생성 -->
  <!-- in HEAD -->
  <script defer src="./js/youtube.js"></script>

  <!-- in BODY -->
  <div id="player"></div> 
  ```
 


  ```javascript
    // IFrame Player Api 사용 예시

    var tag = document.createElement('script');
    tag.src = "https://www.youtube.com/iframe_api";
    var firstScriptTag = document.getElementsByTagName('script')[0];
    firstScriptTag.parentNode.insertBefore(tag, firstScriptTag);

    function onYouTubePlayerAPIReady() {  
      //onYouTubePlayerAPIReady 은 IFrame Player API에서 지정된 함수 이름 입니다.
    // <div id="player"></div>
    new YT.Player('player', {
      videoId: 'An6LvWQuj_8', // 재생할 유튜브 영상 ID
      playerVars: {
        autoplay: true, // 자동 재생 유무
        loop: true, // 반복 재생 유무
        playlist: 'An6LvWQuj_8' // 반복 재생할 유튜브 영상 ID 목록
      },
      events: {
        // 영상이 준비되었을 때,
        onReady: function (event) {
          event.target.mute();  // 음소거
        }
      }
    });
    }

  ```


  
<br><br>

- ## 기능들 :
  >  ## 오픈그래프
  
  [오픈그래프](https://ogp.me/)
<br/>
 사이트 공유 시 필요한 내용들을 설정하는 기능입니다.
 <br />
 <br />
    ```html
      <meta property="og:type" content="website" />
      <meta property="og:site_name" content="Starbucks" />
      <meta property="og:title" content="Starbucks Coffee Korea" />
      <meta property="og:description"
        content="스타벅스는 세계에서 가장 큰 다국적 커피 전문점으로, 64개국에서 총 23,187개의 매점을 운영하고 있습니다."
      />
      <meta property="og:image" content="./images/starbucks_seo.jpg" />
      <meta property="og:url" content="https://starbucks.co.kr" />
    ```

- `og:type`: 페이지의 유형(E.g, `website`, `video.movie`)
- `og:site_name`: 해당 사이트의 이름
- `og:title`: 페이지의 이름
- `og:description`: 해당 페이지 설명
- `og:image`: 페이지의 대표 이미지
- `og:url`: 페이지 주소

   <br />
   <br />

  >  ## 트위터카드
  
   [트위터카드](https://developer.x.com/en/docs/x-for-websites/cards/overview/abouts-cards)
 <br />
 트위터로 공유 시 필요한 내용들을 설정하는 기능입니다.

  <br />
 
    ```
    <meta property="twitter:card" content="summary" />
      <meta property="twitter:site" content="Starbucks" />
      <meta property="twitter:title" content="Starbucks Coffee Korea" />
      <meta property="twitter:description"
      content="스타벅스는 세계에서 가장 큰 다국적 커피 전문점으로, 64개국에서 총 23,187개의 매점을 운영하고 있습니다."
      />
      <meta property="twitter:image" content="./images/tarbucks_seo.jpg" />
      <meta property="twitter:url" content="https://starbucks.co.kr" />
    ```

- `twitter:card`: 카드(페이지)의 유형
- `twitter:site`: 해당 카드의 이름
- `twitter:title`: 카드의 이름
- `twitter:description`: 해당 카드 설명
- `twitter:image`: 카드의 대표 이미지
- `twitter:url`: 카드 주소
  
  <br />
