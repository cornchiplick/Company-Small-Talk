# 3/3
### 1. svn
- subclipse 4.3.3 설치 -> [perspective]에서 svn repository exploring
-> 있는것 다 check out
> svn://203.239.45.230:33688/xclick_edu/xclickr3_edu_2303

### 2. new server - tomcat 9.0

### 3. server jvm edit
> -DinstanceId=1
> -DsiteId=BZ
> -DrunMode=DEBUG

### 4. server.xml edit

### 5. web.xml edit (web)
- sql.path, config.path

### 6. xclick-config.xml
- domain, contextpath, port, repository, resource path

### 7. build.properties

### explain..
gw = src -> ant build -> lib / ..jar
resource - css, image ...
web - webRoot / jsp

---
---
<br>

# 3/6
### eclipse 없이 tomcat 서버 띄워서 [gw] (http://localhost:6001/demo) 띄우기
1. war파일 webapps-root 아래에 넣기
2. catalina.bat 에 아래 설정 추가하기
> set JAVA_OPTS=%JAVA_OPTS% -DinstanceId=1
> set JAVA_OPTS=%JAVA_OPTS% -DsiteId=BZ
> set JAVA_OPTS=%JAVA_OPTS% -DrunMode=DEBUG

3. server.xml 수정하기

---

- XclickController : facade 호출 후, jsp 호출시 사용하는 컨트롤러
- JspController : 위와 순서 반대
> 특별한 경우가 아니면 XclickController 를 사용함을 원칙으로 한다.

- DownController : file 다운할때 씀

---
- `FormData` : jsp의 입력 데이터를 담는 통합적인 class
- 모든 vo 객체는 `BaseVO`를 상속받는다.
- `BaseVO`는 `FormData`를 상속받는다.


---
- BaseFacade : Facade Class의 기본 클래스로서 사용자 Facade는 BaseFacade 를 **반드시** 상속받아서 작성해야 한다.
- BaseDAO : DAO Class 의 기본 클래스로서 이 BaseDAO를 **반드시** 상속받아서 작성해야 한다.

---
---
<br>

# 3/7
- include `common.jsp` 하기

---
---
<br>

