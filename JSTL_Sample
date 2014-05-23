<%@ page language="java" import="java.util.*" pageEncoding="UTF-8"%>
<%@ page import="com.test.domain.Person"%>
<%@ taglib uri="http://java.sun.com/jsp/jstl/core" prefix="c"%>
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN">
<html>
  <head>
    
    <title>JSTL中的c:forEach</title>
    
	<meta http-equiv="pragma" content="no-cache">
	<meta http-equiv="cache-control" content="no-cache">
	<meta http-equiv="expires" content="0">    
	<!--
	<link rel="stylesheet" type="text/css" href="styles.css">
	-->

  </head>
  
  <body>
  <%
  String str[] = {"a", "b", "c","d"};
  pageContext.setAttribute("str", str);
   %>
  <c:forEach items="${str}" var="s">
  	${s}<br/>
  </c:forEach>
  <hr/>
  <%
  String s1[] = {"a", "b", "c", "d", "e", "f", "g"};
  pageContext.setAttribute("s1", s1);
   %>
   <c:forEach items="${s1}" var="s" begin="1" end="5" step="2">
    ${s}<br/>
   </c:forEach>
  <hr/>
  <%
  Map<String, String> map = new LinkedHashMap<String, String>();
  map.put("1", "aaa");
  map.put("2", "bbb");
  map.put("3", "ccc");
  map.put("4","ddd");
  pageContext.setAttribute("map", map);
  %>
  <c:forEach items="${map }" var="me">
  	${me.key }: ${me.value}<br/>
  </c:forEach>
  <hr/>
  <br/>
  <%
  List<Person> list = new ArrayList<Person>();
  	list.add(new Person("葛付以","1",true));
	list.add(new Person("余睿","1",false));
	list.add(new Person("朱巧玲","0",false));
	list.add(new Person("蒋小平","0",false));
	list.add(new Person("邹海洋","1",true));
	list.add(new Person("董泽坤","1",false));
	list.add(new Person("梁胜海","1",false));
	pageContext.setAttribute("ps", list);
   %>
   <!-- gender: 1 代表男， 0 代表女  married： true代表已婚，false代表未婚 -->
   <c:forEach items="${ps}" var="user">
   	${user.name}:${user.gender=="1"?"男":"女"}:${user.married?"已婚":"未婚"}<br/>
   </c:forEach>
   <hr/>
   <br/>
   <table border="1" width="60%">
   	<tr>
   		<th>索引</th>
   		<th>顺序</th>
   		<th>第一个</th>
   		<th>最后一个</th>
   		<th>姓名</th>
   		<th>性别</th>
   		<th>婚姻</th>
   	</tr>
   	<c:forEach items="${ps}" var="user" varStatus="vs">
   		<tr bgcolor="${vs.index%2==0?'#CFCFCF':'#9D2266'}" align="center">
   			<td>${vs.index}</td>
	   		<td>${vs.count}</td>
	   		<td>${vs.first}</td>
	   		<td>${vs.last}</td>
	   		<td>${user.name}</td>
	   		<td>${user.gender=="1"?"男":"女"}</td>
	   		<td>${user.married?"已婚":"未婚"}</td>
   		</tr>
   	</c:forEach>
   </table>
  </body>
</html>
