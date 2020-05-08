## Install Spec Guide
1. JAVA 1.8
2. Tomcat 8.5

## [Error & Solution]
1. [SPRING] 절대 uri : http://java.sun.com/jsp/jstl/core는 web.xml 또는이 응용 프로그램과 함께 배포 된 jar 파일에서 확인할 수 없습니다.
> pom.xml에 다음과 같이 디펜던시 추가 후 필요한 jar 파일을 WEB-INF 아래 lib 폴더에 추가합니다.
> lib 폴더가 없을 경우 만들어야 합니다.
```
<dependency>
	<groupId>javax.servlet</groupId>
	<artifactId>jstl</artifactId>
	<version>1.2</version>
</dependency>
```
2. ... 요소에 대한 선언을 찾을 수 없습니다.
> bean 설정파일(servlet-context.xml)을 살펴봅니다.
> > example) 'component-scan' error -> context:component-scan, 'property' error -> beans:property