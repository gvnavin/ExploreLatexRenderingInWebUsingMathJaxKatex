# ExploreLatexRenderingInWebUsingMathJaxKatex
This is created to contains examples, samples to test rendering of complicated mathematical expression using different rendering libraries like MathJax and KaTex

Latex to HTML Rendering

Found 2 MathJax and KaTeX JS lib to render Latex. These JS lib will converts the latex to MathML 


MathJax

It is a popular JS lib used widely to render mathematical equations 
https://www.mathjax.org/

It runs asynchronously, so you can see equations popping into existence as it works down the page [3]
It can be a bit slow. This need for on-the-fly processing comes at a cost. Every time a page loads in someone’s browser, everything has to be typeset from scratch. Often, this is not a problem. By the time the page has loaded and your eyes has found the opening paragraph, MathJax is done. But sometimes the page is very math-heavy and MathJax has to work hard for so long that it becomes annoying. [5]

The HTML-CSS output is highly browser and client dependent. From basic things like installed fonts to tricky things like hacks around browser and OS bugs, MathJax does a lot of work to guarantee identical display across all browsers. So in a very real sense, you cannot store the HTML-CSS output – as soon as it gets somewhat complex, it will not render well across browsers.   ―Peter Krautzberger, MathJax manager [5]

Both KaTeX and MathJax's biggest slowdown is the font loading [4]

MathJax has promised "significant speed improvements" in their next version [2]

There's a rough "time to process page" at the top. - http://www.intmath.com/cg5/katex-mathjax-comparison.php

MathJax handles more complicated quations [2]
MathJax successfully rendered the Chemical equation during experimentation [11]

While with Mathjax there seem (almost) no Latex features missing [6]

http://docs.mathjax.org/en/latest/tex.html#supported-latex-commands

Pre-rendering not supported. Refer #5

Best Practices are documented in this link - https://github.com/mathjax/MathJax-docs/wiki/Guide:-MathJax-in-Android-apps

Using MathJax in Chrome, "=" and "−" bolder [2]

A JavaScript display engine for mathematics that works in all browsers. [9]


There are many tools to create a Latex code for equations and formulae.
https://en.wikipedia.org/wiki/Formula_editor

I tried below 2 tools to create some equations to experience the process of creating the equations and formulae. 
The below metioned tools provides relatively better experience in creating the formulae and equations
http://www.imatheq.com/imatheq/com/imatheq/math-equation-editor-latex-mathml.html
http://calcinator.com/mathsolver.html


Katex
Khan Academy has released a new library to typeset mathematical notation on webpages, called KaTeX

https://khan.github.io/KaTeX/

KaTeX renders its math synchronously and doesn’t need to reflow the page [1]
KaTeX produces math much faster than MathJax [2]

The KaTeX library takes LaTeX as input and produces HTML as output. When such output is then put on a web page together with the KaTeX CSS file, the math is rendered by the browser using just the HTML and CSS (the CSS points to a number of special-purpose web fonts). [5]

Both KaTeX and MathJax's biggest slowdown is the font loading [4]
However, since KaTeX's CSS can be included manually (instead of letting MathJax put it in the DOM after load) it should load a little faster.


There's a rough "time to process page" at the top. - http://www.intmath.com/cg5/katex-mathjax-comparison.php

KaTeX doesn't handle several of the equations yet. [2]
KaTeX got exception when tried to render Chemical equation during the experimentation [12] [13]
Khan Academy is using KaTeX as a first port of call to render maths, and using MathJax as a fallback for things it can’t render [3]
KaTeX can’t render a number of equations such as \overrightarrow{AB} or aligned equations [6]

https://github.com/Khan/KaTeX/wiki/Function-Support-in-KaTeX

KaTeX produces the same output regardless of browser or environment, so you can pre-render expressions using Node.js and send them as plain HTML [1]

Khan Academy uses KaTeX, which you can try on an Android phone. There's no special support for Android in particular - https://github.com/Khan/KaTeX/issues/194

Using KaTeX in Chrome, "=" and "−" are thin [2]

Katex don't support IE 7 and earlier [4]
It claims to "supports all major browsers, including Chrome, Safari, Firefox, Opera, and IE 8 - IE 11" [2]


References
1. https://khan.github.io/KaTeX/

2. http://www.intmath.com/blog/mathematics/katex-a-new-way-to-display-math-on-the-web-9445

3. http://aperiodical.com/2014/09/katex-the-fastest-math-typesetting-library-for-the-web/

4. https://news.ycombinator.com/item?id=8320439

5. http://blog.janmr.com/2015/01/mathjax-katex-and-a-lot-of-math.html

6. https://www.bersling.com/2016/05/10/displaying-math-on-the-web/

7. http://meta.mathoverflow.net/questions/1908/katex-vs-mathjax

8. The below equation got failed in KaTex. But MathJax rendered it successfully
{O}_{4}+\downarrow 2H\overset{{H}_{2}S{O}_{4}+2{S}_{4}}\rightarrow{H}_{2}+S{O}_{4}\uparrow \xrightarrow[{\Delta }]{{H}_{2}}HCl+H2\phantom{\rule{0ex}{0ex}}

9. https://www.mathjax.org/

10. There's a rough "time to process page" at the top.
http://www.intmath.com/cg5/katex-mathjax-comparison.php

11. https://github.com/gvnavin/ExploreLaTeX/blob/master/math_jax_explore/math_jax.html

12. https://github.com/gvnavin/ExploreLaTeX/blob/master/katex_explore/katex.html

13. Created an issue with Katex for rendering error - https://github.com/Khan/KaTeX/issues/669

14. https://github.com/kexanie/MathView

15. Math ML works in firefox but not working in chrome.
http://stackoverflow.com/questions/29682207/unable-to-render-mathml-content-in-google-chrome
The link has simple Math ML which renders well in Firefox but not in chrome
https://github.com/gvnavin/ExploreLaTeX/blob/master/MathML_explore/math_mathml.html

16. The below link provides some guide in using MathJax in android apps
https://github.com/mathjax/MathJax-docs/wiki/Guide:-MathJax-in-Android-apps

17. Explored Math Jax rendering in WebView in Android. Android Sample app code is available from the below link
https://github.com/gvnavin/ExploreLatexRenderingInAndroidWebViewUsingMathJax

Screenshot:
https://github.com/gvnavin/ExploreLatexRenderingInAndroidWebViewUsingMathJax/commit/9e21c4bc506b862bdde3ad71e56c9ec3924803e2

Android Rendering Sample Code:
https://github.com/gvnavin/ExploreLatexRenderingInAndroidWebViewUsingMathJax/blob/master/app/src/main/java/com/explore/latex/rendering/webview/MainActivity.java
