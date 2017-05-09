###分页标签使用说明

1. 把tld文件夹放到WEB-INF下
2. 把NavigationTag与Page放入工程对应包下
2. 构造Page对象填充下列属性:

		Page<Customer> page = new Page<>();
        page.setTotal(count);           //数据总数
        page.setSize(getSize());     //每页显示条数
        page.setPage(getPage());     //当前页数
        page.setRows(resultList);       //数据列表

3. jsp页面引入下面的标签:
	<%@ taglib prefix="m" uri="/WEB-INF/tld/page.tld" %>
4. 在jsp页面中使用分页:
	<m:page url="${pageContext.request.contextPath }/customer/list.action" />