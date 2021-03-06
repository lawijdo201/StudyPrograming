Core 태그
===========================
```jsp
<%@ taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>
```
### Core 태그 라이브러리를 사용하기위해 반드시 위의 코드를 선언해야 한다.

<c:set>
-----------------------
* 기능: 변수 지원
* JSP 페이지에서 변수를 지정합니다.

### <c:set var="변수이름" value="변수값" [scope="scope속성 중 하나"] />]

<c:remove>
-----------------------
* 기능: 변수 지원
* 지정된 변수를 제거합니다.

### <c:remove var="변수이름" [scope="scope속성 중 하나"] />]

<c:if>
-----------------------
* 기능: 흐름 제어
* 조건문을 사용합니다.

### <c:if test="${조건식}" [var="변수 이름"] [scope="scope속성 중 하나"] /> 

### ~~~

### </c:if>

#### var은 조건식의 결과값 지정

<c:choose>
-----------------------
* switch문을 사용합니다. <c:when>과 <c:otherwise> 서브 태그를 갖습니다.
### <c:choose>

### <c:when test="조건식1"본문내용1</c:when>

### <c:when test="조건식2"본문내용2</c:when> 

### ~~

### <c:otherwise test=본문내용</c:otherwise>
### </c:choose>

<c:forEach>
-------------------------------------
* 반복문을 사용합니다.

### [<c:forEach var="변수 이름" items="반복할 객체이름" begin="시작값" end="마지막값" step="증가값" varStatus="반복상태변수이름"></c:forEach>](https://github.com/lawijdo201/StudyPrograming/blob/main/JSP/JSTL/c:forEach.jsp)

c:forTokens
--------------------
* 구분자로 분리된 각각의 토큰을 처리할 때 사용합니다.

### <c:forTokens var="변수 이름" items="반복할 객체이름" delems=","> 본문내용 </c:forTokens>

<c:import>
--------------------
* URL 처리
* URL을 이용해 다른 자원을 JSP 페이지에 추가합니다.

<c:url>
------------------
* 요청 매개변수로부터 URL을 생성합니다.
### [<c:ur; var="변수이름" value="URL경로" [scope="scope 속성 중 하나"] [<c:param name="매개변수 이름" value="전달값" />]](https://github.com/lawijdo201/StudyPrograming/blob/main/JSP/JSTL/c:url.jsp)

<c:redirect>
-----------------
* response.sendRedirect()기능을 수행합니다.

### [<c:redirect url="redirect할 URL"> [<c:param name="매개변수이름"value="전달값" />] ~~~ </c:redirect>](https://github.com/lawijdo201/StudyPrograming/blob/main/JSP/JSTL/c:redirect.jsp)

<c:catch>
----------------
* 예외 처리에 사용합니다.

<c:out>
------------------
* |JspWriter에 내용을 처리한 후 출력합니다.

### [<c:out value="출력값" [defalut="기본값"] [escapeXml="boolean값"] />](https://github.com/lawijdo201/StudyPrograming/blob/main/JSP/JSTL/c:out.jsp)

* defalut는 value 속성에 지정된 값이 없을 때 출력할 기본값을 지정

* escapeXml은 escape문자를 변환하는 역활, true이면 출력값 그대로 화면에 표시


### JSTL의 contextPath

<c:set var="contextPath" value="${pageContext.request.contextPath}" />]
