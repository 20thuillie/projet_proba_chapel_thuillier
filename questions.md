3) $f_{µ|Z_{obs}=z}(x) = \frac{f_{Z_{obs}|µ = x}(z) . f_µ(x)}{f_{Z_{obs}}(z)}$ donc 
$$
f_{µ|Z_{obs}=z}(x) \propto f_{Z_{obs}|µ = x}(z) . f_µ(x)
$$
à $z$ fixé. Comme cette fonction est d'intégrale 1 par rapport à $x$, il suffit de trouver une fonction qui soit proportionnelle à la même quantité à $z$ fixé et qui soit d'intégrale 1 pour en déduire l'égalité entre cette fonction et $f$.  
Evaluons pour celà 
$$
-2ln(f_{Z_{obs}|µ = x}(z) . f_µ(x))
$$
sachant qu'on pourra donc ne pas tenir compte des termes additifs ne dépendants que de $z$.  
On rappelle que
$$
f_{Z_{obs}|µ = x}(z) = \frac{1}{(2\pi)^{n/2}}\sqrt{det(C_{obs})}exp(-\frac{1}{2}(z-x)^tC_{obs}^{-1}(z-x))
$$
et que 
$$
f_µ(x)=\frac{1}{\sigma \sqrt{2\pi}}exp(-\frac{(x+5)^2}{8})
$$
Ainsi, on a 
$$
-2ln(f_{Z_{obs}|µ = x}(z) . f_µ(x)) = (z-x)^tC_{obs}^{-1}(z-x) +\frac{(x+5)^2}{4}
$$
En mettant cette expression sous forme canonique, puis en ne considérant plus le terme constant, on reconnait la densité d'un vecteur aléatoire gaussien. Le coefficient devant $x^2$ est alors identifiable à $\frac{1}{\hat \sigma^2}$ et le coefficient en $x$ est identifiable à $\frac{-2\hat µ}{\hat \sigma^2}$.  
Ici, il convient de rectifier l'abus de notation précédent: le vecteur qu'on a noté $x$ est en fait $1x$ où 1 est un vecteur est x est le scalaire. 
On obtient donc bien sans problème que 
$$
\hat \sigma^2  = (1^tC_{obs}1+\frac{1}{4})^{-1}
$$
et en remarquant que $C_{obs}$ est symétrique puisqu'il s'agit d'une matrice de covariance, on peut regrouper $z^tC_{obs}1$ et $1^t C_{obs}z$, ce qui nous donne bien:
$$
\hat µ = \hat \sigma ^2 (1^tC_{obs}z_{obs}-\frac{5}{4})
$$
La densité de probabilité correspondant à la loi normale de paramètre ($\hat µ$,$\hat \sigma ^2$) étant proportionnelle par construction à la fonction précédente, et étant d'intégrale 1, on peut bien conclure que 
$$
µ|Z_{obs}=z_{obs} \sim \mathcal{N}(\hat\mu,\,\hat\sigma^{2})
$$
  
4) On sait qu'on peut considérer $f_{|Z=z}$ comme une densité de probabilité. Appelons la $\tilde{f}$. Les formules du cours s'appliquent à $\tilde{f}$. On obtient alors l'égalité désirée.
5) Par application de la question précédente: on obtient:
$$
f_{Z_{UNK},µ|Z_{obs}=z_{obs}}(z_u,x) = f_{Z_{UNK}|µ=x,Z_{obs}=z_{obs}}(z_u).f_{µ|Z_{obs}=z_{obs}}(x)
$$
On rappelle que 
$$
f_{Z_{UNK}|µ=x,Z_{obs}=z_{obs}}(z_u) = \frac{1}{(2\pi)^{\frac{N+1-n}{2}}\sqrt{det(CS)}} exp(-\frac{1}{2}(z_{unk}-m_{Z_{UNK}|Z_{obs}=z_{obs},µ=x})^t(CS)^{-1}(z_{unk}-m_{Z_{UNK}|Z_{obs}=z_{obs},µ=x})
$$
où $CS = C_{obs}-C_{unk,obs}C_{obs}^{-1}C_{obs,unk}$ et $m_{Z_{UNK}|Z_{obs}=z_{obs},µ=x} = x.1 + C_{unk,obs}C_{obs}^{-1}(z_{obs}-x.1)$.