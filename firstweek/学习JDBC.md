1. jdbc是什么
 - java数据库连接，是一种用于执行SQL语句的javaAPI
 - 由一组用java编写的类和接口组成

2. jdbc连接数据库步骤：
 - 加载驱动
 - 连接数据库
 - 使用sql语句操作数据库
 - 执行sql语句
 - 关闭数据库连接，释放资源
 
3. 配置数据库驱动
4. 加载驱动
 class.forname(用户名字)
5. 连接及关闭数据库
 DriverManage.getconnection(url,Username,passname)

void close()

6. 使用Statement接口实现增删改查
 用于执行静态sql语句并返回生成结果的对象

excuteupdate(String sql)

- 添加操作
- 更新操作
- 删除操作
- 
7.使用PreparedStatement实现增删改

- Statement的子接口
- 在数据表中准备了一条sql语句

. Result 结果集的引用
 
- 接口rsult

- boolean next() throws SQLException
- 可以使用foreach遍历查询结果
- String getString(String columnlabel) 获取当前行中指定列的值
8. 处理大数据对象
- 处理CLOB对象（大字符）
- 处理BLOG对象（二进制）
 
输入流inputstream  setAsciistream
setBinarystream

输出流显示图片

9. 使用callablestate  调用存储过程
- preparedstatement的子接口
- 接口的应用
> 
- 过程

10. 
- 使用DantabaseMetaData获取数据库基本信息  
>String getDatabaseProductName()获取数据产品的名称

> int getDriverMajorVersion()获取JDBC驱动程序的主版本号

>int getDriverMinorVersion()获取JDBC驱动程序的此版本号
- 使用ResultSetMetaData获取ResultSet对象中的信息
>int getColumnCount()返回此ResultSet对象中的列数
>String getColumnName(int column)获取指定列的名称
>int getColumnTypeName(int column)获取指定列的SQL类型名称

11.
- 事务的概念
- mysql对事务的支持
- jdbc事务处理

