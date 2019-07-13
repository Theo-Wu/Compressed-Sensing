# Compressed-Sensing   
变换域编码：找到信号的稀疏或可压缩表示的一个基或者框架。   
稀疏指的是n长度的信号，表示为k(k<<n)的非零系数。   
压缩表示指的是信号可以被只有k个非零系数的信号很好的逼近。
稀疏近似：只保留该信号的最大系数的值和位置来高保真地表示。JPEG\MPEG\MP3都是利用稀疏性和可压缩性进行变换编码，稀疏近似是基础。

Candes\Romberg等人说一个具有稀疏表示或者可压缩表示的有限维度信号可由少量线性的、非自适应的测量重建。所需的观测量较少，比一般采样定理好得多(奈奎斯特--香农采样定理)至于如何测量的方法是关键。   

任何k个正弦曲线的正线性组合都由其在t=0处的值和在任何其他2k**个**时间点的值唯一确定。？？当k很小且可能的频率范围很大时，样本远少于采样定理。   

### 压缩感知与采样定理的不同   
1. 采样理论考虑无限长的连续信号。压缩感知关注有限维向量，是一种理论数学方法。
2. 采样是在特定的时间点采样，压缩感知是通过信号的内积或更一般地用检验函数来获得观测量。(现代采样理论的中心思想————用线性观测量来获得信号)   
3. 香农采样定理下的信号重建是用sinc插值得到的，是个线性过程。压缩感知是个非线性过程。(最近也有研究表明传统采样可以用非线性方法)


### 低维信号模型   
现在大多数信号种类，简单的线性模型难以捕捉到信号的大部分结构信息————尽管用向量表示信号是合理的，但大多数情况下不是所有向量都能有效表示信号。因此出现了许多低维信号模型量化高维信号模型的自由度，这些自由度比高维信号本身自由度小很多。
