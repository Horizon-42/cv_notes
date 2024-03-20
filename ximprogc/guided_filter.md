# 导向滤波
当引导图是原图的时候，就成了一个边缘保持滤波器
$$q_i = a_kI_i+b_k, \forall i \in w_k$$
$$q_i = p_i - n_i$$
其中，$q_i$是导向滤波的输出,$p_i$是原图，而$n_i$是假设的噪点；
那么导向滤波就是求参数$a_k,b_k$,使$q_i, p_i$差距最小.
即使
$$E(a_k, b_k) = \sum_{i\in w_k}((a_kI_i+b_k-p_i)^2+\epsilon{a_k}^2)$$
