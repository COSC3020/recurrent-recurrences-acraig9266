# Recurrent Recurrences

Give big $\Theta$ bounds for the following recurrence relations.

1. 
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$
    
T(n) = T(n/13) + 5


T(n)     = T(T(n/13)/13 + 5) + 5


T(n)     = T(n/169) + 10


T(n)     = T(n/2197) + 15


T(n)     = T(n/13<sup>i</sup>) + 5i     for  i = log(n)


T(n)     = T(1) + 5log(n) = 1 + 5log(n)


1 + 5log(n) ∈ Θ(log(n))





2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

T(n) = 13T(n/13) + 5

= 13(13T(n/169) + 5/13) + 5

= 169T(n/169) + 10

= 13<sup>3</sup>T(n/13<sup>3</sup>) + 15

T(n) = 13<sup>i</sup>T(n/13<sup>i</sup>) + 5i  for  i = lg(n)

= 13<sup>lg(n)</sup>T(n/13<sup>lg(n)</sup>) + 5lg(n)

= nT(n/n) + 5lg(n)

= nT(1) + 5lg(n)

= n + 5lg(n)

T(n) ∈ $\Theta$(n)

3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$


T(n) = 13T(n/13) + 2n

= 13(T(n/169) + 2n/13) + 2n

= 169T(n/169) + 4n

= 13(169T(n/13<sup>3</sup>) + 4n/13) + 2n

= 13<sup>3</sup>T(n/13<sup>3</sup>) + 6n

= 13<sup>i</sup>T(n/13<sup>i</sup>) + 2in  for  i = lg(n)

= 13<sup>lg(n)</sup>T(n/13<sup>lg(n)</sup>) + 2nlg(n)

= nT(n/n) + 2nlg(n)

= nT(1) + 2nlg(n)

= n + 2lg(n)

T(n) ∈ $\Theta$(nlg(n))
