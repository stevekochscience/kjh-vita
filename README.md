kjh-vita (forked on github from Kieran Healy http://www.kieranhealy.org/)
Steve Koch stevekochscience@gmail.com
License: as open as Kieran Healy intended
========

A simple LaTeX template that Kieran used for his Vita that he decide to share.

I'm new to latex (and fairly new to unix, so here are some newbie instructions for getting it to work):

1. Upgraded latex, following the directions on this page, with modifications: http://askubuntu.com/questions/163682/how-do-i-install-the-latest-tex-live-2012#comment284348_163683
    
    sudo add-apt-repository ppa:texlive-backports/ppa (add-atp- instead of apt-add)
    sudo apt-get install texlive

2. As suggested by Kieran, comment out the font specs, since I think they need to be purchased and can do that later.

3. Got rid of "blueviolet" error by switching to "xcolor" package from "color" on line 82

4. Look into alternative package for git: http://ctan.org/pkg/gitinfo

5. Need to create the vc.tex file. I still need to figure out how to automate this to update whenever I want. E.g. when I make a commit. For now, the following worked:

5a. Get file vc and vc-git.awk, put into working directory for cv.
5b. Make vc executable (chmod +x vc)
5c. Run vc script to create vc.tex (I think this only works after setting up the git repository)

    sh ./vc
    
    

sh ./vc


 
