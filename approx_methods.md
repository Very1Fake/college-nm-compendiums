# Приближённые методы решения уравнений

## Метод половинного деления (метод проб)

```math
\text{Решить уравнение }f(x)=0
```

1. Отделение корней

2. Уточнение корней т.е. доведение их до заданной точности

### Алгоритм

Пусть $`\xi\in[a;b]`$ - единичный корень

1. В качестве первого приближения $`\Rightarrow\xi_1=\frac{a+b}2`$

2. Вычисляем $`f(a),f(\xi_1),f(b)\Rightarrow`$ т.е. рассматриваем $`[a;\xi_1], [\xi_1;b]`$. Тот из промежутков на концах которого разные знаки и содержит корень.
```math
\text{Пусть}\quad f(\xi_1)<0,\quad f(b)>0\quad\\\Rightarrow\xi\in[\xi_1;b]
```

3. В качестве второго приближения $`\Rightarrow\xi_2=\frac{\xi_1+b}2`$

4. Вычисляем $`f(\xi_1),f(\xi_2),f(b)\Rightarrow`$ т.е. рассматриваем $`[\xi_1;\xi_2],[\xi_2;b]`$
```math
\text{Пусть}\quad f(\xi_1)<0,\quad f(\xi_2)>0\quad\\\Rightarrow\xi\in[\xi_1;\xi_2]
```

5. В качестве третьего приближения $`\Rightarrow\xi_3=\frac{\xi_1+\xi_2}2`$

```math
\text{...}\\\quad\\
|\xi_{n+1}-\xi_n|<\epsilon\quad|f(\xi_n)|<\epsilon
```

### Пример

```math
\text{Решить уравнение}\quad x^3+2x-7=0, \quad\epsilon=0.1\\
\xi\in(1;2)\quad f(1)<0\quad f(2)> 0\\
\begin{align}
\xi_1=\frac{a+b}2&=1.5\Rightarrow f(1.5)=-0.625<0\Rightarrow[1.5;2]\\
\xi_2=\frac{\xi_1+b}2=\frac{1.5+2}2&=1.75\Rightarrow f(1.5)=1.1313>0\Rightarrow[1.5;1.7]\\
\xi_3=\frac{\xi_1+\xi_2}2=\frac{1.5+1.7}2&=1.6\Rightarrow f(1.5)=0.296>0\Rightarrow[1.5;1.6]\\
\xi_4=\frac{\xi_1+\xi_3}2=\frac{1.5+1.6}2&=1.55\Rightarrow f(1.5)=-0.176<0\Rightarrow[1.55;1.6]\\
\xi_5=\frac{\xi_3+\xi_4}2=\frac{1.6+1.55}2&=1.57
\end{align}
```
