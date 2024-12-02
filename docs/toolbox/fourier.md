## Transformation de Fourier

### Du discret au continu

Nous avons établi dans le chapitre précédent que tout signal périodique physique peut s'écrire en notation complexe :

\[
f_T(t) = \sum_{n=-\infty}^\infty \underline{c_n}\, \mathrm{e}^{i n\, 2\pi\nu\,t}
\]

avec \(\nu = \frac{1}{T}\), où \(\underline{c_n}\) est un ensemble **discret** de coefficients complexes donnés par :

\[
\underline{c_n} = \frac{1}{T} \int_{-T/2}^{T/2} f(t)\, \mathrm{e}^{-i n\, 2\pi\nu\, t}\, \mathrm{d}t, \quad \text{avec } n \in \mathbb{Z}
\]

Considérons dorénavant un signal \(f(t)\) **non périodique**. On peut toujours considérer que le signal représente un unique motif d'un signal périodique dont la période tendrait vers l'infini. En d'autres termes, on peut considérer que le signal est de fréquence \(\nu \to 0\) et que les harmoniques balayent tout l'espace des réels ; le spectre discret devenant alors continu. Voyons comment cela se traduit mathématiquement.

D'après les relations précédentes, un signal périodique peut s'écrire :

\[
f_T(t) = \sum_{n=-\infty}^\infty \left[ \nu \int_{-T/2}^{T/2} f(t')\, \mathrm{e}^{-i n\, 2\pi\nu\,t'}\, \mathrm{d}t' \right] \mathrm{e}^{i n\, 2\pi\nu\,t}
\]

Faisons tendre \(T \to \infty\), c'est-à-dire \(\nu \to 0\) :

\[
f(t) = \lim_{\nu \to 0} \sum_{n=-\infty}^\infty \left[ \mathrm{e}^{i n\, 2\pi\nu\,t} \int_{-\infty}^\infty f(t')\, \mathrm{e}^{-i n\, 2\pi\nu\, t'}\, \mathrm{d}t' \right] \nu
\]

### Intégrale de Riemann

Rappelons qu'une intégrale peut être vue comme une somme de rectangles sous la courbe avec un espacement tendant vers 0. Mathématiquement, on a l'identité :

\[
\int_{-\infty}^\infty g(\nu)\, \mathrm{d}\nu = \lim_{\nu \to 0} \sum_{n=-\infty}^\infty g(n\nu)\, \nu
\]

On reconnaît ici une intégrale au sens de Riemann. Ainsi, un signal non périodique peut formellement s'écrire :

\[
f(t) = \int_{-\infty}^\infty \mathrm{e}^{i 2\pi\nu\, t} \left[ \int_{-\infty}^\infty f(t')\, \mathrm{e}^{-i 2\pi\nu\,t'}\, \mathrm{d}t' \right] \mathrm{d}\nu
\]

Le terme entre crochets est appelé **transformée de Fourier**.

### Intégrale de Fourier

Tout signal physique peut se décomposer en une intégrale de Fourier, de la forme :

\[
f(t) = \int_{-\infty}^\infty \widehat{f}(\nu)\, \mathrm{e}^{i 2\pi \nu\, t}\, \mathrm{d}\nu \tag{1.a}
\]

où \(\widehat{f}(\nu)\) désigne la transformée de Fourier du signal. \(\widehat{f}(\nu)\) est une fonction continue à valeurs complexes, définie par :

\[
\widehat{f}(\nu) = \int_{-\infty}^\infty f(t)\, \mathrm{e}^{-i 2\pi \nu\,t}\, \mathrm{d}t \tag{1.b}
\]

Ce théorème concerne les signaux de carré sommable pour lesquels \(\int_\mathbb{R}\|f(t)\|^2\, \mathrm{d}t\) est finie, c'est-à-dire des signaux qui transportent une énergie finie comme c'est le cas en physique.

---