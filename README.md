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

4. SCRATCH THE ABOVE -- Upgraded to Ubuntu 12.04 LTS.  Will determine later if this solved the latex problems.  Following the directions on this page, with modifications: http://askubuntu.com/questions/163682/how-do-i-install-the-latest-tex-live-2012#comment284348_163683

5.  sudo add-apt-repository ppa:texlive-backports/ppa (add-atp- instead of apt-add); sudo apt-get install texlive (I may have better done sudo apt-get update and then sudo apt-get upgrade)  This gets it too Tex Live 2012/Debian version. Then redid step 2 above.

6. sudo texlive-latex-extra as per comment by uvts_cvs on http://tex.stackexchange.com/questions/73116/fresh-install-texlive-2012-ubuntu-12-04-tlmgr-nowhere-to-be-found

7. This may be the cause of all my problems: need to run vc from latex using:
\immediate\write18{sh ./vc}
\input{vc}

8. trying sudo apt-get install texlive-fonts-extra ... didn't seem to help

9. Minion Pro must cost money

======
A new day, need to fix these instructions. Anyway, got rid of "blueviolet" error by switching to "xcolor" package from "color" on line 82

Sudo apt-get install gawk

Look into http://ctan.org/pkg/gitinfo

Ran the command on bash: git --no-pager log -1 HEAD --pretty=format:"Hash: %H%nAbr. Hash: %h%nParent Hashes: %P%nAbr. Parent Hashes: %p%nAuthor Name: %an%nAuthor Email: %ae%nAuthor Date: %ai%nCommitter Name: %cn%nCommitter Email: %ce%nCommitter Date: %ci%n" |gawk -v script=log -v full=0 -f vc-git.awk > vc.tex

Okee dokee now this works.  Will try to fix these notes tomorrow.


 
