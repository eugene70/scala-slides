```scala
def sum(f: Int => Int)(a: Int, b: Int) = (a to b map f).sum
sum(x => x * x)(1, 10)
sum(_ * 2)(1, 10)
def f(a: Int, b: Int): Int = a * b
def g(a: Int)(b: Int): Int = a * b
f(2, 3)
g(2)(3)
sum(g(2))(1, 10)

val pair = ("ans", 42)
val (label, value) = pair
pair._1
pair._2
val List(a, b, c) = List(1, 2, 3)
val Array(a, b, c) = "1 2 3" split ' '

1 to 10
1 until 10
1 to 10 by 3
6 to 1 by -2
1.to(10)
Seq(1, 1, 2, 2, 3, 3)
Set(1, 1, 2, 2, 3, 3)
Seq(1, 1, 2, 2).toSet
IndexedSeq(1, 2, 3)
IndexedSeq(1, 2, 3) :+ 4
0 +: IndexedSeq(1, 2, 3)
List(1, 2, 3)
1::(2::(3::Nil))
1::2::3::Nil
Nil.::(3).::(2).::(1)

val (xs, ys) = (List(1, 1, 2, 2, 3, 3), IndexedSeq(1, 2, 3))
xs.head
xs.tail
ys.last
ys.init
xs take 4
xs drop 4
ys(1)
xs ++ ys
xs.reverse
ys updated(1, 10)
ys
xs indexOf 3
xs contains 3
xs contains 4
xs zip ys
ys zip xs
xs.sum
xs.product
xs.max
xs.min

xs filter (x => x%2 == 0)
xs filterNot (x => x%2 == 0)
xs filter (_%2 == 0)
xs partition (_%2 == 0)
xs takeWhile (_%3 > 0)
xs dropWhile (_%3 > 0)
xs span (_%3 > 0)
xs map (x => x * 2)
xs map square
xs groupBy (_ % 2)

xs.reduceLeft((acc, x) => acc + x)
xs.foldLeft(10)((acc, x) => acc + x)
xs.foldLeft(10)(_ + _)
(10 /: xs)(_ + _)
```
