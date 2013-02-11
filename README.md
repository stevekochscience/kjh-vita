kjh-vita (forked on github from Kieran Healy http://www.kieranhealy.org/)
Steve Koch stevekochscience@gmail.com
License: as open as Kieran Healy intended
========

A simple LaTeX template that Kieran used for his Vita that he decide to share.

I'm new to latex (and fairly new to unix, so here are some newbie instructions for getting it to work):

1. Start out with some kind of latex.  I'm using Ubuntu 11.10 and I think I previously installed some latex packages.  Unfortunately, I can't remember what I started with.  Not too much beyond what comes with Ubuntu 11.10, though.

2. Get the xelatex package
    sudo apt-get install texlive-xetex

3. Get the version control files from CTAN: http://www.ctan.org/tex-archive/support/vc . Follow instructions in the PDF manual.  E.g., if using git, copy the two files, vc an vc-git.awk to your project directory.

4. SCRATCH THE ABOVE -- Upgraded to Ubuntu 12.04 LTS.  Will determine later if this solved the latex problems
