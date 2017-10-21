#1.JSTL core标签库使用时注意事项

**①jsp页面添加指令**
```
<%@ taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>
```
**②maven导入jstl包**

#2.maven中pom.xml配置的依赖关系
>MD5加密DigestUtils-->codec包			
>StringUtils-->lang3包
数据库连接-->mysql					
Apache数据库连接池-->dbcp2
DbHelp工具类-->dbutils				
转换成json-->google-gson
jstl core标签库-->jstl+指令		

#3.mvn项目配置pom.xml依赖的jar包
```
mvn配置
<properties>
    <commons-codec-version>1.10</commons-codec-version>
    <commons-dbutils-version>1.6</commons-dbutils-version>
    <commons-dbcp2-version>2.1.1</commons-dbcp2-version>
    <commons-lang3-version>3.4</commons-lang3-version>
    <gson-version>2.2.4</gson-version>
    <mysql-version>5.1.38</mysql-version>
	<jstl-version>1.2</jstl-version>
</properties>
  
	
<dependencies>
  
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>3.8.1</version>
      <scope>test</scope>
    </dependency>

    <dependency>
	    <groupId>javax.servlet</groupId>
	    <artifactId>javax.servlet-api</artifactId>
	    <version>3.1.0</version>
	    <scope>provided</scope>
	</dependency>

    <dependency>
	    <groupId>commons-codec</groupId>
	    <artifactId>commons-codec</artifactId>
	    <version>${commons-codec-version}</version>
	</dependency>
  
    <dependency>
	    <groupId>commons-dbutils</groupId>
	    <artifactId>commons-dbutils</artifactId>
	    <version>${commons-dbutils-version}</version>
	</dependency>
  
    <dependency>
	   <groupId>com.google.code.gson</groupId>
	   <artifactId>gson</artifactId>
	   <version>${gson-version}</version>
	</dependency>
	
	<dependency>
	    <groupId>jstl</groupId>
	    <artifactId>jstl</artifactId>
	    <version>${jstl-version}</version>
	</dependency>
	
	<dependency>
	    <groupId>mysql</groupId>
	    <artifactId>mysql-connector-java</artifactId>
	    <version>${mysql-version}</version>
	</dependency>
	
	<dependency>
	    <groupId>org.apache.commons</groupId>
	    <artifactId>commons-dbcp2</artifactId>
	    <version>${commons-dbcp2-version}</version>
	</dependency>
	
	<dependency>
	    <groupId>org.apache.commons</groupId>
	    <artifactId>commons-lang3</artifactId>
	    <version>${commons-lang3-version}</version>
	</dependency>
	
</dependencies>
```





