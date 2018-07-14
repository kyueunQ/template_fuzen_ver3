# Template_fuzen_ver.3



## Main Page 구성

- About Us
- 이모티콘 제작 과정
- Service 소개
- 비용

[]: http://v.media.daum.net/v/20171212112222575?f=p	"낮아진 이모티콘 시장장벽"



### CSS 

- layouts을 부분적으로 적용할 수 있을까?

  - http://guides.rubyonrails.org/layouts_and_rendering.html

  - http://api.rubyonrails.org/classes/ActionView/Layouts.html

  - `controller`에서 `layout false`를 선언하니 해당 main_page 뷰에는 기존에 *app/views/layouts/application.rb*에서 설정한 nav, side 등이 적용되지 않았다. 

  - 그런데 `Carousel`기능까지 작동되지 않아서 *app/views/layouts/application_main.rb*를 새로 만들었고,

    아래와 같이 추가하니 작동을 했다.

    *app/controllers/mainpages.controller.rb*

    ```ruby
    class MainPagesController < ApplicationController
        layout "application_main"
        ...
        
    end
    ```

    

### 계획

- nav바 버튼 클릭시, 해당 부분으로 물 흐르듯 부드럽게 이동하기
- 가이드의 개요 list 추가하기