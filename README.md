# cli-latex
stick a latex expression in terminal, get a png with that expression on your clipboard. easy as that.

written in python because that's what i know.

## dependencies
* [python](https://www.python.org/)
* [latex](https://www.latex-project.org/get/) and pdflatex
* [imagemagick](https://imagemagick.org/index.php)
* [cat](https://en.wikipedia.org/wiki/Cat_(Unix))
* [xclip](https://github.com/astrand/xclip)

## how it works
the comments in `generator.py` should be self-explanatory

## how to use
to use this, first copy the `generator.py` file into your working directory. now, do the following:

```
python generator.py "<latex>"
```

...where <latex> is whatever the equation is. don't include the dollar signs -- i already did that, as you can see for yourself in `generator.py`. 

there might be a short delay depending on how long/complicated the latex you've put in is, but after that you'll have the image copied into your clipboard.

## example
obviously i need an example; otherwise, nobody's gonna be interested. well, here it is:

```
python generator.py "\int_{-\infty}^\infty \frac{1}{\sqrt{2\pi}} e^{-\frac{x^2}{2}} \text{dx} = 1"
```

![output of the above](https://raw.githubusercontent.com/integralLeft/cli-latex/main/output.png)

## extra fun
if you want to be able to do this anywhere but don't feel like sticking the `generator.py` file in literally every single directory, you could add the generator file to your `$PATH` (but that is probably a pain or something) OR you could use the handy dandy bash script i wrote to (a) make it shorter to type (like who tf wants to type `python generator.py` every time) and (b) make it available everywhere!!!

all you need to do is edit your `~/.zshrc` (or `~/.bashrc` if you haven't ascended yet) file to alias stuff to it. should be ez.


