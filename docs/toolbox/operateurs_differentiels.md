# OPÉRATEURS DIFFÉRENTIELS

Fondamentalement, ce sont des opérateurs de dérivation, dans ce chapitre nous allons établir leurs expressions dans divers systèmes de coordonnées.

## L'opérateur gradient

### Définition

L'opérateur gradient est un *opérateur différentiel* qui s'applique à un **champ scalaire** (fonction scalaire dépendant de l'espace et du temps) et le transforme en un **champ vectoriel** (vecteur dépendant de l'espace et du temps). Il se lit « gradient » ou « nabla » et se note :

\[
\overrightarrow{\text{grad}}f(\text{M},t)\quad\text{ou}\quad\overrightarrow{\nabla}f(\text{M},t)
\]

Dans le système de coordonnées cartésiennes, le gradient s'exprime ainsi :

!!! note ""
	\[
	\overrightarrow{\text{grad}}f(x,y,z,t) = 
	\dfrac{\partial f(x,y,z,t)}{\partial x}\overrightarrow{u_{x}} + 
	\dfrac{\partial f(x,y,z,t)}{\partial y}\overrightarrow{u_{y}} + 
	\dfrac{\partial f(x,y,z,t)}{\partial z}\overrightarrow{u_{z}}
	\]

Les différentes expressions du gradient dans les systèmes de coordonnées utilisés couramment en physique sont présentées dans le tableau ci-dessous :


| **Système**     | \(f(\text{M},t)\)         | **Expression de** \(\text{grad}f\)                                                                                                                                 |
|------------------|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cartésien        | \(f(x,y,z,t)\)           | \(\dfrac{\partial f}{\partial x}\overrightarrow{u_{x}} + \dfrac{\partial f}{\partial y}\overrightarrow{u_{y}} + \dfrac{\partial f}{\partial z}\overrightarrow{u_{z}}\) |
| Cylindriques     | \(f(r,\theta,z,t)\)      | \(\dfrac{\partial f}{\partial r}\overrightarrow{u_{r}} + \dfrac{\partial f}{r\partial \theta}\overrightarrow{u_{\theta}} + \dfrac{\partial f}{\partial z}\overrightarrow{u_{z}}\) |
| Sphériques       | \(f(r,\theta,\varphi,t)\)| \(\dfrac{\partial f}{\partial r}\overrightarrow{u_{r}} + \dfrac{\partial f}{r\partial \theta}\overrightarrow{u_{\theta}} + \dfrac{\partial f}{r\sin\theta\partial \varphi}\overrightarrow{u_{\varphi}}\) |



### Propriétés

L'opérateur gradient est un opérateur linéaire et vérifie donc :

\[
\overrightarrow{\nabla}(\alpha f + \beta g) = \alpha \overrightarrow{\nabla}f + \beta \overrightarrow{\nabla}g
\quad\text{avec}\quad (\alpha, \beta) \in \mathbb{R}^2
\]

Le gradient d'un produit de champs scalaires vaut :

\[
\overrightarrow{\nabla}(f \cdot g) = f \overrightarrow{\nabla}g + g \overrightarrow{\nabla}f
\]

où \(f\) et \(g\) sont deux fonctions de l'espace et du temps.

**Lien avec la différentielle** -- On peut définir le gradient à partir de sa relation avec la différentielle. Soit \(M\) un point de l'espace et \(M'\) un point infiniment voisin, la différentielle \(\text{d}f\) représente la variation du champ scalaire \(f\) lorsque l'on se déplace de \(M\) à \(M'\) à \(t\) fixé :

\[
\text{d}f \stackrel{\text{def}}{=} f(\text{M}',t) - f(\text{M},t) = \overrightarrow{\nabla}f(\text{M},t) \cdot \overrightarrow{\text{d}\ell}
\quad\text{avec}\quad
\overrightarrow{\text{d}\ell} = \overrightarrow{\text{MM'}}
\]

En conséquence :

- Le vecteur \(\overrightarrow{\nabla}f(\text{M},t)\) est perpendiculaire à la surface de niveau de \(f\) passant par \(M\) à l'instant \(t\).
- Le vecteur gradient est orienté vers les valeurs croissantes de \(f\) et sa norme mesure le taux de variation spatiale dans la direction de plus grande pente :

\[
\left\| \overrightarrow{\nabla}f \right\| = \dfrac{\text{d}f}{\text{d}\ell}
\]

---
