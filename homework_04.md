# exercise_04
***
## 简述题目
>在一个系统中，有两种放射性原子A和B，原子A会衰变成原子B，而原子B也会衰变成原子A。严格上来说，这并不是一个“衰变”循环。一个更加恰当的解释应当是这个系统在保持能量不变的状态下可以在原子A和B中相互转化。而描述这个过程的速率方程是这样的：
<img src="http://latex.codecogs.com/gif.latex?\frac{dN_{A}}{dt}=\frac{N_{B}}{t_{dcy}}-\frac{N_{A}}{t_{dcy}}" alt="" title="" />
![(0.2)](http://latex.codecogs.com/png.latex?\frac{dN_{B}}{dt}=\frac{N_{A}}{t_{dcy}}-\frac{N_{B}}{t_{dcy}})
利用这个方程解决这个原子数分别为NA和NB的系统，同时：
![衰变周期](http://latex.codecogs.com/png.latex?t_{dcy}=1s)

## 方程的解析
>假设某类原子的衰变方程为：
![(1.1)](http://latex.codecogs.com/png.latex?\frac{dN}{dt}=-\frac{N}{t_{dcy}})
然后对一段时间内的原子数量做泰勒展开：
![(1.2)](http://latex.codecogs.com/png.latex?N(\Delta t)=N(0)+\frac{dN}{dt}\cdot\Delta t+\frac{1}{2} \cdot \frac{d^2 N}{dt^2}+...)
只取前两项，则有：
![(1.3)](http://latex.codecogs.com/png.latex?N(\Delta t)\approx N(0)+\frac{dN}{dt}\cdot\Delta t .)
对(1.1)方程做近似：
![(1.4)](http://latex.codecogs.com/png.latex?\frac{dN}{dt}=\lim(\Delta t \to 0)\frac{N(t+\Delta t)-N(t)}{t}\approx\frac{N(t+\Delta t)-N(t)}{\Delta t})
所以有：
![(1.5)](http://latex.codecogs.com/png.latex?N(t+\Delta t)\approx N(t)+\frac{dN}{dt}\cdot\Delta t.)
由(1.1),有：
![(1.6)](http://latex.codecogs.com/png.latex?N(t+\Delta t)\approx N(t)-\frac{N(t)}{t_{dcy}}\cdot\Delta t)

## 题目方程解析
>令：
![(1.7)](http://latex.codecogs.com/png.latex?\Delta N=N_{B}-N_{A})
由(1.3)知：
![(1.8.1)](http://latex.codecogs.com/png.latex?N_{A}(\Delta t)\approx N_{A}(0)+\frac{dN_{A}}{dt}\cdot\Delta t)
![(1.8.2)](http://latex.codecogs.com/png.latex?N_{B}(\Delta t)\approx N_{B}(0)+\frac{dN_{B}}{dt}\cdot\Delta t)
由(1.5)知：
![(1.9.1)](http://latex.codecogs.com/png.latex?\begin{align*}N_{A}(t+\Delta t)\approx N_{A}(t)+\frac{dN_{A}}{dt}\cdot \Delta t \\&=N_{A}(t)+\frac{1}{t_{dcy}}\cdot(N_{B}-N_{A})\cdot\Delta t\end{align*})
![(1.9.2)](http://latex.codecogs.com/png.latex?\begin{align*}N_{B}(t+\Delta t)\approx N_{B}(t)+\frac{dN_{B}}{dt}\cdot \Delta t \\&=N_{B}(t)+\frac{1}{t_{dcy}}\cdot(N_{A}-N_{B})\cdot\Delta t\end{align*})
再由(1.7),得：
![(1.10.1)](http://latex.codecogs.com/png.latex?N_{A}(t+\Delta t)\approx N_{A}(t)+\frac{1}{t_{dcy}}\cdot\Delta N\cdot\Delta t)
![(1.10.2)](http://latex.codecogs.com/png.latex?N_{B}(t+\Delta t)\approx N_{A}(t)-\frac{1}{t_{dcy}}\cdot\Delta N\cdot\Delta t)

## 代码模拟
* **我对c语言比较熟悉，所以先用c语言做模拟，之后再改成python**
```
#include <stdio.h>
#include <math.h>
#define MAX 100
int Delta_N;        //Delta_N=N_B-N_A
double dt;
double t_decay;
double t[MAX];
double N_A[MAX],N_B[MAX];
double t_max;
//初始化函数
double initialize()
{
	printf("initial number of A-atom ->\n");
	scanf("%lf",&Number_A);
	printf("initila number of B-atom ->\n");
	scanf("%lf",&Number_B);
	printf("the time of decaying ->");
	scanf("%lf",&time_decay);
	printf("time step ->");
	scanf("%lf",&dt);
	t[0]=0.0;
	return;
}
```

* **python语言部分**
