# homewrok_03

## let your name move!
### show the gif graph

![movename](https://github.com/RicardoZiTseng/computationalphysics_N2014301020006/blob/master/GIF.gif)

### show the code
```
import os,time
print("####         #      ####")
print("#    #       #     #    #")
print("#     #      #     #")
print("#    #       #     #")
print("####         #     #")
print("#   #        #     #")
print("#    #       #     #    #")
print("#     #      #      ####")
time.sleep(0.5)
i=os.system('cls')
print("	####         #      ####")
print("	#    #       #     #    #")
print("	#     #      #     #")
print("	#    #       #     #")
print("	####         #     #")
print("	#   #        #     #")
print("	#    #       #     #    #")
print("	#     #      #      ####")
time.sleep(0.5)
i=os.system('cls')
print("		####         #      ####")
print("		#    #       #     #    #")
print("		#     #      #     #")
print("		#    #       #     #")
print("		####         #     #")
print("		#   #        #     #")
print("		#    #       #     #    #")
print("		#     #      #      ####")
time.sleep(0.5)
i=os.system('cls')
print("			####         #      ####")
print("			#    #       #     #    #")
print("			#     #      #     #")
print("			#    #       #     #")
print("			####         #     #")
print("			#   #        #     #")
print("			#    #       #     #    #")
print("			#     #      #      ####")
time.sleep(0.5)
i=os.system('cls')
print("				####         #      ####")
print("				#    #       #     #    #")
print("				#     #      #     #")
print("				#    #       #     #")
print("				####         #     #")
print("				#   #        #     #")
print("				#    #       #     #    #")
print("				#     #      #      ####")
time.sleep(0.5)
i=os.system('cls')
print("					####         #      ####")
print("					#    #       #     #    #")
print("					#     #      #     #")
print("					#    #       #     #")
print("					####         #     #")
print("					#   #        #     #")
print("					#    #       #     #    #")
print("					#     #      #      ####")
time.sleep(0.5)
i=os.system('cls')
print("						####         #      ####")
print("						#    #       #     #    #")
print("						#     #      #     #")
print("						#    #       #     #")
print("						####         #     #")
print("						#   #        #     #")
print("						#    #       #     #    #")
print("						#     #      #      ####")
time.sleep(0.5)
i=os.system('cls')
print("							####         #      ####")
print("							#    #       #     #    #")
print("							#     #      #     #")
print("							#    #       #     #")
print("							####         #     #")
print("							#   #        #     #")
print("							#    #       #     #    #")
print("							#     #      #      ####")
time.sleep(0.5)
i=os.system('cls')
print("								####         #      ####")
print("								#    #       #     #    #")
print("								#     #      #     #")
print("								#    #       #     #")
print("								####         #     #")
print("								#   #        #     #")
print("								#    #       #     #    #")
print("								#     #      #      ####")
time.sleep(0.5)
i=os.system('cls')
print("									####         #      ####")
print("									#    #       #     #    #")
print("									#     #      #     #")
print("									#    #       #     #")
print("									####         #     #")
print("									#   #        #     #")
print("									#    #       #     #    #")
print("									#     #      #      ####")

```

## let your graph turn around
### show the gif graph
![movegraph](https://github.com/RicardoZiTseng/computationalphysics_N2014301020006/blob/master/2.gif)

### show the code
```
import os
def graph(x,y):
	a="#"
	l=list(a)
	for i in range(79):
		l.append("#")
	for j in range(39):
		l[x]=" "
		l[y]=" "
		a="".join(l)
		print(a)
		l[x]="#"
		l[y]="#"
		x=x-1
		y=y+1
	for k in range(40):
		l[39]=" "
		l[40]=" "
		a="".join(l)
		print(a)
x=0
y=0
for i in range(80):
	x=x+i
	y=y+i
	graph(x*2,y)
	os.system("cls")
	graph(y*2,x)
graph(x,y)
```
本来想避免用数像素点的方法来制造旋转效果的，想自己设计算法来制造旋转的效果，但水平有限，想不出来，只能做一个神经病般的动画效果了。
感谢室友和我一起讨论代码！
@卢江玮
@彭辰铭
@杨照军
