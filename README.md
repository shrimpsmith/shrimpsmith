- 👋 Hi, I’m @shrimpsmith
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
shrimpsmith/shrimpsmith is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
## R语言入门与数据分析
# 读入文件（二）
1.读取网络文件 ①http/ftp②局域网内file开头的完整文件的地址
  如果是读取html中嵌入的表格，就不属于读取文本文件
2.读取非文本文件
  读取html中的表格 使用xml包
  readXMLTable函数可以用来读取网页中的数(一般情况下比较难以读取，因为R只能处理规则的格式，网页上呈现出来的格式仅用于读者阅读，格式并不固定）
  which = 3 只读取网页中第三个表格的数据
3.foreign package
  不仅可以读取统计软件的数据，同时可以生成对应格式的数据
4.读取剪切板上的数据
x <- read.table('clipboard', header = T, sep =',')
x <- read.table('clipboard', header = T, sep ='\t')
read.clipboard() 
readLines("文件名",n=读入的最大函数) 读取文件中各行，并以字符串形式返回结果
scan('文件名', what = list(numeric(0))) 重复执行指定的模式
设置为0一直读取到行尾 设置为2 读取到第二行

## 写入文件
