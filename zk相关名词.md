## 名词解释

可以发现这些概念的约束是递进的

### **semigroup**

**A semigroup is a magma where the binary operator must be associative.**

- In other words, a semigroup is a set with a binary operator that is closed and associative.

集合+二元操作符,满足结合律+封闭性

### monoid

**A monoid is a semigroup with an identity element.**

在semigroup 基础上加上了 **identity element. 特性**

### group

monoid plus below opration

- inverse

**Cyclic Group**

存在几何中的一个元素g,对g不断进行群运算得到的元素,可以生成整个群;

- elliptic curve over a finite field(eg. integer mod p) is Cyclic Group

### abelian group

满足交换律的group

### ring

A Ring is a set with two binary operators such that

- under the first binary operator, the set is a abelian group
- under the second binary operator, the set is a monoid
- the second binary operator distributes over the first
- example
    
    Prove:A ring with only {0} under addition and multiplication is a trivial ring
    

- 多项式是一个环:在加法下满足abelian group,乘法下满足monoid(没有逆运算)

### Field

A field is a set with two binary operators such that

- under the first binary operator, the set is an abelian group
- under the second binary operator, *excluding the zero element*, the set is an abelian group

- The set of all integers under addition and multiplication is not a field
    - 因为在乘法下面,整数的逆可能不再是整数(eg.5)
- The set of all rational numbers is a field

- **Integers modulo a prime number is a field under addition and multiplication**
    - in modular arithmetic, every element in **a finite field has a multiplicative inverse;**
    - 关键点来了!!! 后续可以经常看到很多mod操作,原因就是mod操作之后满足filed条件

- 有限域(finite field)
