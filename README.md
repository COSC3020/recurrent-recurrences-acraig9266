# Recurrent Recurrences

Give big $\Theta$ bounds for the following recurrence relations.

1.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$

T(n) = T(n/13) + 5


T(n)     = T(T(n/13)/13 + 5) + 5


T(n)     = T(n/169) + 10


T(n)     = T(n/2197) + 15


T(n)     = T(n/13<sup>i</sup>) + 5i     for i = log(n)


T(n)     = T(1) + 5log(n) = 1 + 5log(n)


1 + 5log(n) ∈ Θ(log(n))
