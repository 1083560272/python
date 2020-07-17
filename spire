# -*- codeing = utf-8 -*-
#@Time : 2020/7/12 1:51 下午
#@Author : 韩奇
#@File : testBS4.py
#@Software : PyCharm

'''
BeautifulSoup4将负责的HTML文档转换成一个复杂的树形结构，每个节点都是python对象，所有对象可以归纳为4种：

-Tag
-NavigableString
-BeautifulSoup
-Comment
'''


from bs4 import BeautifulSoup

file = open("./baidutest.html",'rb')

html = file.read().decode('utf-8')
bs = BeautifulSoup(html,'html.parser')  #解析上面的文档



#print(bs.head)
#print(bs.title)
#print(bs.a)

#Tag 标签及其内容

#print(type(bs.head))


#NavigableString  打印标签里的内容(字符串)
#print(bs.title.string)
#print(bs.a.attrs)


#BeautifulSoup  表示整个文档

#print(bs)
#print(type(bs.a.string))


#Comment  是一个特殊的NavigableString输出内容不包含




#--------------------------------------------------

#文档的遍历
#print(bs.head.contents)
#print(bs.head.contents[1])

#文档的搜索
#(1)find_all
#字符串过滤：会查找与字符串完全匹配的内容
#t_list = bs.find_all('a')


#正则表达式搜索：使用search()方法来匹配内容
#import re
#t_list=bs.find_all(re.compile('a'))


#方法：传入一个函数（方法），根据函数的要求来搜索

#def name_is_exists(tag):
#    return tag.has_attr(name_is_exists)
#t_list = bs.find_all(name_is_exists)


#(2)kwargs 参数

#t_list = bs.find_all(id="head")

#t_list= bs.find_all(class_=True)


#(3)text参数
#import re
#t_list = bs.find_all(text=re.compile('\d'))  #应用正则表达式来查找包含特定文本的内容（标签里的字符串）
#for item in t_list:
#    print(item)


#（4）limit参数
#t_list = bs.find_all('a',limit = 3)
#for item in t_list:
#    print(item)



#css选择器

#print(bs.select('title'))  #通过标签来查找

#t_list = bs.select('#u1')    #通过id来查找

#t_list = bs.select('a[class = "bri"]')  #通过属性来查找

#t_list= bs.select("head > title")  #通过子标签来查找

#t_list = bs.select(".manv ～ .bri")  #通过兄弟节点进行查找

t_list = bs.select('img')

for item in t_list:
  print(item)




