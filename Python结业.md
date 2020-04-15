# python结业项目

## 需求

要求用户输入三次信息，第一次输入为用户名（任意字符），第二次为网址或任意字符，第三次则输入一个加密口令，也可以是任意字符，第四个是菜单，要求用户密码看起来貌似为某一类型的加密方式

选项1:Base64 选项2:hash 选项3:普通密码

普通密码格式限制首字符大写，含有英文和数字，以及字符，并且分布均无特性。



### 思路

首先将用户输入的信息进行拼接，这里不采取过滤的方式来进行过滤用户输入的内容。

```
#!/usr/bin/env python3
#-*- coding:utf-8 -*-
import hashlib
import base64
import random
import string
import crypt
import sys

def basecode () :
	#base = all.encode(encoding="utf-8")
	# 设定字符集编码并赋值给base
	#print ('我是1',base)

	# 使用base64进行加密
	encodestr = base64.b64encode(md5code.encode(encoding='utf-8'))
	print ("你的新密码是:",encodestr[0:longer].decode('ASCII'))

	# 使用base64进行解密
	#decodestr = base64.b64decode(encodestr)
	#print (decodestr.decode())

def password (longer) :
	# 使用字符串对象获得一个大写的首字母
	sum1 = ''
	random.seed(all)
	abc = random.randint(65,90)
	sum1 = chr(abc)

	# 使用字符串内的元素分别随机为某一段数字
	for i in all :
		random.seed(i)
		abc = random.randint(33,126)
		sum1 += chr(abc)

	print (f'你的普通密码是：{sum1[0:longer]}')

def finished():
	y = input ("生成成功，是否退出程序？ 输入y退出，否则程序将继续运行\n>")
	if y == 'y' or y =="Y" or y =="YES" or y == 'yes' :
		sys.exit()
	else :
		print('程序继续运行')
	
# 代码开始执行
if __name__ =='__main__' :
	flag = 1
	while flag == 1 :
		print ("欢迎使用密码生成器")

		print ("请输入用户名:")
		username = input(">")

		print ("请输入网址或其他字符串:")
		other = input(">")

		print ("请输入任意密码:")
		apwd = input(">")

		all = username+other+apwd

		# 密码预处理
		md5 = hashlib.md5()	
		# 测试一次加密后是否正确
		md5.update(all.encode(encoding='utf-8'))
		md5code = md5.hexdigest()

		print ('*' * 20)
		print ("请选择你需要的加密类型：")
		print ("1: BASE64 2:hash 3:普通密码")
		choose = input(">")
		while True :
			try :
				longer = int(input ("请输入你的密码长度：\n>"))
			except ValueError :
				print ('密码长度输入有误，请重新输入')
			else:
				break

		if choose == '1' :
			basecode()
			finished()

		elif choose == '2' :
			newhash = str(hash(md5code))
			print (newhash[0:longer])
			finished()

		elif choose == '3' :
			password(longer)
			finished()
		else :
			print ("输入不正确，请重新输入")

```

### 总结

误区，不可采用随机数算法进行计算密码。因为无法进行复现。但可以用于生产一次性密码。

密码杂凑法失败，密码头几乎固定，无法使用。

https://blog.gtwang.org/linux/generate-linux-shadow-encrypted-password/

