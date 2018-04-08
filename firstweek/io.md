1.java的io包中定义了多个流类型（类或抽象类）来实现输入或输出功能

2.从不同的角度对流进行分类：

- 按数据流的方向不同分为输入流和输出流
- 按处理数据单位不同分为字节流和字符流
- 按功能不同分为节点流和处理流 
>节点流：从一个特定的数据源读、取数据

>处理流：对已存在的流（节点流或处理流）连接或封装，通过对数据的处理为程序提供更强大的读写功能

3.J2SDK提供的位于java包内的所有流类型都继承自以下四种抽象流类型：



|       | 字节流 |字符流
|---|:---|:----:|
输入流| InputStream|Reader|
输出流| OutputStream|Writer|

4.一些方法

InputStream

- int read()    ++从输入流中读取单个字节，返回所读取的字节数据(字节数据可直接转换为int类型)++
- int read(byte[] b)     ++从输入流中最多读取b.length个字节的数据，并将其存储在字节数组b中，返回实际读取的字节数++
- int read(byte[] b,int off,int len) ++从off位置开始，最多读取len个字节的数据，并存储在数组b中，返回实际读取的字节数++

Reader

- int read ++（字符数据可直接转换为int类型）++
- int read(char []c)
- int read(char[] c,int off,int len)

OutputStream/Write

- void write(int c) ++将指定的字节/字符输出到输出流中++
- void write(byte[]/char[] buf)
- void write(byte[]/char[] buf,int off,int len)

Write可以用字符串来代替字符数组，即以String对象作为参数

- void write(String str)
- void write(String str,int off,int len)

5. 缓冲流                  
>BufferedReader 

>BufferedWriter

6. 转换流
>OuterputStreamWriter
>InputStreamReader
```
InputStreamReader isr = new InputStreamReader(System.in);
//输出输入的字符
BufferedReader br = new BufferedReader(isr);//可以输出一行           
```
7. 数据流
- DataInputstream
- DataOutputstream              
可以输入输出int/folat型数据
