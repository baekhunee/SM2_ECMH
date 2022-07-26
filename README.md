# 实验名称
Elliptic curve MultiSet Hash

# 实验完成人
权周雨 

学号：202000460021 

git账户名称：baekhunee

# ECMH
  ECMH整体思路是：先把集合里的元素映射成椭圆曲线上的点，然后利用椭圆曲线上的加法求解哈希值。
  
  为达到相同的安全性，ECMH算法需要的密钥长度远远小于哈希求和算法，因而ECMH相较哈希求和算法更为安全。

# 部分代码说明
## def epoint_mod(a, n)
定义椭圆曲线上的模运算即返回值等于a mod n

## def epoint_modmult(a, b, n)
定义椭圆曲线上的模乘运算，返回值等于a*b^(-1) mod n

## def epoint_add(P, Q, a, p)
定义椭圆曲线上的加法运算，返回值等于P + Q

## def epoint_mult(k, P, a, p)
定义椭圆曲线上的点乘运算，返回值等于k * P

## def keygen(a, p, n, G)
生成SM2算法的公私钥对

## def isQR(n,p)
使用欧拉准则判断n是否是模p的二次剩余

## def QR(n,p)
求解二次剩余

## def _hash(S)
定义集合上的哈希函数

# 运行截图
![image](https://user-images.githubusercontent.com/105578152/180953575-b951b547-2e38-4eb8-a753-19e482e23690.png)
