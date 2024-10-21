I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
ChatGPT was asked to make the solutions nicely formatted for a markdown file without changing any of the actual content/ideas.

# Recurrent Recurrences

Give big $\Theta$ bounds for the following recurrence relations.

1. 
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

$$
T(n) = T\left(\frac{n}{13}\right) + 5
$$

$$
T(n) = T\left(\left(\frac{n}{13}\right)/13 + 5\right) + 5
$$

$$
T(n) = T\left(\frac{n}{169}\right) + 10
$$

$$
T(n) = T\left(\frac{n}{2197}\right) + 15
$$

$$
T(n) = T\left(\frac{n}{13^i}\right) + 5i \quad \text{for } i = \log(n)
$$

$$
T(n) = T(1) + 5\log(n) = 1 + 5\log(n)
$$

$$
1 + 5\log(n) \in \Theta(\log(n))
$$


2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

$$
T(n) = 13T\left(\frac{n}{13}\right) + 5
$$

$$
= 13\left(13T\left(\frac{n}{169}\right) + \frac{5}{13}\right) + 5
$$

$$
= 169T\left(\frac{n}{169}\right) + 10
$$

$$
= 13^{3}T\left(\frac{n}{13^{3}}\right) + 15
$$

$$
T(n) = 13^{i}T\left(\frac{n}{13^{i}}\right) + 5i \quad \text{for } i = \log(n)
$$

$$
= 13^{\log(n)}T\left(\frac{n}{13^{\log(n)}}\right) + 5\log(n)
$$

$$
= nT\left(\frac{n}{n}\right) + 5\log(n)
$$

$$
= nT(1) + 5\log(n)
$$

$$
= n + 5\log(n)
$$

$$
T(n) \in \Theta(n)
$$



3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$


$$
T(n) = 13T\left(\frac{n}{13}\right) + 2n
$$

$$
= 13\left(T\left(\frac{n}{169}\right) + \frac{2n}{13}\right) + 2n
$$

$$
= 169T\left(\frac{n}{169}\right) + 4n
$$

$$
= 13\left(169T\left(\frac{n}{13^{3}}\right) + \frac{4n}{13}\right) + 2n
$$

$$
= 13^{3}T\left(\frac{n}{13^{3}}\right) + 6n
$$

$$
= 13^{i}T\left(\frac{n}{13^{i}}\right) + 2in \quad \text{for } i = \log(n)
$$

$$
= 13^{\log(n)}T\left(\frac{n}{13^{\log(n)}}\right) + 2n\log(n)
$$

$$
= nT\left(\frac{n}{n}\right) + 2n\log(n)
$$

$$
= nT(1) + 2n\log(n)
$$

$$
= n + 2n\log(n)
$$

$$
T(n) \in \Theta(n\log(n))
$$

