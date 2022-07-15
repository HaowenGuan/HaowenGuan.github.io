# Welcome to Theory Page
This page is a navigator to all my blogs and study notes. It's capable of viewing Markdown file and Mathematical expressions directly in-place of the static html website. 

This page can automatically generate a table-of-content and update it on the right whenever a new markdown file is rendered. Not only by that, the table-of-content incorporated a scrollspy function which provide an interactive viewing experience.

## Display LaTeX in HTML
Use `$...$` or `\(...\)` delimiters for in-line math, and `$$...$$` or `\[...\]` delimiters for displayed equations.

### Demo
When $a \ne 0$, there are two solutions to $ax^2 + bx + c = 0$ and they are
$$x = {-b \pm \sqrt{b^2-4ac} \over 2a}.$$

<p>
$$ \begin{array}{rcll}
y & = & x^{2}+bx+c\\
& = & x^{2}+2\times\dfrac{b}{2}x+c\\
& = & \underbrace{x^{2}+2\times\dfrac{b}{2}x+\left(\frac{b}{2}\right)^{2}}-
{\left(\dfrac{b}{2}\right)^{2}+c}\\
&  & \qquad\left(x+{\dfrac{b}{2}}\right)^{2}\\
& = & \left(x+\dfrac{b}{2}\right)^{2}-\left(\dfrac{b}{2}\right)^{2}+c
& \left|+\left({\dfrac{b}{2}}\right)^{2}-c\right.\\
y+\left(\dfrac{b}{2}\right)^{2}-c & = & \left(x+
\dfrac{b}{2}\right)^{2} & \left|\strut(\textrm{vertex form})\right.\\
y-y_{S} & = & (x-x_{S})^{2}\\
S(x_{S};y_{S}) & \,\textrm{or}\,
& S\left(-\dfrac{b}{2};\,\left(\dfrac{b}{2}\right)^{2}-c\right)
\end{array} $$
</p>

## ACKNOWLEDGMENTS
This page renders Markdown file using [GitHub Markdown API](https://docs.github.com/en/rest/markdown). According to GitHub document, every unauthenticated clients is limited to 60 requests per hour.

The implementation of displaying math expressions is power by [MathJax](https://www.mathjax.org) library.






















