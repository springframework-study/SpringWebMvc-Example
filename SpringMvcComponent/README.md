# 스프링 MVC 구성 요소

## DispatcherSerlvet의 기본 전략
+ DispatcherServlet.properties

## MultipartResolver
+ 파일 업로드 요청 처리에 필요한 인터페이스
+ HttpServletRequest를 MultipartHttpServletRequest로 변환해주어 요청이 담고 있는 파일을 꺼낼 수 있는 API 제공

## LoclaeResolver
+ 클라이언트의 위치(Locale) 정보를 파악하는 인터페이스
+ 기본 전략은 요청의 accept-language를 보고 판단

## ThemeResolver
+ 애플리케이션에 설정된 테마를 파악하고 변경할 수 있는 인터페이스
+ 참고: <https://memorynotfound.com/spring-mvc-theme-switcher-example/>

## HandlerMapping
+ 요청을 처리할 핸들러를 찾는 인터페이스

## HandlerAdapter
+ HandlerMapping이 찾아낸 "핸들러"를 처리하는 인터페이스
+ 스프링 MVC ***확장력***의 핵심

## RequestToViewNameTranslator
+ 핸들러에서 뷰 이름을 명시적으로 리턴하지 않은 경우, 요청을 기반으로 뷰 이름을 판단하는 인터페이스

## ViewResolver
+ 뷰 이름(string)에 해당하는 뷰를 찾아내는 인터페이스

## FlashMapManager
+ FlashMap 인스턴스를 가져오고 저장하는 인터페이스
+ FlashMap은 주로 리다이렉션을 사용할 때 요청 매개변수를 사용하지 않고 데이터를 전달하고 정리할 때 사용한다.
+ redirect:/events